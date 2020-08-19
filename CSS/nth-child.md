:nth-child()
-
- A CSS pseudo-class, CSS 의사 클래스(가상 클래스)
- 형제 사이에서의 순서에 따라 요소를 선택한다.

<br />

<h4>형제요소에 각기 다른 스타일을 적용할 때</h4>

HTML

```
<section class="playlist">
    <section class="music-content">
        <div class="music-content__card"></div> // --- 1. color: #F85A2A;
        <div class="music-content__imformation">
            <div class="information__name">Matargasti</div>
            <div class="information__singer">Mohit Chauhan</div>
        </div>
    </section>
    <section class="music-content">
        <div class="music-content__card"></div> // --- 2. color: #FF89BB;
        <div class="music-content__imformation">
            <div class="information__name">Attitude</div>
            <div class="information__singer">Lewis OfMan - Attitude</div>
        </div>
    </section>
    <section class="music-content">
        <div class="music-content__card"></div> // --- 3. color: #1947E5;
        <div class="music-content__imformation">
            <div class="information__name">Try Everything</div>
            <div class="information__singer">Shakira - Zootopia</div>
        </div>
    </section>
    <section class="music-content">
        <div class="music-content__card"></div> // --- 4. color: #00C6AD;
        <div class="music-content__imformation">
            <div class="information__name">Sunflower</div>
            <div class="information__singer">Joseph Vincent - Sunflower</div>
        </div>
    </section>
</section>
```

<br />

CSS

```
// 1 -> 첫 번째 'music-content'의 첫 번째 'div'를 선택
.music-content:nth-child(1) > div:nth-child(1) {
  background-color: #F85A2A;
}

// 2 -> 두 번째 'music-content'의 첫 번째 'div'를 선택
.music-content:nth-child(2) > div:nth-child(1) {
  background-color: #FF89BB;
}

// 3 -> 세 번째 'music-content'의 'music-content__card'를 선택
.music-content:nth-child(3) > .music-content__card {
  background-color: #1947E5;
}

// 4 -> 네 번째 'music-content'의 'music-content__card'를 선택
.music-content:nth-child(4) > .music-content__card {
  background-color: #00C6AD;
}
```
▶ `div:nth-child(1)` === `.music-content__card` <br />
▶ `nth-child(odd)` : 형제 요소에서 홀수 번째(1, 3, 5, ...)인 요소를 나타낸다. <br />
▶ `nth-child(even)` : 형제 요소에서 짝수 번째(2, 4, 6, ...)인 요소를 나타냅니다. <br />
▶ `>`: Child combinator, 첫 번째와 선택자와 일치하는 요소의 직접 자식인 두 번째 선택자와 일치하는 요소만 일치한다.