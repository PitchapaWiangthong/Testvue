<template>
  <div>
    <h1>{{ HeaderWeb }}</h1>

    <ul>
      <li>
        <router-link to="/"><button>Home</button></router-link>
      </li>
      <li>
        <router-link to="/demo1"><button>Demo1</button></router-link>
      </li>
      <li>
        <router-link to="/demo2"><button>Demo2</button></router-link>
      </li>
      <li>
        <router-link to="/demo3"><button>Demo3</button></router-link>
      </li>
      <li>
        <router-link to="/demo4"><button>Demo4 compute</button></router-link>
      </li>
      <li>
        <router-link to="/demo5"><button>Demo5 binding</button></router-link>
      </li>
      <li>
        <router-link to="/demo6"><button>Demo6 form</button></router-link>
      </li>
    </ul>

    <router-view></router-view>

  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      HeaderWeb: "Welcome To My Website",
    };
  },
};
</script>

<style scoped>
ul {
  margin: 0;
  padding: 0;
}
li {
  display: inline;
  margin-right: 10px;
}
.title{
  font-size: 100px;
  color: aquamarine;
}
</style>

<style>
.content{
  color: rgb(134, 4, 255);
}
</style>