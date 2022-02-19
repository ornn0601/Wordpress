# functions 명령어

## 1. 이미지 최대크기 자동조절 삭제  
```php
add_filter( 'big_image_size_threshold', '__return_false' );
```
- 워드프레스에서 이미지 최대크기를 자동 조절하는 기능을 off한다.  