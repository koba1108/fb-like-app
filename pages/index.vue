<template>
  <div style="padding-bottom: 52px;">
    <TheHeader/>
    <main>
      <TweetBox/>
      <Timeline/>
    </main>
    <TheNav/>
  </div>
</template>

<script>
  import TheHeader from '../components/TheHeader'
  import TheNav from '../components/TheNav'
  import TweetBox from '../components/TweetBox'
  import Timeline from '../components/Timeline'

  export default {
    components: {
      Timeline,
      TweetBox,
      TheNav,
      TheHeader,
    },
  }
</script>
