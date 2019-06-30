<template>
  <div class="sample01">
    <input type="text" v-model="message" />
    <h2 v-text="message"></h2>

    <input type="checkbox" :value="fruits[0].id" v-model="fruits[0].checked">{{fruits[0].value}},
    <input type="checkbox" :value="fruits[1].id" v-model="fruits[1].checked">{{fruits[1].value}},
    <input type="checkbox" :value="fruits[2].id" v-model="fruits[2].checked">{{fruits[2].value}},
    <input type="checkbox" :value="fruits[3].id" v-model="fruits[3].checked">{{fruits[3].value}},
    <input type="checkbox" :value="fruits[4].id" v-model="fruits[4].checked">{{fruits[4].value}},

    <div>
      checked :
      <span>{{filtered.length}}</span>
    </div>
<!--    <div>-->
<!--      fruits :-->
<!--      <span>{{filtered}}</span>-->
<!--    </div>-->
    <table align="center">
      <tr v-for="fruit in filtered">
        <td>{{fruit.id}}</td>
        <td>{{fruit.value}}</td>
        <td>{{fruit.checked}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  computed: {
      filtered: function() {
        return this.fruits.filter(function (item) {
          return item.checked
        });
    }
  },
  data() {
    return {
      message: 'default input value',
      fruits: [
        {
          id: 1,
          value: '사과',
          checked: true
        },
        {
          id: 2,
          value: '귤',
          checked: false
        },
        {
          id: 3,
          value: '파인애플',
          checked: false
        },
        {
          id: 4,
          value: '바나나',
          checked: false
        },
        {
          id: 5,
          value: '배',
          checked: false
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
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
