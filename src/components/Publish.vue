<template>
  <div class="publish">
    <button @click="publish1">Publish1</button>
    <button @click="publish2">Publish2</button>
  </div>
</template>

<script>
export default {
  methods: {
    publish1 () {
      this.$mqtt.publish('VueMqtt/publish1', 'message to Sub1')
    },
    publish2 () {
      this.$mqtt.publish('VueMqtt/publish2', 'message to Sub2')
    }
  },
  mqtt: {
    publish1 (data) {
      console.log(String.fromCharCode.apply(null, data))
    },
    publish2 (data) {
      console.log(String.fromCharCode.apply(null, data))
    }
  }
}
</script>
