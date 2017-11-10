<template>
  <div class="sub" v-html="buff">
  </div>
</template>

<script>
export default {
  data () {
    return {
      buff: 'Sub3:<br>'
    }
  },
  mqtt: {
    /** 'VueMqtt/#' or 'VueMqtt/+' or '+/+' or '#' */
    'VueMqtt/+' (data, topic) {
      if (topic.split('/').pop() === 'publish1') {
        console.log('topic:', 'VueMqtt/publish1')
      }
      this.buff = this.buff + data + '<br>'
    }
  }
}
</script>
