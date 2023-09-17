```React
//app/[company]/page.js
  useEffect(() => {

    const fetchData = async (endpoint, setter) => {

      try {

        const response = await fetch(

          `/api/${endpoint}?symbol=${props.params.company}`

        );

        const data = await response.json();

        setter(data);

      } catch (error) {

        console.error(`Error fetching ${endpoint} data:`, error);

      }

    };
```