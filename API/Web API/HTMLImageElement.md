Web API > HTMLImageElement
-
HTMLImageElement 인터페이스는 HTML `<img>` 요소를 나타내며 영상 요소를 조작하는 데 사용되는 특성과 방법을 제공한다.

<br />

<h5>Image()</h5>

```
const field = document.querySelector('.game__field');
const bugImg = new Image();
bugImg.src = 'src/img/bug.png';
field.appendChild(bugImg);
```
or <br />
<h5>document.createElement('img')</h5>

```
const field = document.querySelector('.game__field');
const bugImg = document.createElement('img');
function setImg(image) {
    image.style.background = 'url("src/img/bug.pnp")';
	image.style.width = '50px';
	image.style.height = '50px';
	image.style.position = 'absolute';
	image.style.left = '100%';
	image.style.top = '25%';
	image.style.transform = 'translate(-100%, -100%)';
	field.appendChild(image);
}
setImg(bugImg);
```

or <br />
<h5>element.innerHTML</h5>

```
const field = document.querySelector('.game__field');
field.innerHTML = `<img src="src/img/bug.png">`;
```