## Comparable 인터페이스와 Comparator 인터페이스
Java 컬렉션 정렬하는 데 필요한 메서드 정의

### Comparable
정렬할 클래스는 java.lang.Comparable 인터페이스를 구현해야 한다.
사용자 정의 클래스에 대해서도 정렬할 수 있다.
Comparable 인터페이스는 compareTo 메서드를 지원하며, 이 메서드는 매개변수로 정렬될 클래스 타입의 객체를 받는다.
메서드를 호출한 객체가, 매개변수 객체보다 크면 양수, 같으면 0, 작으면 음수를 리턴하도록 구현을 강제한다.
Comparable을 구현한 메서드는 첫번째 Collections.sort() 메서드를 호출한다.

### Comparator
정렬할 클래스는 java.util.Comparator 인터페이스를 구현해야 한다.
Comparable과 마찬가지로 사용자 정의 클래스에 대해서도 정렬할 수 있다.
Comparator 인터페이스는 compare 메서드를 지원하며, 클래스 내에서 오버라이드 하면 된다.
o1이 o2보다 크다면 양수, 같다면 0, 작다면 음수를 리턴하면 된다.
Comparator를 구현한 클래스는 두번째 Collections.sort() 메서드를 호출한다.

## Comparable vs Comparator
Comparable을 구현했는지, Comparator을 구현했는지에 따라 호출하는 Collections.sort() 메서드가 다르다. (오버로드)
Comparable의 compareTo 메서드는 호출한 객체와 매개변수로 주어진 객체를 비교한다.
Comparator의 compare 메서드는 매개변수로 주어진 두 객체를 비교한다.
Comparable 정렬은 하나의 오버라이딩 된 메서드를 사용하기 때문에, 한가지 속성만을 기준으로 정렬할 수 있다.
Comparator 정렬은 클래스를 생성하기 때문에, 메서드를 오버로딩 할 수 있어서, 여러 속성을 기준으로 정렬할 수 있다.
