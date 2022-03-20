</-- HTML CODE -->

<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Coming Soon</title>
  <link rel="stylesheet" type="text/css" href="style.css">
  <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
  <script src="custom.js"></script> 
</head>
<body>
  <span class="bar"><i class="fa fa-bars"></i></span>
  <nav class="toggle-nav">
    <ul class="listing">
      <li>
        <a href="https://www.facebook.com/stackfindover">
          <i class="fa fa-facebook"></i>
        </a>
      </li>
      <li>
        <a href="https://www.twitter.com/stackfindover">
          <i class="fa fa-twitter"></i>
        </a>
      </li>
      <li>
        <a href="https://www.instagram.com/stackfindover">
          <i class="fa fa-instagram"></i>
        </a>
      </li>
      <li>
        <a href="https://www.youtube.com/stackfindover">
          <i class="fa fa-youtube"></i>
        </a>
      </li>
      <li>
        <a href="mailto:stackfindover@gmail.com">
          <i class="fa fa-envelope"></i>
        </a>
      </li>
    </ul>
  </nav>
  <section class="coming-soon">
    <div class="coming-soon-inner">
      <h1 class="heading">Coming Soon</h1>
      <h2 class="small-heading">Under Construction</h2>
      <div class="counter-timer">
        <ul>
            <li><span id="days"></span>days</li>
            <li><span id="hours"></span>Hours</li>
            <li><span id="minutes"></span>Minutes</li>
            <li><span id="seconds"></span>Seconds</li>
          </ul>
        </div>
    </div>
  </section>
</body>
</html>


</-- CSS CODE  -->

* {
  margin: 0;
  padding: 0;
  font-family: 'Oswald', sans-serif; 
}
body {
    overflow: hidden;
}
.coming-soon {
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: #fece00;
    overflow: hidden;
}
.coming-soon-inner {
    position: relative;
}
.heading {
    font-size: 100px;
    text-transform: uppercase;
    padding: 20px;
    background: #000;
    color: #fece00;
    transform: skewY(-10deg);
    font-weight: 500;
    line-height: 100px;
}
.small-heading {
    font-size: 30px;
    text-transform: uppercase;
    display: inline-block;
    padding: 20px;
    background: #fff;
    color: #000;
    transform: skewY(-10deg);
    font-weight: 500;
    line-height: 30px;
    box-shadow: 10px 10px 20px rgb(0 0 0 / .3);
    position: absolute;
    right: 0;
    bottom: -44px;
}

ul {
    list-style: none;
    display: flex;
    column-gap: 10px;
}
.counter-timer {
    transform: skewY(-10deg);
    position: absolute;
    left: 0;
    bottom: -75px;
}
.counter-timer > ul > li > span {
    padding-right: 5px;
}



/*******************************/
span.bar {
    display: block;
    position: absolute;
    right: 10px;
    top: 10px;
    z-index: 999;
}
span.bar i {
    font-size: 35px;
    cursor: pointer;
}
nav.toggle-nav {
    position: fixed;
    right: -100px;
    background: #fff;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: 0.5s linear;
    z-index: 333;
}
nav.toggle-nav.active {
  right: 0px;
}
ul.listing, ul.listing > li {
    display: block;
}
ul.listing > li > a {
    font-size: 30px;
    color: #000;
    padding: 10px;
    display: block;
    text-align: center;
    transition: 0.5s linear;
}
ul.listing > li > a:hover{
    color: #fece00;
}


.coming-soon-inner:before {
    content: "";
    height: 2px;
    width: 60%;
    background: #000;
    position: absolute;
    top: -50px;
    right: 0;
    transform: skewY(-10deg);
}

.coming-soon-inner:after {
    content: "";
    height: 2px;
    width: 60%;
    background: #fff;
    position: absolute;
    bottom: -80px;
    right: 0;
    transform: skewY(-10deg);
}

.heading:before {
    content: "";
    height: 2px;
    width: 60%;
    background: #000;
    position: absolute;
    top: -50px;
    left: 0;
}

.heading:after {
    content: "";
    height: 2px;
    width: 60%;
    background: #fff;
    position: absolute;
    bottom: -120px;
    left: 0;
}


@media only screen and (max-width: 400px) and (min-width: 200px) {
  .heading {
      font-size: 30px;
        line-height: 40px;
      text-transform: uppercase;
      padding: 10px 20px;
  }
  .small-heading {
      font-size: 20px;
        padding: 10px;
        bottom: -49px;
  }
  .counter-timer li {
      font-size: 12px;
  }

  .coming-soon-inner:before {
    top: -20px;
  }
  .heading:before {
    top: -20px;
  }
  .heading:after {
    bottom: -100px;
  }

} 
@media only screen and (max-width: 767px) and (min-width: 401px) {
  .heading {
      font-size: 40px;
        line-height: 50px;
      text-transform: uppercase;
      padding: 10px 20px;
  }
  .small-heading {
      font-size: 25px;
        padding: 10px;
        bottom: -48px;
  }
  .counter-timer li {
      font-size: 15px;
  }
  .coming-soon-inner:before {
    top: -30px;
  }
  .heading:before {
    top: -30px;
  }
  .heading:after {
    bottom: -100px;
  }
}


</--JS CODE  -->

const second = 1000,
      minute = second * 60,
      hour = minute * 60,
      day = hour * 24;

let countDown = new Date('Sep 30, 2021 00:00:00').getTime(),
    x = setInterval(function() {    

    let now = new Date().getTime(),
        distance = countDown - now;

    document.getElementById('days').innerText = Math.floor(distance / (day)),
    document.getElementById('hours').innerText = Math.floor((distance % (day)) / (hour)),
    document.getElementById('minutes').innerText = Math.floor((distance % (hour)) / (minute)),
    document.getElementById('seconds').innerText = Math.floor((distance % (minute)) / second);
}, second)



$(document).ready(function(){
  jQuery(".bar").click(function(){
    jQuery(".toggle-nav").toggleClass("active");
    jQuery(this).toggleClass("active-toggle");
    var activetoggle = jQuery(".bar").hasClass("active-toggle");
    if(activetoggle === true) {
      jQuery(".bar i").removeClass("fa-bars");
      jQuery(".bar i").addClass("fa-close");
    }else {
      jQuery(".bar i").removeClass("fa-close");
      jQuery(".bar i").addClass("fa-bars");
    } 
  }); 
}); 

</-- COMPLETE THE CODE -->
