# Transition

## 속성

1. transition-property: 트랜지션을 적용해야 하는 CSS 속성 명시(단, 수치로 표현된 값만 적용)

    ```css
    transition-property: all; // default
    transition-property: margin-right, color, height;
    ```

2. transition-duration: 트랜지션 지속 시간

    ```css
    transition-duration: 1s;
    ```

3. transition-timing-function: 속성의 중간값을 게산하는 방법을 정의하는 함수

    ```css
    transition-timing-function: ease; // default
    transition-timing-function: linear;
    transition-timing-function: step-end;
    ```
    ![캡처](https://user-images.githubusercontent.com/39231606/120195732-12038d80-c25a-11eb-84b3-ecbaf5048870.PNG)


4. transition-delay: 트랜지션이 시작되기까지 기다리는 시간

   ```css
   transition-delay: 0s; // default
   transition-delay: 0.5s; 
   ```

#### 단축 문법 

```css
transition: <property> <duration> <timing-function> <delay>;
```
