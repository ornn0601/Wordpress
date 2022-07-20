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

	option.eq(index).prop('selected', true); // 초기 선택을 랜덤으로 선택한다.
	return false;
}
randomSelected();
```

## 4. Random option
```js
jQuery(document).ready(function() {

	let dropdownSelect = $('select[name=o_dropdown-1]');
	let dropdownOption = $('select[name=o_dropdown-1] option');
	let dropdownOptionArr = dropdownOption.toArray();

	// option 배열에서 "first_as_label인 선택해주세요" 삭제 후 배열 다시 만들기
	let newOptionArr = dropdownOptionArr.slice(1);

	function selectOptionShuffle(array) {
		let arr = array.sort(() => Math.random() - 0.5);

		// html 삽입
		for ( var i = 0; i < arr.length; i++ ) {
			dropdownSelect.append(arr[i]);
		}

	}
	selectOptionShuffle(newOptionArr);
	```
