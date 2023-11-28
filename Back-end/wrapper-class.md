# Wapper Class

8개의 기본형을 객체로 다뤄야할 떄 사용하는 클래스

Java(=객체지향언어)에서 모든 것이 객체로 구성되어있어야함

기본형을 제외하지 않은 이유는 성능!! 때문

- 기본형(직접 접근) -> int i = 10;
- 참조형(참조변수 내에 주소 읽고 찾아가서 접근) -> Integer i2 = new Integer("100");

결국, i == i2 // false, i.equals(i2) //true, i.compareTo(i2)=0

.equals() => 같으면 true / 다르면 false
.compareTo() => 같으면 0 / 오른쪽 값이 작으면 양수 / 오른쪽 값이 크면 음수(정렬할 때 사용)

| 원시 타입(Primitive Type) | 참조타입(Reference Type) |
| ------------------------- | ------------------------ |
| boolean                   | Boolean                  |
| char                      | Character                |
| byte                      | Byte                     |
| short                     | Short                    |
| int                       | Integer                  |
| long                      | Long                     |
| float                     | Float                    |
| double                    | Double                   |
