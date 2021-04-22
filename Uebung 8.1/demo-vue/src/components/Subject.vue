<template>
        <div v-for="subject in subjects" :key="subject.name">
            <h2>{{ subject.name }}</h2>

            <ul>
                <li v-for="grade in subject.grades">{{ grade }}</li>
            </ul>

            Durchschnitt: {{ getAverage(subject.grades) }}
            <hr />
        </div>
</template>

<script>
export default {
  name: 'Subject',
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
        },
        methods: {
            getAverage: function(grades) {
                let total = 0;
                grades.forEach(grade => total += grade);
                const avg = total / grades.length;
                return Math.round(avg * 2) / 2; // Round to 0.5
            }
        }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
