<script>
  import { Navigation, Pagination, Scrollbar, A11y, Mousewheel } from "swiper";
  import { Swiper, SwiperSlide } from "swiper/svelte";
  import Home from "./pages/Home.svelte";
  import Videos from "./pages/Videos.svelte";

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
		<div class="page">
			<div class="padding">
				<Home goTo={goTo} />
			</div>	
      	</div>
	</SwiperSlide>
    <SwiperSlide>
		<div class="page">
			<div class="padding">
				<Videos goTo={goTo} />
			</div>	
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
	background-color: burlywood;

  }
  .page {
    height: 100vh;
  }

  .page .padding {
	  padding-left: 50px;
	  height: 100%;
  }

  
  @media only screen and (max-width: 600px) {
	  .page .padding {
		  padding-left: 30px;
	  }
  }

</style>
