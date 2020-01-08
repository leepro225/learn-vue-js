# 컴포넌트 개념 

#### 컴포넌트
    
재사용성을 올리기 위해 화면의 영역을 나누어 컴포넌트 단위로 개발  
컴포넌트 간의 관계가 생긴다


#### 전역 컴포넌트 등록

    <div id="app">
        <app-header></app-header>
    </div>
    
    Vue.component('app-content', {
        template : '<h1>Header</h1>'
    });
    
    new Vue({
        el : '#app'
    });
    
실무에서는 잘 쓰지 않음!



#### 지역 컴포넌트 등록

    new Vue({
        el : '#app',
        components : {
            // '컴포넌트 이름' : 컴포넌트 내용
            'app-footer' : {
                template : '<footer>something</footer>
            }
        }
    });

