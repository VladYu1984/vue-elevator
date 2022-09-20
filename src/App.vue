<template>
  <div class="main">
    <img id ="stop" class="stop" src="data:image/png;base64,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" alt="Stop">
    
    <table>
      <tr><td class="elevator_sh"> </td><td><button id="call5" @click="elevatorCall(5)">5</button> </td></tr>
      <tr><td class="elevator_sh"> </td><td><button id="call4" @click="elevatorCall(4)">4</button> </td></tr>
      <tr><td class="elevator_sh"> </td><td><button id="call3" @click="elevatorCall(3)">3</button> </td></tr>
      <tr><td class="elevator_sh"> </td><td><button id="call2" @click="elevatorCall(2)">2</button> </td></tr>
      <tr><td class="elevator_sh"> </td><td><button id="call1" @click="elevatorCall(1)">1</button> </td></tr>
      <div id="elev" class="elev">
      <img id="elevator" class="elevator" src="data:image/jpeg;base64,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" @transitionend="elevatorStop()"/>
      </div>
    </table>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {},
  data(){
    return{
      calls: [],
      call: 0,
    }
  },
  mounted(){ 
    if(localStorage.getItem('call') != 0){
      this.call = localStorage.getItem('call')
    }else{
      this.call = 0
    }
    if(JSON.parse(localStorage.getItem('calls')).length != 0){
      this.calls = this.calls.concat(JSON.parse(localStorage.getItem('calls')))
    }else{
      this.calls.length = 0
    }
    this.elevatorMove()
  },
  methods: {
    elevatorCall(lvl){
      if(this.calls.length > 0){
        for(let i=0; i<this.calls.length; i++){
          if(lvl == this.calls[i]){
            return;
          }
        }
      }
      this.calls.push(lvl)
      this.command_calls()
    },
    command_calls(){
      document.getElementById('stop').style.display = 'none'
      if(this.calls.length > 0){
        this.call = this.calls[0]
        localStorage.setItem('call', this.call)
        setTimeout(this.elevatorMove, 500)
      }
    },
    elevatorMove() {
      let options = { 
        5: '65px',
        4: '225px',
        3: '380px',
        2: '540px',
        1: '700px'
      }
      document.getElementById('elevator').style.top = options[this.call]
    }, 
    elevatorStop(){
      this.calls.shift()
      localStorage.setItem('calls', JSON.stringify(this.calls))
      document.getElementById('stop').style.display = 'block'
      setTimeout(this.command_calls, 3000)
    },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
table {
   border: 1px solid black;
    width: 1500px;
    height: 500px;
    text-align: left;
}
tr{
  border: 1px solid black;
  width: 1000px;
}
td {
   border: 2px solid black;
}
td.elevator_sh{
  width: 150px;
  height: 150px;
}
img{
  width: 150px;
  height: 150px;
  position: absolute;
  transition: all 2.7s ease-in-out;
  -webkit-transition: all 2.7s ease-in-out; /** Chrome & Safari **/
  -moz-transition: all 2.7s ease-in-out; /** Firefox **/
  -o-transition: all 2.7s ease-in-out; /** Opera **/
}
.elevator{
    top: 699px;
    left: 15px;
}
img.up{
  display: none;
  padding-left: 900px;
  margin-left: 610px;
}
img.down{
  display: none;
  margin-left: 1500px;
  margin-top: 650px;
}
img.stop{
  display: none;
  margin-left: 1500px;
  margin-top: 300px;
}
</style>