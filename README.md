# Unreal Engine 5 스타일 가이드

원본은 [Allar/ue5-style-guide](https://github.com/Allar/ue5-style-guide) 에 있습니다. 모든 내용이 유익하니 시간을 들여 정독할 가치가 충분하다고 생각합니다.

모든 내용을 번역하기에는 시간이 상당히 오래 걸릴 것 같으니 개인적으로 필요하고 유익하다고 생각되는 내용들 위주로 작성할 예정입니다.  
또한, 제 입맛대로 수정하는 부분도 존재하니 혹시 참고하실 경우 주의하시길 바랍니다.

## Boolean 변수

모든 boolean 변수는 접두사 b 를 사용하며 파스칼 케이스를 사용합니다.

가능한 한 특정 상태를 나타내는 형용사를 사용합니다. 동사는 여러 복잡한 상태를 나타내는 경우가 많기 때문에 최대한 사용하지 않도록 합니다. 이 경우에는 Boolean 대신 Enum 을 사용하도록 합니다.

- `bDead`
- `bHostile`

## 카테고리

블루프린트에서 수정 가능한 변수들은 `Config` 카테고리에 할당합니다.
- 변수가 많은 경우에는 하위 카테고리를 추가합니다.
- 하위 카테고리를 설정할 때는 카테고리 사이에 한 칸씩 여백을 준 다음 `|` 를 추가합니다.
- 예시: `Config | Animations`

## Advanced Display

블루프린트에서 수정이 가능하나 잘 건들지 않는 변수의 경우 `Advanced Display` 옵션을 설정합니다.

## 특정 상태 정보를 Bool 값으로 반환하는 함수의 이름은 질문 형식이어야 합니다.

- `IsDead`
- `IsVisible`
- `CanReload`
- `HasWeapon`

## Posts vs NumPosts or PostsCount

배열은 복수형 명사를 사용하고 특정 객체의 개수를 나타내는 경우에는 `Num` 이나 `Count` 를 붙여 표시합니다.
