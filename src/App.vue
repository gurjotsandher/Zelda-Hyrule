<template>
  <div class="app">
    <p> {{ jobs[0].location }}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from 'vue';
import Job from './types/Job';

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    //// Both reactive and refs can be used

    // REACTIVE
    // const state = reactive({
    //   name: 'Link',
    //   age: 25 as string | number
    // })

    
    // return { ...toRefs(state)  }
    
    // REFERENCE
    // const name = ref<string>('Link')
    // const age = ref<number|string>(10)

    // return { name, age }

    const jobs = ref<Job[]>([
      { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
      { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
      { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' }
    ])

    return { jobs }
  },
  // methods: {
  //   changeName(name: string) {
  //     this.name = name;
  //     return name;
  //   },
  //   changeAge(age: string | number) {
  //     this.age = age
  //     return age;
  //   }
  // }
});
</script>

<style>

</style>
