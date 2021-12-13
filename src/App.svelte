<script>
  import { Navigation, Pagination, Scrollbar, A11y, Mousewheel } from "swiper";
  import { Swiper, SwiperSlide } from "swiper/svelte";

  // Import Swiper styles
  import "swiper/css";
  import "swiper/css/navigation";
  import "swiper/css/pagination";
  import "swiper/css/scrollbar";

  let swiper = null;

  function onSwiper(e) {
    const [s] = e.detail;
    swiper = s;
  }
  $: console.log(swiper);

  function goTo(page) {
	  try {
		swiper.slideTo(page);
	  } catch (err) {
		  console.log(err)
	  }
	
  }
</script>

<main>
  <Swiper
    modules={[Navigation, A11y, Scrollbar, Mousewheel]}
    slidesPerView={1}
    on:slideChange={() => console.log("slide change")}
    on:swiper={onSwiper}
    mousewheel={{sensitivity: .5}}
	speed={750}
  >
    <SwiperSlide>
		<div class="page page-1">
			<div class="title">Page: Home</div>
			<div class="slide-link" on:click={()=> {goTo(0)}}>Home</div>
			<div class="slide-link" on:click={()=> {goTo(1)}}>Videos</div>
			<div class="slide-link" on:click={()=> {goTo(2)}}>About</div>
			<div class="slide-link" on:click={()=> {goTo(3)}}>Services</div>
			<div class="slide-link" on:click={()=> {goTo(4)}}>Contact</div>
      	</div>
	</SwiperSlide>
    <SwiperSlide>
		<div class="page page-2">
			<div class="title">Page: Videos</div>
			<div class="slide-link" on:click={()=> {goTo(0)}}>Home</div>
			<div class="slide-link" on:click={()=> {goTo(1)}}>Videos</div>
			<div class="slide-link" on:click={()=> {goTo(2)}}>About</div>
			<div class="slide-link" on:click={()=> {goTo(3)}}>Services</div>
			<div class="slide-link" on:click={()=> {goTo(4)}}>Contact</div>
			<iframe width="560" height="315" src="https://www.youtube.com/embed/E4Qyt10AZZo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      	</div>
	</SwiperSlide>
	<SwiperSlide>
		<div class="page">
			<div class="title">Page: About</div>
			<div class="slide-link" on:click={()=> {goTo(0)}}>Home</div>
			<div class="slide-link" on:click={()=> {goTo(1)}}>Videos</div>
			<div class="slide-link" on:click={()=> {goTo(2)}}>About</div>
			<div class="slide-link" on:click={()=> {goTo(3)}}>Services</div>
			<div class="slide-link" on:click={()=> {goTo(4)}}>Contact</div>
      	</div>
	</SwiperSlide>
	<SwiperSlide>
		<div class="page">
			<div class="title">Page: Services</div>
			<div class="slide-link" on:click={()=> {goTo(0)}}>Home</div>
			<div class="slide-link" on:click={()=> {goTo(1)}}>Videos</div>
			<div class="slide-link" on:click={()=> {goTo(2)}}>About</div>
			<div class="slide-link" on:click={()=> {goTo(3)}}>Services</div>
			<div class="slide-link" on:click={()=> {goTo(4)}}>Contact</div>
      	</div>
	</SwiperSlide>
	<SwiperSlide>
		<div class="page">
			<div class="title">Page: Contact</div>
			<div class="slide-link" on:click={()=> {goTo(0)}}>Home</div>
			<div class="slide-link" on:click={()=> {goTo(1)}}>Videos</div>
			<div class="slide-link" on:click={()=> {goTo(2)}}>About</div>
			<div class="slide-link" on:click={()=> {goTo(3)}}>Services</div>
			<div class="slide-link" on:click={()=> {goTo(4)}}>Contact</div>
      	</div>
	</SwiperSlide>

  </Swiper>
</main>

<style>
  main {
    text-align: center;
  }
  .page {
    height: 100vh;
	display: flex;
	flex-direction: column;
	align-items: center;
  }

  .title {
	  padding: 20px;
  }

  .slide-link {
	  padding: 10px;
	  background-color: #4D0013;
	  color: white;
	  width: 100px;
	  cursor: pointer;
  }

  .page-1 {
	  background-image: url("/images/1.jpg");
	  background-size: contain;
	  background-position: center;
	  background-repeat: no-repeat;
  }

  .page-2 {
	  background-image: url("/images/2.jpg");
	  background-size: contain;
	  background-position: center;
	  background-repeat: no-repeat;
  }

</style>
