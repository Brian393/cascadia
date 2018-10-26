<style scoped>
.video {
position: relative; padding-bottom: 56.25%; height: 0;
}
.video iframe {
position: absolute; top: 0; left: 0; width: 100%; height: 100%;
}
.quote {
font-weight: bold; font-style: italic; color: #333333;  text-align: center;
}
.quote-2 {
font-weight: bold; font-style: italic; color: #333333;
}
</style>

<template>
  <div class="aside-content">
    <div class="title">
      <h1>Messenger of nature</h1>
    </div>
    <div class="video">
      <iframe width="350" height="197" src="https://www.youtube.com/embed/hERlmXgqv7o?&amp;start=87&amp;autoplay=1&amp;mute=0&amp;loop=1&amp;playlist=hERlmXgqv7o" frameborder="0" allow="autoplay; encrypted-media; loop" allowfullscreen></iframe>
    </div>
    <div class="caption">A voyage from land to sea and back again<br>&mdash;video by Diarmuid, <a href="https://www.youtube.com/channel/UCLAqBw-p3I6918YOVCIcIVQ">here</a>&mdash;</div>
    <br>
    <Accordion :open="false">
      <h3 slot="header">Legends</h3>
      <div class="flex">
        <img src="images/ChinookAlevin.png" class="fullwidth"><br>Chinook alevin, <a href="https://www.seattleaquarium.org/blog/redd-alert-our-chinook-salmon-are-hatching">source</a>
      </div>
    </Accordion>
    <br>
    <p>What you see are the critical habitat areas of Chinook, Coho, Chum and Sockeye salmon in the US Pacific Northwest. Critical habitat means stream reaches that have been determined essential to the continuing health of unique populations. The image blurs the movements of these populations into bifurcating streams of color: survival lines. They ask you how the salmon maintain a generational bond between the mountains and the ocean, and whether you can do so with them.</p>

    <p>The data prepared by the National Oceanic and Atmospheric Administration are far more complex than any single line could reveal. They divide the four endangered species not only into seasonal runs but also into distinct gene pools, associated with the real pools and gravel beds that call the fish back to spawn. Further documents locate the areas where populations have gone extinct, or where stream reaches have been entirely blocked by dams. Other studies try to assess the geographical range in which the fish could potentially flourish. This kind of science is beautiful, because it opens windows into non-human worlds.</p>

    <p>A great challenge for cartography would be to render all this knowledge perceptible in the blink of an eye. But it's not obvious how, and besides, you can get lost in the data. The idea here is to focus on the most powerful message that the salmon have for us now, which is that of finding a pathway to the place where the cycles originate.</p>

    <p>Five maps can be accessed from the buttons below. Roll the cursor over the landscape to find the streams through which each species moves. Locate the places that make you want to come closer. Think about river bends, currents, cascades, dreamy aquascapes and looming threats of all kinds, not just from bears but mostly from human construction and debris and hot water. Can we still feel the link between the oceans and the mountains? Can we help keep this incredible connection alive?</p>
<br>
<Accordion>
  <h3 slot="header">sources</h3>
</Accordion>

</div>
</template>
<style scoped>
.flex {
  display: flex;
  flex-direction: column;
}
.flex div {
  display: flex;
  align-items: center;
  margin-bottom: 0.5em;
}
.flex img {
  margin-right: 0.5em;
}
</style>
<script>
import AppLightBox from '../../components/AppLightBox.vue'
import Accordion from '../../components/Accordion.vue'
import {eventBus} from '../../main'

export default {
  name: 'WatershedFalls',
  components: {
    Accordion,
    AppLightBox
  },
  methods: {
    emit: function (method, args) {
      eventBus.$emit(method, args)
    }
  }
}
</script>