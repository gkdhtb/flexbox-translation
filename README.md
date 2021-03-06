# [번역] A Complete Guide to Flexbox
- 원문: https://css-tricks.com/snippets/css/a-guide-to-flexbox/
## 배경
Flexbox Layout(Flexible Box) 모듈은 컨테이너의 사이즈를 모르거나 유동적인 상황에서도 컨테이너 속 아이템들의
<br>더 효과적인 레이아웃, 정렬, 간격 분배를 제공하는 것을 목표로 하고 있다.

Flex layout의 주요 쟁점은 가능한 공간(디바이스 디스플레이 종류나 스크린 사이즈에 따른)을 최상의 방법으로 채울 수 있게 컨테이너에게 아이템들의 너비와 높이,순서를 바꿀수 있는 능력을 주는 것이다. Flex 컨테이너는 가능한 여유 공간을 채우면서 아이템을 확장시킬 수 있고, 넘치는 것을 방지하기 위해 아이템을 수축시킬 수 있다.

가장 중요한 것은. Flexbox layout은 일반적인 레이아웃 (block: 수직기반, inline: 수평기반) 과는 다르게 **방향에 종속적이지 않다.** 
<br>Flexbox layout은 페이지들에서 잘 동작하지만, 크고 복잡한 어플리케이션을 지원하기엔 유연성이 부족하다.

> **NOTE**
<br>Flexbox Layout은 어플리케이션의 컴포넌트 단위와 작은 규모의 레이아웃에 가장 적절하며, 
<br>큰 규모의 레이아웃에는 *'Grid'* 를 사용하는 것이 적절하다.

## 기초 & 용어
Flexbox는 하나의 속성이 아닌 전체 모듈이기 때문에, 이것은 많은 속성 쌍을 포함하고 있다. 
<br>속성들 중 일부는 컨테이너('flex container'인 부모 요소)에 사용하고, 나머지는 'flex items'이라 불리우는 자식요소에서 사용한다.

'보통의'레이아웃이 블럭과 인라인 플로우 방향에 놓인다면, flex 레이아웃은 'flex-flow 방향'에 놓이게된다.
<br>flex 레이아웃의 주요 아이디어를 설명하는 아래의 그림을 유심히 살펴보자. 
![flex basic](https://user-images.githubusercontent.com/22817401/50204191-51e69b00-03a7-11e9-80df-adc10fa4efe6.jpeg)
아이템들은 **메인축**(main-start 부터 main-end) 또는 **교차축**(cross-start 부터 cros-end)에 따라서 배치된다.

- **main axis :** flex 컨테이너의 메인축은 flex 아이템들이 배치되는 기본축이다. 메인축은 반드시 수평축이 될 필요는 없다. 
<br>메인 축은 flex-direction 속성에 의존한다.
- **main-start | main-end :** flex 아이템들은 main-start에서 시작해서 main-end로 가면서 컨테이너 안에 위치하게 된다.
- **main-size :** 기본 치수 안에 있는 flex 아이템의 너비 또는 높이가 그 아이템의 기본 크기이다.
- **cross axis :** 매안 축의 수직축을 cross axis 라고 부른다. cross axis의 방향은 메인 축의 방향에 의존한다.
- **cross-start | cross-end :**
