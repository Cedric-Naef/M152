<template>
<div class="main">
    <Subject :subject="subject" />
    <Summary :summary="summary" />
</div>
</template>

<script>
import Subject from './components/Subject.vue'
import Summary from './components/Summary.vue'

    export default {
        components: {Subject, Summary},
        data: function() {
            return {
                subjects: [
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
                        grades: [4.25,3.4,3.5]
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
    }
</style>