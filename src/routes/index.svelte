<script>
  import Image from 'svelte-image';
  import Waypoint from 'svelte-waypoint';
  import Button from 'components/Button';
  import Checkbox from 'components/Checkbox';
  import Code from 'components/Code';
</script>

<h1>Svelte image</h1>

<p>Is a preprocessor which transforms image like this:</p>

<Code code={`<Image alt='fuji' src='fuji.jpg' />`} />

<p>into optimized lazy loaded image with
  <a href="https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images">srcset</a> like
</p>

<Code code={`
<img src="data:image/png;base64,/9j/2wBDAAYEBQYFBAYG...BwYIChAKCgkJChQODwwQF" alt="fuji">
<img alt="fuji" fit="cover" sizes="(max-width: 1000px) 100vw, 1000px" srcset="g/400-fuji.jpg 375w, g/800-fuji.jpg 768w, g/1200-fuji.jpg 1024w">`
} />

<Image alt='fuji' src='fuji.jpg' />
<Image alt='doggo' src='animals.jpg' />
<Image alt='painting 1' src='1.jpg' />
<Image alt='painting 2' src='2.jpg' />
<Image alt='painting 3' src='3.jpg' />
<Image alt='painting 4' src='4.png' />
<Image alt='painting 5' src='5.jpg' />
<Image alt='painting 6' src='6.jpg' />
<Image alt='painting 7' src='7.jpg' />
<Image alt='painting 8' src='8.jpg' />