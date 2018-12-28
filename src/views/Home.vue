<template>
  <yandex-map 
    :coords="[55.7522200, 37.6155600]"
    zoom="15"
    :controls="[]"
    map-type="map"
		style="width: 100%; height: 100%;">
    
    <ymap-marker 
			marker-type="placemark"
      :marker-id="1"
			:coords="[55.7522200, 37.6155600]"
			hint-content='Домофон1 в кремле'
			:balloon="{header: 'Домофон1 \'Улица\'', body: 'Название улицы', footer: 'Доп инфо'}"
			:icon="{color: 'red', glyph: 'info'}">
		</ymap-marker>
  
    <ymap-marker 
			marker-type="placemark"
      :marker-id="2"
			:coords="[55.7528200, 37.6255600]"
			hint-content='Домофон2 в кремле'
			:balloon="{header: 'Домофон \'Улица\'', body: 'Название улицы', footer: 'Доп инфо'}"
			:icon="{color: 'red', glyph: 'info'}">
		</ymap-marker>

    <ymap-marker 
			marker-type="placemark"
      :marker-id="3"
			:coords="[55.7542200, 37.6175600]"
			hint-content='Домофон2 в кремл'
			:balloon="{header: 'Домофон2 \'Улица\'', body: 'Название улицы', footer: 'Доп инфо'}"
			:icon="{color: 'red', glyph: 'info'}">
		</ymap-marker>

  </yandex-map>
</template>

<script>
  import { yandexMap, ymapMarker } from 'vue-yandex-maps'

  export default {
    components: {
      yandexMap,
      ymapMarker
    }
  }
</script>
