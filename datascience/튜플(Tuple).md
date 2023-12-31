튜플(Tuple)은 [[관계형 데이터베이스(Relational Database)]]에서 사용되는 중요한 개념으로, 테이블(Table)에 저장되는 [[데이터(Data)]] 레코드(Record)를 나타냅니다. 튜플은 테이블의 각 행(Row)에 해당하며, 테이블의 각 열(Column)에 포함된 데이터 값을 가집니다. 다음은 튜플의 주요 특징과 관련된 개념입니다:

1. **데이터 레코드**: 튜플은 데이터베이스 테이블에 저장되는 개별적인 데이터 레코드를 나타냅니다. 각 튜플은 테이블의 열에 따라 데이터 값이 채워진다.

2. **고유 식별자**: 튜플은 테이블 내에서 고유한 식별자를 가질 수 있습니다. 이 식별자는 튜플을 구분하고 검색할 때 사용됩니다. 이러한 식별자를 주요 키(Primary Key)라고 부릅니다.

3. **튜플 내 데이터**: 튜플 내의 각 데이터 값은 특정 열에 대응하며, 튜플의 순서대로 배열되어 있습니다. 예를 들어, "Customers" 테이블의 튜플은 고객의 이름, 주소, 전화번호 등의 정보를 포함할 수 있습니다.

   ```
   (1, 'John', 'Doe', 'john@example.com')
   ```

4. **불변성(Immutability)**: 튜플은 일반적으로 불변(Immutable)합니다. 이것은 한 번 생성되면 튜플 내의 데이터 값을 변경할 수 없다는 의미입니다. 데이터를 업데이트하려면 새로운 튜플을 생성해야 합니다.

5. **다수의 열**: 튜플은 테이블의 여러 열에 대한 데이터를 포함할 수 있으며, 테이블의 구조에 따라 필요한 만큼의 열을 가질 수 있습니다.

6. **튜플 연산**: SQL과 같은 데이터베이스 쿼리 언어를 사용하여 튜플에 대한 다양한 연산을 수행할 수 있습니다. 예를 들어, 데이터 검색, 삽입, 갱신, 삭제 등의 연산이 가능합니다.

테이블의 각 튜플은 튜플 내의 데이터 값이 해당 열의 데이터 유형과 일치해야 합니다. 관계형 데이터베이스에서 튜플은 데이터의 무결성을 유지하기 위해 중요한 역할을 합니다. 이러한 데이터 무결성은 데이터베이스의 정확성과 일관성을 보장하며, 주요 키(Primary Key) 및 외래 키(Foreign Key)와 함께 데이터의 신뢰성을 제공합니다.

튜플은 데이터베이스의 쿼리 작업에서 사용되며, 특정 조건을 만족하는 튜플을 선택하거나 데이터를 필터링하고 정렬하는 데 사용됩니다.