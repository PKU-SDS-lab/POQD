<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Overview from './sections/Overview.vue'
import Detail from './sections/Detail.vue'
import Result from './sections/Result.vue'
import BibTeX from './sections/BibTeX.vue'
import Motivation from './sections/Motivation.vue'
export default {
  components: {
    Title,
    Abstract,
    Motivation,
    // Overview,
	  Detail,
	  Result,
    BibTeX
  }
}
</script>

<template>
  <Title/>
  <Abstract/>
  <Motivation/>
  <!-- <Overview/> -->
  <Detail/>
  <Result/>
  <BibTeX/>
</template>