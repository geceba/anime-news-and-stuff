<script>
	import Footer from './components/Footer/Footer.svelte';
	import Social from './components/Social/Social.svelte';
	import Testimonial from './components/Testimonials/Testimonial.svelte';
	import About from './components/About/About.svelte';
	import Services from './Services/Services.svelte';
	import Banner from './components/Banner/Banner.svelte';
	import Navbar from './components/Navbar/Navbar.svelte';
	import DATA from './Data/data';
</script>


<Navbar navlists={DATA.NAVBAR_DATA} header={DATA.HEADER}/>

<Banner bannerData={DATA.BANNER_DATA} />

<Services serviceData={DATA.SERVICE_DATA} />

<About aboutData={DATA.ABOUT_DATA}/>

<Testimonial testimonialData={DATA.TESTIMONIAL_DATA} />

<Social socialData={DATA.SOCIAL_DATA} />

<Footer footerData={DATA.FOOTER_DATA} header={DATA.HEADER} /> 