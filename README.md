## 회사 홍보 반응형 웹페이지

### 🖥환경
- HTML
- CSS
- Bootstrap
- jQuery
- 카카오 API

### 🖼썸네일
![05-full](https://user-images.githubusercontent.com/83056872/128047862-d9064f89-883b-41f7-b13a-796c7927b5d7.jpg)

### ✍중요

**카카오 API를 이용하여 지정위치 보여주기**
![지도](https://user-images.githubusercontent.com/83056872/128048296-d2da4f28-9074-499c-a9ac-9eb14e221bc0.JPG)
```html
<div id="map" class="container-fluid text-center">
    <h2>오시는길</h2>
    <div id="kakaomap" style="width: 100%;height: 500px;"></div>
    <script type="text/javascript" src="//dapi.kakao.com/v2/maps/sdk.js?appkey=1b64a4ecf605e8f55bd0b3f1be7b9340"></script>
    <script> 
        var mapContainer = document.getElementById('kakaomap'), // 지도를 표시할 div 
        mapOption = { 
                center: new daum.maps.LatLng(37.52538287504007, 126.89139198462752), // 지도의 중심좌표
                level: 3 // 지도의 확대 레벨
            };

        var map = new daum.maps.Map(mapContainer, mapOption); // 지도를 생성합니다

        // 마커가 표시될 위치입니다 
        var markerPosition  = new daum.maps.LatLng(37.52538287504007, 126.89139198462752); 

        // 마커를 생성합니다
        var marker = new daum.maps.Marker({
            position: markerPosition
        });

        // 마커가 지도 위에 표시되도록 설정합니다
        marker.setMap(map);
    </script>
</div>
```

**jQuery Smooth Scroll 플러그인**
```javascript
<script>
    $(document).ready(function(){
        // Add smooth scrolling to all links in navbar + footer link
        $(".navbar a, footer a[href='#myPage']").on('click', function(event) {
    
        // Make sure this.hash has a value before overriding default behavior
        if (this.hash !== "") {
    
        // Prevent default anchor click behavior
        event.preventDefault();
    
        // Store hash
        var hash = this.hash;
    
        // Using jQuery's animate() method to add smooth page scroll
        // The optional number (900) specifies the number of milliseconds it takes to scroll to the specified area
        $('html, body').animate({
            scrollTop: $(hash).offset().top
        }, 900, function(){
    
            // Add hash (#) to URL when done scrolling (default click behavior)
            window.location.hash = hash;
            });
        } // End if
        });
    })
</script>
```

### 🏷URL
http://leap22.dothome.co.kr/company/
