# form 태그로 데이터 보내기

      <template>1
        <form v-on:submit.prevent="submitForm"> // event modifyer? .prevent 이벤트의 기본 동작을 막겟다!
          <div>
            <label for="username">id: </label>
            <input id="username" type="text" v-model="username"> // 양방향 데이터 바인딩, data의 username이랑 연결됨
          </div>
          <div>
            <label for="password">pw: </label>
            <input id="password" type="password" v-model="password">
          </div>
          <button type="submit">login</button>
        </form>
      </template>

      <script>
      import axios from 'axios';
      export default {
        data: function() {
          return {
            username: '',
            password: '',
          }
        },
        methods: {
          submitForm: function() {
            // event.preventDefault(); -> form태그 특성상 새로고침되는 것을 막아주는 거
            console.log(this.username, this.password);
            var url = 'https://jsonplaceholder.typicode.com/users';
            var data = {
              username: this.username,
              password: this.password
            }
            axios.post(url, data)
              .then(function(response) {
                console.log(response);
              })
              .catch(function(error) {
                console.log(error);
              });
          }
        }
      }
      </script>
      
      
      
      
  이벤트 버블링 참고 : https://joshua1988.github.io/web-development/javascript/event-propagation-delegation/
