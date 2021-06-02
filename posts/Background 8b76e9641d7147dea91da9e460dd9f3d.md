# Background

# Background-img

- background: center / cover  **no-repeat**  **url('http://~~~~~');**
    - background속성에 순서 상관 없이 넣어도 된다.
    - 단 사이즈는 포지션 다음에 /사용해서 사용해야한다.

    ```css
    background-image: url();
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    ```

    [background](https://mzl.la/3nn6Q2J)

---

- background-image
    - 요소의 배경 이미지 삽입

        ---

    - none  이미지없음       Default Value
    - url("경로")  이미지경로

        ---

    - 배경색상은 이미지 뒤에 나온다.

---

- background-repeat
    - 요소의 배경 이미지 반복

        ---

    - repeat  이미지를 수직, 수평 반복   Default Value
    - repeat-x  이미지를 수평 반복
    - repeat-y  이미지를 수직 반복
    - no-repeat  반복 없음  ⭐️

    ```css
    /* 반복하지 않음 */               이미지영역이 끝나면 **빈공간으로 나타난다.**
    background-repeat: no-repeat;

    /* 가로 방향으로만 반복 */
    background-repeat: repeat-x;

    /* 세로 방향으로만 반복 */
    background-repeat: repeat-y;

    /* 가로와 세로 모두 반복 */
    background-repeat: repeat;

    /* 반복할 수 있는 만큼 반복한 뒤, 남는 공간은 이미지 간의 여백으로 배분 */
    background-repeat: space;

    /* 반복할 수 있는 만큼 반복한 뒤, 남는 공간은 이미지 확대를 통해 배분 */
    background-repeat: round;
    ```

---

- background-position
    - 요소의 배경 이미지 위치

        ---

    - 0% 0%  0% ~ 100% 사이 값    Default Value
    - 1방향 2방향: top, bottom, left, right, center
    - x축 y축  단위: px, em, rem 등

    ```css
    /* 단어로 지정해주기 (가로: left, center, right, 세로: top, center, bottom) */
    /* 아래와 같은 총 9개의 조합이 가능 */
    background-position: left top;
    background-position: left center;
    background-position: left bottom;
    background-position: right top;
    background-position: right center;
    background-position: right bottom;
    background-position: center top;
    background-position: center center;
    background-position: center bottom;

    /* 퍼센트로 지정해주기 (가로: 전체 width의 25% 지점, 세로: 전체 height의 75% 지점 ) */
    background-position: 25% 75%;

    /* 픽셀로 지정하기 (가로: 가장 왼쪽 가장자리에서부터 오른쪽으로 100px 이동한 지점, 세로: 가장 상단 가장자리에서 아래로 200px 이동한 지점) */
    background-position: 100px 200px;
    ```

    [background-position](https://mzl.la/3dVykK5)

---

- background-size
    - 요소의 배경 이미지 크기

        ---

    - auto 이미지의 실제 크기   Default Value
    - 단위: px, em, rem등
    - x축 값만 입력하면 자동으로 y축이 비율에 맞게 조절된다.
    - cover  비율을 유지, 요소의 더 넓은 너비에 맟춤
    - contain  비율을 유지, 요소의 더 짧은 너비에 맟춤

    ```css
    /* 원래 이미지 사이즈대로 출력 */
    background-size: auto;

    /* 화면을 꽉 채우면서, 사진 비율을 유지 */
    background-size: cover;

    /* 가로, 세로 중 먼저 채워지는 쪽에 맞추어서 출력 */
    background-size: contain;

    /* 픽셀값 지정 (가로: 30px, 세로: 50px로 설정) */
    background-size: 30px 50px;

    /* 퍼센트값 지정 (가로: 부모 요소 width의 60%, 세로: 부모 요소 height의 70%로 설정) */
    background-size: 60% 70%;
    ```

---

- background-attachment
    - 요소의 배경 이미지 스크롤 특성

        ---

    - scroll  이미지가 요소를 따라가서 같이 스크롤     Default Value
    - fixed  이미지가 뷰포트에 고정, 스크롤 x
    - local  요소 내 스크롤 시 임지가 같이 스크롤

# Background-color

- background-color
    - 요소의 배경 색상
    - transparent  투명함    Default Value
    - 색상: 지정가능한 색상

        ```css
        /* Keyword values */
        background-color: red;
        background-color: indigo;

        /* Hexadecimal value */
        background-color: #bbff00;    /* Fully opaque */
        background-color: #bf0;       /* Fully opaque shorthand */
        background-color: #11ffee00;  /* Fully transparent */
        background-color: #1fe0;      /* Fully transparent shorthand  */
        background-color: #11ffeeff;  /* Fully opaque */
        background-color: #1fef;      /* Fully opaque shorthand  */

        /* RGB value */
        background-color: rgb(255, 255, 128);        /* Fully opaque */
        background-color: rgba(117, 190, 218, 0.5);  /* 50% transparent */

        /* HSL value */
        background-color: hsl(50, 33%, 25%);         /* Fully opaque */
        background-color: hsla(50, 33%, 25%, 0.75);  /* 75% opaque, i.e. 25% transparent */

        /* Special keyword values */
        background-color: currentcolor;
        background-color: transparent;   /* 배경색이 없습니다. */

        /* Global values */
        background-color: currentcolor;
        background-color: transparent;
        background-color: transparent;
        ```

        [background-color](https://mzl.la/2QVNgif)