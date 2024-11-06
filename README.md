<link href="https://fonts.googleapis.com/css?family=VT323" rel="stylesheet">
<div style="font-family: 'VT323', monospace; font-size: 16px; color: #00ff00; background-color: #000000; padding: 20px; border-radius: 10px;">
<style>
  body {
      background: #383838;
      color: #00dd00;
      font-family: 'VT323', monospace;
      font-size: 1.4em;
      margin: 0;
      padding: 20px;
      overflow: hidden;
      position: relative;
  }
  .scanlines {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(rgba(0, 0, 0, 0.1) 50%, transparent 50%);
      background-size: 100% 3px;
      pointer-events: none;
      animation: flicker 1.5s infinite;
  }
  @keyframes flicker {
      0% { opacity: 0.95; }
      50% { opacity: 0.98; }
      100% { opacity: 0.95; }
  }
  @keyframes scroll {
      0% { height: 0 }
      100% { height: 100%; }
  }
  @keyframes blink {
      to { opacity: 0; }
  }
  h1, h2, h3 h4, h5, h6 { 
  font-weight: normal;
  margin: 0;
  text-transform: uppercase;
  }
  a {
    color: white;	
    text-decoration: none;	
  }
  a:hover {
    color: red;
  }
  p { 
    line-height: 100%;
    margin: 0; 
  }	
  span { animation: blink 1s infinite }
  ul {
    list-style: none;
  }
  ul a:before,
  p a:before {
    color: #00dd00;
    content: ' [ ';
  }
  ul a:after,
  p a:after {
    color: #00dd00;
    content: ' ] ';	
  }
  header.site {
    margin: 0 0 40px 0;
    text-transform: uppercase;
  }
  nav.site { 
    margin: 0 0 40px 0;
    width: 100%;
  }
  nav.site ul {
    padding: 0;
  }
  nav.site ul li {
    display: inline-block;
    padding: 0 10px;
    min-width: 250px;
    width: auto;
  }
  .overlay {
    height: 1px;
    position: absolute;
    top: 0;
    left: 0;
    width: 1px;
  }
  .overlay:before {
    background: linear-gradient(#101010 50%, rgba(16, 16, 16, 0.2) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.03), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.03));
    background-size: 100% 3px, 6px 100%;
    content: "";
    display: block;
    pointer-events: none;
    position: fixed;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
    z-index: 2;
  }	
  .overlay:after {
    animation: flicker 0.30s infinite;
    background: rgba(16, 16, 16, 0.2);
    content: "";
    display: block;
    pointer-events: none;
    position: fixed;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
    z-index: 2;
  }
  .col {
    float: left;
    padding: 0 20px;
  }
  .col.two { width: auto; }
  .wrapper {
    animation: scroll 5s 1;
    margin: 0;
    overflow: hidden;
    padding: 0;
  }
  .content { 
    animation: scroll 3s 1;
    overflow: hidden;
    padding: 40px; 
    position: relative;
    width: 95%;
  }
  #logo-v {
    display: block;
    height: auto;
    margin: 0 auto;
    width: 200px;
  }
  img.pip-hero {
    display: block;
    float: left;
    height: auto;
    margin: 5px 10px 5px 0;
    width: 120px;
  }
  form {}
  label {
    clear: left;
    display: block;
    float: left;
    margin-right: 10px;
    padding-top: 5px;
  }
  input[type=text],
  textarea {
    background: transparent;
    border: none;
    color: #00dd00;
    display: block;
    float: left;
    font-family: 'VT323', Courier;
    font-size: 1.2em;
    position: relative;
    width: 80%;
    z-index: 10
  }
  textarea {
    margin-bottom: 20px;
    overflow: auto;
    resize: none;
  }
  input[type=text]:focus,
  textarea:focus,
  input[type=submit]:focus,
  a.button:focus {
    outline: 0;
  }
  input[type=submit],
  a.button {
    background: transparent;
    border: 1px solid #00dd00;
    clear: both;
    color: #00dd00;
    cursor: hand;
    display: inline-block;
    font-family: 'VT323', Courier;
    font-size: 1em;
    margin-bottom: 20px;
    opacity: 0.25;
    padding: 10px 100px;
    position: relative;
    text-decoration: none;
    text-transform: uppercase;
    z-index: 10;
  }
  input[type=submit]:hover,
  a.button:hover {
    background: #00dd00;
    color: #383838;
    opacity: 0.8;
  }
  .expandingArea { position: relative }
  .scanline {
    animation: scroll 10s 5s infinite;
    background: -moz-linear-gradient(top,  rgba(0,221,0,0) 0%, rgba(0,221,0,1) 50%, rgba(0,221,0,0) 100%);
    background: -webkit-linear-gradient(top,  rgba(0,221,0,0) 0%,rgba(0,221,0,1) 50%,rgba(0,221,0,0) 100%);
    background: linear-gradient(to bottom,  rgba(0,221,0,0) 0%,rgba(0,221,0,1) 50%,rgba(0,221,0,0) 100%);
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#0000dd00', endColorstr='#0000dd00',GradientType=0 );
    display: block;
    height: 20px;
    opacity: 0.05;
    position: absolute;
      left: 0;
      right: 0;
      top: -5%;
    z-index: 2;
  }
  .clear {
    clear: both;
  }
  .clearfix {
    overflow: auto;
    zoom: 1;
  }
  .upper { text-transform: uppercase; }
</style>
<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
<script src="https://static.tumblr.com/maopbtg/oimmiw86r/jquery.autosize-min.js"></script>

<div class="overlay"></div>
<div class="scanline"></div>
<div class="wrapper">

# PROFILE OS™
---

### Hello there, I'm Dmitry 👋
*Almost 9 years exeprienced software developer.*
*Welcome to my SHELTER*

I'm a software developer!
- 🤖 Tryin' to create something significant in AI
- 👐 Open source addict
- ☕ Love the f**g coffee

- - -

[![💻 Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=dagrigorev&hide=c&theme=chartreuse-dark)](https://github.com/dagrigorev)

- - -

<img align="left" alt="dagrigorev's Github Stats" src="https://github-readme-stats.vercel.app/api?username=dagrigorev&show_icons=true&hide_border=true&theme=chartreuse-dark" />
<br />

- - -

## [ Contact Me ](mailto://dmitryandreevichgr@gmail.com)

- - -

### **Email >> _dmitryandreevichgr@gmail.com_**  
### **tg >> _@dagrigorev_**  

- - -

**v2.0.0**  
(C)2024 dagrigorev

</div>