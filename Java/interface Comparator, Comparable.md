Java 컬렉션 정렬하는 데 필요한 메서드 정의

| Comparable 인터페이스 | Comparator 인터페이스 |
| --- | --- |
| 정렬할 클래스는 java.lang.Comparable 인터페이스를 구현 | 정렬할 클래스는 java.util.Comparator 인터페이스를 구현 |
| 사용자 정의 클래스에 대해서도 정렬할 수 있음 | 사용자 정의 클래스에 대해서도 정렬할 수 있음 |
| compareTo 메서드(정렬될 클래스 타입의 객체를 매개변수로 받으며, 호출한 객체와 매개변수로 주어진 객체를 비교)를 지원 | compare 메서드(매개변수로 주어진 두 객체를 비교)를 지원 + 클래스 내에서 오버로딩 |
| 메서드를 호출한 객체가 매개변수 객체보다 크면 양수, 같으면 0, 작으면 음수를 리턴 | o1이 o2보다 크다면 양수, 같다면 0, 작다면 음수를 리턴 |
| Comparable을 구현한 메서드는 첫번째 Collections.sort() 메서드를 호출 | Comparator를 구현한 클래스는 두번째 Collections.sort() 메서드를 호출<br>💡 Comparable을 구현했는지, Comparator을 구현했는지에 따라 호출하는 Collections.sort() 메서드가 다름(오버로딩) |
| Comparable 정렬은 하나의 오버라이딩 된 메서드를 사용 → 1가지 속성만을 기준으로 정렬할 수 있음 | Comparator 정렬은 클래스를 생성 → 메서드 오버로딩 가능 → 여러 속성을 기준으로 정렬할 수 있음 |
