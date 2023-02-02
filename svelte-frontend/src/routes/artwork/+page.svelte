<!-- this page will have my art work on it -->
<!-- process is not defined -->
<script>
    import NavBar from "../../components/NavBar.svelte";
    import { onMount } from "svelte"
    // import Jimp from 'jimp';
    import banshee from "../../images/banshee.png"
    
    let thumbnailWidth = 200;
    let thumbnailHeight= 200;


    let optimizedImage = "";

    // onMount(async () => {
    // const image = await Jimp.read(banshee);
    // await image.resize(300, Jimp.AUTO);
    // const data = await image.getBufferAsync(Jimp.MIME_JPEG);
    // optimizedImage = `data:image/jpeg;base64,${data.toString('base64')}`;
    // });

    // onMount(async () => {
    //   const image = await Jimp.read(banshee);
    //   await image.resize(300, Jimp.AUTO);
    //   const buffer = await image.getBufferAsync(Jimp.MIME_JPEG);
    //   const data = buffer.toString('base64');
    //   optimizedImage = `data:image/jpeg;base64,${data}`;
// });

</script>

<style>
  h1 {
    font-family: Arial, Helvetica, sans-serif;
  }
</style>

<h1 >generative art</h1>
<NavBar/>

<img src={banshee} alt=""
  loading="lazy"
  decoding="async"
  width={thumbnailWidth}
  height={thumbnailHeight}
/>




