# CONTACT FORM 7  

## 1. form에 id와 class 넣기
```html
[contact-form-7 id="01" title="title" html_id="id" html_class="class"]
```  
- html_id, html_class를 추가하여 form를 컨트롤 할 수 있는 네임속성을 부여한다.  

## 2. label의 for와 input의 id 연결하기  
```html
<label for="userName">name</label>
[text* name id:userName class="form-control" placeholder "Enter your name"]
```  

## 4. Random selected  
```js
function randomSelected() {
	let select = $('select[name=dropdown]');
	let option = select.find('option');
	let index = Math.floor(Math.random() * option.length);
	option.eq(index).prop('selected', true); // 초기 선택을 랜덤으로 해준다.
	return false;
}
randomSelected();
```