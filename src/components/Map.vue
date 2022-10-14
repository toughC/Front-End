<template>
  <div id="map">
    <BottomNav></BottomNav>
  </div>
</template>
  
<script>
import BottomNav from "./BottomNav.vue";

export default {
  name: 'Map',
  data() {
    return {

    }
  },
  components: {
    BottomNav: BottomNav,
  },
  mounted() {
    // this.getMarkerData(); // 단말 데이터 불러오기
    // this.getData(); // 기상 데이터 불러오기

    // window 객체에 kakao가 등록되어있는지 확인하고, 없을 때만 로딩
    if (!window.kakao || !window.kakao.maps) {
      // script 태그 객체 생성
      const script = document.createElement("script");
      // src 속성을 추가하며 .env.local에 등록한 service 키 활용
      script.src = '//dapi.kakao.com/v2/maps/sdk.js?autoload=false&appkey=b88b3479010b6ac898d720fce45a3927';

      // javascript를 통해서 script를 로딩 시켰으므로, 로딩 완료에 대한 감지도 역시 javascript를 통해서 이뤄져야 함
      // 로딩 완료 시점을 파악하기 위해 load 이벤트 사용
      // 동적 로딩을 위해서 autoload=false 추가

      /* global kakao */
      script.onload = () => kakao.maps.load(this.initMap);


      // script.addEventListener("load", () => {
      //   kakao.maps.load(this.initMap);
      //   // console.log("loaded", window.kakao);
      // });

      // document의 head에 script 추가
      document.head.appendChild(script);
    }
    else {
      console.log("이미 로딩됨 : ", window.kakao);
      this.initMap();
    }
  },
  methods: {
    // 맵 생성
    initMap() {
      // 맵 생성
      if (this.map == null) {
        const container = document.getElementById("map");
        const options = {
          center: new kakao.maps.LatLng(35.14932, 129.11462, 16),
          level: 6,
        };


        this.map = new kakao.maps.Map(container, options);
      }

      console.log("맵을 불러왔어!");
    },
  }
}
</script>
  
<style>
@import "../css/map.css";
</style>
  