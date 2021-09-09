# navercafe-traceremover.js
네이버 카페에서 게시물과 댓글을 지워주는 Script 입니다. 


~~~javascript
(function deleteComment(interval){
    const cafe_document = document.getElementById('cafe_main').contentWindow.document;
    const cafe_window = document.getElementById('cafe_main').contentWindow.window;
    cafe_window.confirm = () => true;
    cafe_document.getElementById('chk_all').click();
    cafe_document.getElementsByClassName('BaseButton BaseButton--skinGray size_default')[0].click();
    setInterval(()=>deleteComment(interval), interval);
})(10000); //10000자리에 적당한 숫자를 ms 단위로 입력해주세요. 너무 짧게하면 차단당합니다. 
~~~
