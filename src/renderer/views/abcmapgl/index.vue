<template>
  <div id="asd" :class="$style.container">
    abcmapgl啊啊asdasd
  </div>
</template>

<script setup lang="ts">
import { useRoute, useRouter } from '@common/utils/vueRouter'
import { ref, computed, nextTick, onMounted } from '@common/utils/vueTools'
import maplibregl from 'maplibre-gl'

const route = useRoute()
const router = useRouter()
console.log('setup', maplibregl)

onMounted(() => {
  console.log('onMounted', maplibregl)
  const map = new maplibregl.Map({
    container: 'asd',
    style: 'https://demotiles.maplibre.org/style.json', // stylesheet location
    center: [-74.5, 40], // starting position [lng, lat]
    zoom: 9, // starting zoom
  })
})

</script>

<style lang="less" module>
.container {
  border: red solid 2px;
}

.header {
  // padding: 5px 0;
  flex: none;
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-between;
}

.main {
  position: relative;
  flex: auto;
  // min-height: 0;
}
</style>
