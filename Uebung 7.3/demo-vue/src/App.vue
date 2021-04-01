<template>
<div class="main">
    <h1>Noten</h1>

    <h2>Alle Noten</h2>
        <ul class="all">
             <li v-for="item in marks">{{ item.name }} {{item.grades}} </li>
        </ul>

    <h2>Durchschnitt</h2>
        <ul class="middle">
             <li v-for="item in marks">{{ item.name }} {{item.grades}} </li>
        </ul>

    <h2>Durchscnitt gesamt</h2>
        <ul class="middleAll">
             <li v-for="item in marks">{{ item.name }} {{item.grades}} </li>
        </ul>

    <h2>Mangelpunkte</h2>
       <ul class="low">
             <li v-for="item in marks">{{ item.name }} {{item.grades}} </li>
       </ul>
</div>
</template>

<script>
 export default{
    data: function() {
        return {
            marks: [
               {
                  name: "Mathematik",
                  grades: [5,4.7,3.5,4.1] 
               },
               {
                name: "Geschichte",
                   grades: [5.5,4.9,5.75] 
               },
               {
                  name: "Physik",
                   grades: [2,2.7,4.3] 
               },
               {
                  name: "Deutsch",
                  grades: [4.25,4.1,3.5] 
              },
           ]
        }
    }
 }


</script>

<style lang="scss">
    .main {
        max-width: 500px;
        margin: 0 auto;
        background-color: #eee;
        padding: 20px;

        h1 {
            text-align: center;
        }

        h1 {
            text-align: center;
        }
    }
</style>
