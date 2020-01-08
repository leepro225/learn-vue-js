# 인스턴스 개념 

#### 인스턴스 new Vue()
    function Vue() {
      this.logText = function() {
        console.log('hello');
      }
    const vm = new Vue();
    
    vm.logText(); // hello
    
vue안의 내장 객체들을 사용하기 위해 인스턴스를 생성한다.

    const vm = new Vue({
      el : '#app',
      data : {
        message : 'hi'
      }
    });
 
안은 객체!

