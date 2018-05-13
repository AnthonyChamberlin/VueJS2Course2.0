<template>
    <div id="ninjas">
        <ul>
            <li 
                v-for="ninja in ninjas" 
                @click="ninja.show = !ninja.show"
                :key="ninja.id"
            >
                <h3>{{ ninja.name }}</h3>
                <h4 v-show="ninja.show">{{ ninja.speciality }}</h4>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
  data() {
      return {
        ninjas: [
            {name: "Ant", speciality:"Dev Stuff", show: false},
            {name: "Ben", speciality:"Law", show: false},
            {name: "Joe", speciality:"Engineering", show: false},
            {name: "Dan", speciality:"Saving the World", show: false},
            {name: "Sam", speciality:"Aciton Man", show: false},
            {name: "Dylan", speciality:"Who the fuck is dylan", show: false},
        ]
      }
  }
}
</script>

<style scoped>
#ninjas {
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
}

ul {
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
}

li {
    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;
}
</style>
