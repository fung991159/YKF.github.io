<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Fung Yeung personal website</title>
  <link href='https://fonts.googleapis.com/css?family=Inconsolata' rel='stylesheet' type='text/css'>
  <link href="https://fonts.googleapis.com/css?family=Germania+One" rel="stylesheet">
  <!-- icon -->
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.1.0/css/all.css" integrity="sha384-lKuwvrZot6UHsBSfcMvOkWwlCMgc0TaWr+30HWe3a4ltaBwTZhyTEggF5tJv8tbt" crossorigin="anonymous">
</head>

<style>
  body {background: linear-gradient(45deg,rgb(45, 103, 230), rgb(255, 255, 255))}

  #contact {position: absolute;
            bottom: 10px;
            right: 100px;
            }
  
  ul {
  list-style-type: none;
  } 

  ul i {
    font-size:30px;
  }
  
  ul i.fa-star{
    font-size:1px;
  }

  /* ul i.info{
    font-size:30px;
  } */
  
  #name {font-family: 'Germania One', cursive;
           font-size: 50px;
           color:#111;}
  
  .intro {
          /* border: 10px dotted black; */
          padding: 30px;
          /* background: rgb(202, 199, 199); */
          /* background-clip: padding-box; */
          display:inline; 
          }
  
  .typewrite { color:rgb(5, 59, 17);
               text-decoration: none;
               }

  /* nav bar         */
  nav {
    background:black;
    top:0;
    width: 100%;
    transition:all 0.5s;
    position: relative;
    z-index: 1;
  }

  body.fixed-nav nav {
    position: fixed;
    box-shadow:0 5px 0 rgba(0,0,0,0.1);
  }

  nav ul {
    margin: 0;
    padding:0;
    list-style: none;
    display:flex;
  }

  nav li {
    flex:1;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  li.logo {
    max-width:0;
    overflow: hidden;
    background: white;
    transition: all 0.5s;
    font-weight: 600;
    font-size: 30px;
  }

  li.logo a {
    color:black;
  }

  .fixed-nav li.logo {
    max-width:500px;
  }

  nav a {
    text-decoration: none;
    padding:0px;
    display: inline-block;
    color:white;
    transition:all 0.2s;
    text-transform: uppercase;
  }

  .skills h5 {
    padding-bottom: 0px;
  }
  
  .skills h1 {
    display:inline-block;
    padding-top:0px;
    padding-left:5px;
  }
    
</style>
<body>
  <!-- nav bar -->  <!-- add jump to page transition-->
  <nav id="main">
      <ul>
        <li class="logo"><a href="#"><i class="fas fa-long-arrow-alt-up"></i></a></li>  
        <li><a href="#anchorAboutMe">About me</a></li>
        <li><a href="#">Skills</a></li>
        <li><a href="#">Previous works</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>

  <!-- short Introduction add photo here -->
  <div class = "intro">
    <div id = "name">Fung Yeung</div>  
    <h2>
        <a href="" class="typewrite" data-period="2000" data-type='[ "Data Analyst", "Data visualization lover", "History geek", "Philomath"]'>
          <span class="wrap"></span>
        </a>
    </h2>
  </div>

  <div class ="aboutMe">
    <h5 id="anchorAboutMe">About Me</h5>
    <p> Hello I am Fung! I have passion in lot of fields in life. To name a few, I love data analytic, data visualization, reading, investing and sailing</p>
  </div>

  
  <!-- Skills -->
  <div class = "skills">
   <h5>Skills &nbsp;<i id="skillInfo" class="fas fa-info-circle" style="font-size:15px;"></i></h5>
   <ul> 
     <h4>Data-related</h4>
     <li><i class="fab fa-r-project" title="R Project"></i>&nbsp;&nbsp;&nbsp;R project&nbsp;&nbsp;&nbsp;<i class="fas fa-star"></i><i class="fas fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i></i></li>
     <br>
     <li><img src="https://qph.ec.quoracdn.net/main-qimg-91e9c9cb7b33fbe025b71b119fe9f753" title="Excel VBA" height="30" width="30">&nbsp;&nbsp;&nbsp;&nbsp;Excel VBA&nbsp;<i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="far fa-star"></i></li>
     <br>
     <li>&nbsp;<img src="https://www.wize-net.co.jp/develop/images/img_d3_main.png" title="D3.js" height="30" width="30">&nbsp;&nbsp;D3.js&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="far fa-star"></i><i class="far fa-star"></i></li>
   </ul>
   <h1><i class="fab fa-html5"  title="HTML5"></i></h1>
   <h1><i class="fab fa-css3-alt" title="CSS3"></i></h1>
   <h1><i class="fab fa-js" title="Javascript"></i></h1>

   <h1><i class="fab fa-python" title="Python"></i></h1>
   
   <img src="https://upload.wikimedia.org/wikipedia/en/2/24/Imacros.png" title="Imacros for Firefox" height="30" width="30">

  </div>

<!-- previous works -->

  <!-- Contact Info -->
  <div id="contact">
      <i class="fas fa-map-marker-alt"></i> Hong Kong
      <i class="far fa-paper-plane"></i> yeung.kei.fung@gmail.com
  </div>

 
  <script>
  // typewriter effect
  var TxtType = function(el, toRotate, period) {
        this.toRotate = toRotate;
        this.el = el;
        this.loopNum = 0;
        this.period = parseInt(period, 10) || 2000;
        this.txt = '';
        this.tick();
        this.isDeleting = false;
    };

    TxtType.prototype.tick = function() {
        var i = this.loopNum % this.toRotate.length;
        var fullTxt = this.toRotate[i];

        if (this.isDeleting) {
        this.txt = fullTxt.substring(0, this.txt.length - 1);
        } else {
        this.txt = fullTxt.substring(0, this.txt.length + 1);
        }

        this.el.innerHTML = '<span class="wrap">'+this.txt+'</span>';

        var that = this;
        var delta = 80 - Math.random() * 100;  //typing speed control

        if (this.isDeleting) { delta /= 2; }

        if (!this.isDeleting && this.txt === fullTxt) {
        delta = this.period;
        this.isDeleting = true;
        } else if (this.isDeleting && this.txt === '') {
        this.isDeleting = false;
        this.loopNum++;
        delta = 500;
        }

        setTimeout(function() {
        that.tick();
        }, delta);
    };

    window.onload = function() {
        var elements = document.getElementsByClassName('typewrite');
        for (var i=0; i<elements.length; i++) {
            var toRotate = elements[i].getAttribute('data-type');
            var period = elements[i].getAttribute('data-period');
            if (toRotate) {
              new TxtType(elements[i], JSON.parse(toRotate), period);
            }
        }
        // INJECT CSS
        var css = document.createElement("style");
        css.type = "text/css";
        css.innerHTML = ".typewrite > .wrap { border-right: 0.1em solid #bbb}";   // typing dash
        document.body.appendChild(css);
    };
    
    //fix nav bar
    const nav = document.querySelector('#main');
    let topOfNav = nav.offsetTop;
    function fixNav() {
      if (window.scrollY >= topOfNav) {
        document.body.style.paddingTop = nav.offsetHeight + 'px';
        document.body.classList.add('fixed-nav');
      } else {
        document.body.classList.remove('fixed-nav');
        document.body.style.paddingTop = 0;
      }
    }
    window.addEventListener('scroll', fixNav);
    
    // Skills additional info

    const skillInfoButton = document.getElementById("skillInfo");
    skillInfoButton.addEventListener("mouseover", ()=>{
      console.log("hello")
    })
    </script>
</body>

 
