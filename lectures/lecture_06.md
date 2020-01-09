# event emit 개념

### event emit

    <div id="app">
        // <app-header v-on:click="메서드명"></app-header>
           <app-header v-on:click="passEvent"></app-header>
    </div>
    <script>
        const appHeader = {
            template : '<button>header</button>'
        }

        new Vue({
            el : '#app',
            components : {
                'app-header' : 'appHeader'
            },
            data : {
                message : 'hi'
            },
            methods : {
                passEvent : function() {
                    this.$emit('pass');
                }
            }
        });
    </script>
    
 emit은 자식이 부모로 데이터를 보낼때 사용  
 버튼을 클릭하면 passEvent라는 메서드를 실행, 안을 들어가보니 pass라는 메서드를 실행하라고 함.  






![04](./img/04.JPG)

이벤트 이력(logging)을 확인할 수 있는 탭  
<app-header>컴포넌트로부터 pass라는 이벤트가 발생했다는 뜻




