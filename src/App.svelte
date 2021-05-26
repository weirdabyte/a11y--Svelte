<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import About from "./routes/About.svelte";
  import Contact from "./routes/Contact.svelte";


  export let url = "";

</script>

<body>
 
  <div class="wrapper">

  <Router url="{url}">
    <section class="nav-section">
  <img class="logo" src="./img/logo.png" alt="logo">
    <nav class="nav">
      <ul>
        <li><Link to="/">Home</Link> </li>
        <li><Link to="About">About</Link> </li>
        <li><Link to="Contact">Contact</Link> </li>
    </ul>
    </nav>
  </section>
    <div>
      <Route path="About" component={About}/> 
      <Route path="Contact"component={Contact} /> 
      <Route path="/"> <Home /></Route>
    </div>
  </Router> 

<section class="footer">
  <div class="info">
  <h5>Kontakt Info:</h5>
  <p>Adress: Lorem Ipsum 99, 4567 Oslo</p>
  <p>Telefon nummer: 0708 - 42 ** *9.</p>
  <p>E-mail: loremipsum@testing.com</p>
  
  </div>
  <h6>All images are from: LogoMakr.com</h6>

  <div class="socialMedia">
    <h6>Follow us on:</h6>
    <Router>
      <a href="https://www.facebook.com/" target="_blank" rel="noopener noreferrer"> <img src="./img/facebook.png" alt="facebook" class="mediaImage"> </a>
      <a href="https://www.twitter.com/" target="_blank" rel="noopener noreferrer"> <img src="./img/twitter.png" alt="twitter" class="mediaImage" /> </a>
      <a href="https://www.instagram.com/" target="_blank" rel="noopener noreferrer"> <img src="./img/instagram.png" alt="instagram" class="mediaImage"> </a>
    </Router>
  </div>
</section>
</div>
</body>