# navercafe-traceremover.js
네이버 카페에서 게시물과 댓글을 지워주는 JavsScript Code 입니다.

<img width="1118" alt="image" src="https://user-images.githubusercontent.com/2310571/200477409-1298f268-d4cb-41e2-aaa0-f2c1871c1fbb.png">


네이버 카페의 내가 쓴 글이나 내가 쓴 댓글 보기에 들어가시고 F12를 누르고 Console에 들어가서 아래 코드를 복붙하세요. (게시글 댓글 둘다 됩니다.)


~~~javascript
setInterval(() => {
    const cafe_document = document.getElementById('cafe_main').contentWindow.document;
    const cafe_window = document.getElementById('cafe_main').contentWindow.window;
    cafe_window.confirm = () => true;
    cafe_document.getElementById('chk_all').click();
    cafe_document.getElementsByClassName('BaseButton BaseButton--skinGray size_default')[0].click();
}, 5000);
//5000자리에 적당한 숫자를 ms 단위로 입력해주세요. 너무 짧게하면 차단당합니다. 
~~~
