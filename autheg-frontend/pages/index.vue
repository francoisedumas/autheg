<template>
  <v-layout>
    <v-flex>
      <v-list>
        <v-list-item v-for="example in examples" :key="example.id" :class="example.colour">
          <v-list-item-content>{{example.name}}</v-list-item-content>
        </v-list-item>
      </v-list>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data () {
    return {
      examples: []
    }
  },
  methods: {
    async updateExamples() {
      this.examples = await this.$axios.$get('/examples')
    }
  },
  mounted () {
    this.updateExamples()
  }
}
</script>