<template>
  <div>
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
        <li>
            <el-button type="text">1111</el-button>
            <el-button>sousuo</el-button>
            <el-button type="primary" icon="search"  @click.native="houwa">搜索</el-button>
            <i class="el-icon-loading"></i>
          <i class="el-icon-share"></i>
          <i class="el-icon-edit"></i>
        </li>
    </ul>
    <h2>Ecosystem</h2>

</template>

<script>
    export default {
        name: 'hello',
        data() {
            return {
                msg: 'Welcome to Your Vue.js App'
            }
        },
        methods: {
            startHacking() {
                this.$notify({
                    title: '续一秒',
                    message: 'We have laid the groundwork for you. Now it\'s your time to build something +1S!',
                    duration: 1000
                })
            },
            houwa() {
                this.$message({
                    type: 'success',
                    message: '-1S'
                })
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
    @import "../sass/common.scss";
    h1,
    h2 {
        font-weight: normal;
        @include transform(translate(0, 0))
    }
    
    ;
    ul {
        list-style-type: none;
        padding: 0;
    }
    
    li {
        display: inline-block;
        margin: 0 10px;
    }
    
    a {
        color: #42b983;
    }
</style>