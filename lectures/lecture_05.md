# props 속성

### props 속성

    <div id="app">
        // <app-header v-bind: <span class="evidence">프롭스 속성 이름</span>="상위 컴포넌트의 데이터 이름"></app-header>
           <app-header v-bind:propsData="message"></app-header>
    </div>
    <script>
        const appHeader = {
            template : '<h1>header</h1>',
            props : ['propsData']
        }
        
        new Vue({
            el : '#app',
            components : {
                'app-header' : 'appHeader'
            },
            data : {
                message : 'hi'
            }
        });
    </script>
    






