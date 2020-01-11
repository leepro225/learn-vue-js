# 뷰 라우터

####  뷰 라우터 소개와 설치

싱글 페이지 어플리케이션을 구현을 위한 뷰 라이브러리

### NPM 방식 설치

    npm install vue-router
    

### 라우터 연결하기

    <div id="app"></div>
    
    <script>
        const LoginComponent = {
            template : '<div>login</div>
        }
        
        const Router : new VueRouter({
            // 페이지의 라우팅 정보(어디로 이동할지에 대한 정보)
            routes : [
                {
                    // 페이지의 url 주소
                    path : '/logign',
                    // 해당 url에서 표시될 컴포넌트
                    component : LoginComponent 
                },
                {}                                                                                                                                                                                                                     
            ]
        });
        
        new Vue({
            el : '#app',
            router : Router
        });
    </script>
    
router는 methods처럼 기본 내장된 예약어임. 라우터를 인스턴스화 하고 연결함.

