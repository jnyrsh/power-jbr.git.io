<template>
    <div>
        <div class="he">
            <p class="left" @click="fan()">〈</p>
            <p class="center" :style="{ marginLeft: '31px' }">{{this.$route.query.val}}</p>
            <p class="right" @click="fan()">切换城市</p>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {

        };
    },
    created() {

    },
    mounted() {
        // this.$route.query.val
        console.log(this.$route.query)
    },
    methods: {
        fan(){
            this.$router.go(-1)
        }
    }
};
</script>

<style lang='scss'>
.he {
  width: 100%;
  height: 50px;
  display: flex;
  justify-content: space-between;
  box-sizing: border-box;
  padding: 0 10px;
  color: white;
  background: #3190e8;
  position: fixed;
  z-index: 1000;
  margin-bottom: 50px;
}
</style>
