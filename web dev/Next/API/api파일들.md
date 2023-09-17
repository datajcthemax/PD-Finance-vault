Next에서는 보통 app/pages/api폴더 안에 api파일들을 저장한다.

```javascript
// app/pages/api/stocks.js

import mysql from 'mysql2/promise';

  

export default async function handler(req, res) {

  if (req.method === 'GET') {

    try {

      const connection = await mysql.createConnection({


        host: process.env.DB_HOST,

        port: parseInt(process.env.DB_PORT, 10),

        user: process.env.DB_USER,

        password: process.env.DB_PASSWORD,

        database: process.env.DB_DATABASE,

      });

  

      const query = `

      SELECT s.Symbol, s.Close AS Price, s.Change, s.Volume

      FROM stock_data s

      JOIN (

          SELECT Symbol, MAX(Date) AS MaxDate

          FROM stock_data

          GROUP BY Symbol

      ) latest ON s.Symbol = latest.Symbol AND s.Date = latest.MaxDate

    `;

  

      const [rows] = await connection.execute(query);

      res.status(200).json(rows);

      connection.end();

    } catch (error) {

      console.error('Error fetching stock data:', error);

      res.status(500).json({ error: 'Internal Server Error' });

    }

  } else {

    res.status(405).json({ error: 'Method not allowed' });

  }

}
```

1. `npm install mysql2` [[Next.js]]에서 [[MySQL]]를 사용하기 위해서는 mysql2라는 모듈이 필요하다.
2. `createConnection`메서드를 이용해서 DB정보를 입력한다. 이때 [[Github]]보여서는 안될 중요한 정보는 환경변수로 저장함.
3. [[StockDashboard]]에서 보여주는 데이터는, 가장 최근일 기준으로, 전일 종가, 거래량, 등락률이 필요하니 디비에서 해당 데이터를 가져와주는 쿼리문을 작성해서 `query`변수에 저장.
4. 남은 코드는 데이터 호출 성공/실패, 실패시 에러처리등