# Animation

## 속성

1. animation-duration: 애니메이션 지속 시간

    ```css
    animation-duration: 1s;
    ```

2. animation-timing-function: 중간 상태들의 전환을 어떤 시간간격으로 진행할지 지정

    ```css
    animation-timing-function: ease; // default
    animation-timing-function: linear;
    animation-timing-function: steps(5, end);
    animation-timing-function: cubic-bezier(0.1, -0.6, 0.2, 0);
    ```

3. animation-delay: 언제 애니메이션이 시작될지 지정

   ```css
   animation-delay: 0s; // default
   animation-delay: 0.5s; 
   ```

4. animation-iteration-count: 애니메이션이 몇 번 반복될지 지정

   ```css
   animation-iteration-count: 3;
   animation-iteration-count: infinite; // 무한 반복
   ```

5. animation-direction: 애니메이션이 종료되고 다시 처음부터 시작할지 역방향으로 진행할지 지정

   ```css
   animation-direction: normal; // default
   animation-direction: alternate;
   animation-direction: reverse;
   ```

6. animation-play-state: 애니메이션을 멈추거나 다시 시작

   ```css
   animation-play-state: running; // default
   animation-play-state: paused;  
   ```

### Frame-by-frame animation

png 파일을 이용해서 gif 같은 효과를 낼 수 있는 방법

- 장점
  - 코드로 조작 가능
  - 배경을 투명하게 할 수 있다는 점

```css
@keyframes spaceship-ani {
  to {
    background-position: -2550px 0;
  }
}
/* 고해상도를 위해 픽셀을 원래 이미지의 반으로 지정(원래 이미지 300px)*/
.spaceship {
  width: 150px;
  height: 150px;
  background: url('images/sprite_spaceship.png') no-repeat 0 0 / auto 150px;
  animation: spaceship-ani 1s infinite steps(17);
}
```


> `@keyframes`에서 `0%`는 `from`으로 대체 가능, `100%`는 `to`로 대체 가능
