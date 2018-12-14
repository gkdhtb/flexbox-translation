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
