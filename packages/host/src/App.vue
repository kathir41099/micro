<template>
  <div class="mt-10 text-3xl mx-auto max-w-6xl">
    <Header />
    <div>Name: host</div>
    <div>
      count: {{ count }}
    </div>
    <div>
      <button @click="addOne">
        Add one
      </button>
    </div>
    <div>
      <router-view></router-view>
    </div>
    <!-- <div>Framework: vue3</div>
    <div>Language: JavaScript</div>
    <div>CSS: Tailwind</div> -->
  </div>
</template>

<script>
import { defineAsyncComponent } from 'vue';

// import Header from 'remote/Header'

const Header = defineAsyncComponent(() => import("remote/Header"))

export default {

  components: {
    Header
  },

  computed: {
    count() {
      return this.$store.state.count;
    }
  },

  methods: {
    addOne() {
      this.$store.commit('addOne')
    }
  }

}
</script>