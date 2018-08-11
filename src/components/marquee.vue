<template>
    <!-- 跑马灯效果 -->
    <div>
        <input value="浪起来" type="button" @click="lang"> 
        <input value="低调" type="button" @click="stop">

        <div class="div">{{ msg }}</div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      msg: "猥琐发育！别浪！",
      timer: null
    };
  },
  mounted (){
      this.lang();
  },
  methods: {
    lang() {
        if(this.timer != null) return ;
      this.timer = setInterval(() => {
        var start = this.msg.substring(0, 1);
        var end = this.msg.substring(1);
        this.msg = end + start;
      }, 400);
    },
    stop() {
        clearInterval(this.timer);
        this.timer = null;
    }
  }
};
</script>

<style>
input {
  margin-right: 20px;
}
.div {
  margin-top: 20px;
  margin: 30px;
}
</style>

