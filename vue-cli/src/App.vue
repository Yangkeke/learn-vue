<template>
  <div id="app">
    <h1 v-html="title"></h1>
    <ul>      
      <li v-for="item in items" v-bind:class="{finished: item.isFinished}">
        {{item.label}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      title: 'this is a title',
      items: [
        {
          label: 'coding',
          isFinished: false
        },{
          label: 'sleeping',
          isFinished: true
        }
      ],
      liClass: 'thisisLiClass'
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

.finished{
  color: red;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px;
}
</style>
