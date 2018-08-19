<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Fung Yeung personal website</title>
  <link href='https://fonts.googleapis.com/css?family=Inconsolata' rel='stylesheet' type='text/css'>
  <link href="https://fonts.googleapis.com/css?family=Germania+One" rel="stylesheet">
  <!-- icon -->
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.1.0/css/all.css" integrity="sha384-lKuwvrZot6UHsBSfcMvOkWwlCMgc0TaWr+30HWe3a4ltaBwTZhyTEggF5tJv8tbt" crossorigin="anonymous">
  <script src="https://d3js.org/d3.v5.min.js"></script>
</head>

<style>

  /* webpage background color */
  body {background: linear-gradient(45deg,rgb(45, 103, 230), rgb(255, 255, 255))}

/* nav bar*/
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
    padding:20px;
    display: inline-block;
    color:white;
    transition:all 0.2s;
    text-transform: uppercase;
  }

 /* Name section */
 #name {font-family: 'Germania One', cursive;
           font-size: 50px;
           color:#111;}

/* Type writer effect */
.typewrite { color:rgb(5, 59, 17);
            text-decoration: none;
            }

/* About me section */
#intro {
        padding: 30px;
        display:inline; 
        }
 
/* Skills section*/
#container {
    display: flex;
    flex-flow: row nowrap;
    justify-content: space-around;
}

#container ul {
    max-width: 50%;
    width: 15%;
    float:left;
    /* list-style-type: none;   */
}

#container ul li {
    display: table-cell;
    /* height: 100px; */
    list-style-type: none;
    margin: 10px;
    vertical-align: middle;
}

#container ul li i {
    font-size:30px;
}

#container ul li i.fa-star {
    font-size:13px;
}

#aboutMe {
  width: 70%
}

#intro, #aboutMe, #skills {
  padding-left: 1%
}
#contact {position: relative;
            bottom: 10px;
            left: 20px;
         }

/* all d3 charts style*/
svg {
    display: block;
    margin: 0 auto;
    cursor: pointer; 
}

/* three column charts */
text.qtyLineText { 
                font-size: 11px;
                stroke: purple;
                stroke-width: 0.5px;
    }

    text.shadow {
        font-size: 11px;
        stroke:white;
        stroke-width:3px;
        opacity:0.8;
    }

    .yaxis path {display:none;}

    .path.zeroDashLine {
        opacity:1;
    }

    .underTableText {
        font-size:0.8em
    }

</style>
<body>
  <!-- nav bar -->  <!-- add jump to page transition-->
  <nav id="navbar">
      <ul>
        <li class="logo"><a href="#"><i class="fas fa-long-arrow-alt-up"></i></a></li>  
        <li><a href="#anchorAboutMe">About me</a></li>
        <li><a href="#">Skills</a></li>
        <li><a href="#">Previous works</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
  </nav>

  <!-- short Introduction add photo here -->
  <div id = "intro">
    <div id = "name">Fung Yeung</div>  
    <h2>
        <a href="" class="typewrite" data-period="2000" data-type='[ "Data Analyst", "Data visualization lover", "History geek", "Philomath"]'>
          <span class="wrap"></span>
        </a>
    </h2>
  </div>

  <div id ="aboutMe">
    <h3 id="anchorAboutMe">About Me</h3>
    <p> Hello I am Fung! I have passion in lot of fields in life. To name a few, I love data analytic, data visualization, reading, investing and sailing</p>
  </div>
  <br>
  <!-- Skills -->
    <!-- pending to add tooltips for icon and stars-->
   <h3 id="skills">Skills &nbsp;<i class="fas fa-info-circle" style="font-size:15px;" title="Hello"></i></h3> 
   <div id="container">

    <ul> 
     <h4>Data-related</h4>
     <li>
      <i class="fab fa-r-project" title="R Project"></i>&nbsp;&nbsp;&nbsp;R project&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="far fa-star"></i>
      <i class="far fa-star"></i>
      <i class="far fa-star"></i>
     </li>
     <br>
     <li><img src="https://qph.ec.quoracdn.net/main-qimg-91e9c9cb7b33fbe025b71b119fe9f753" title="Excel VBA" height="30" width="30">&nbsp;&nbsp;&nbsp;Excel VBA&nbsp;&nbsp;&nbsp;&nbsp;
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="far fa-star"></i>
     </li>
     <br>
     <li>&nbsp;<img src="https://www.wize-net.co.jp/develop/images/img_d3_main.png" title="D3.js" height="30" width="30">&nbsp;&nbsp;D3.js&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="far fa-star"></i>
      <i class="far fa-star"></i>
     </li>
    </ul>

    <ul> 
     <h4>Web Development</h4>
     <li><i class="fab fa-html5"  title="HTML5"></i>&nbsp;&nbsp;HTML5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="far fa-star"></i>
    </li> 
     <br>
     <li><i class="fab fa-css3-alt"  title="CSS3"></i>&nbsp;&nbsp;CSS3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="fas fa-star"></i>
      <i class="far fa-star"></i>
      <i class="far fa-star"></i>
    </li> 
     <br>
     <li><i class="fab fa-js"  title="Javascript"></i>&nbsp;&nbsp;Javascript&nbsp;&nbsp;&nbsp;&nbsp;
     <i class="fas fa-star"></i>
     <i class="fas fa-star"></i>
     <i class="fas fa-star"></i>
     <i class="far fa-star"></i>
     <i class="far fa-star"></i>
     </li> 
   </ul>

   <ul> 
    <h4>Others</h4>
    <li><i class="fab fa-python"  title="Python"></i>&nbsp;&nbsp;Python&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     <i class="fas fa-star"></i>
     <i class="far fa-star"></i>
     <i class="far fa-star"></i>
     <i class="far fa-star"></i>
     <i class="far fa-star"></i>
   </li> 
    <br>
    <li><img src="https://upload.wikimedia.org/wikipedia/en/2/24/Imacros.png" title="iMacros for Firefox" height="30" width="30">&nbsp;&nbsp;iMacros&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
     <i class="fas fa-star"></i>
     <i class="fas fa-star"></i>
     <i class="fas fa-star"></i>
     <i class="far fsa-star"></i>
     <i class="far fa-star"></i>
     </li> 
    </ul>
   </div>


<!-- previous works -->
<div>
  <br style="clear: both;">
  <br>
  <h3 >Previous Works</h2>
    <!-- D3.js example -->
    <p>In my current job I uses D3.js to show data in a interactive and dynamic way</p>
    <p>Here is a excel chart converted into HTML version. By doing so the it allows automation of generating chart on a regular basis. 
        Also it saves lot of time in terms of adjusting chart appearance</p>
        <div id="Top10_EU" data-title="Top 10 apparel countries export to the EU" data-qtyLineHeight=5  
        data-link="https://docs.google.com/spreadsheets/d/e/2PACX-1vShlPjGPJdg8HbQ5w_N5w6UnDjjNEOqqIEb5cDHI2reosL7hCU2q4Dl_IdfnyVaZR4dwdPBf2-1Rffo/pub?output=csv"></div>

    <p> This is a simple interactive chart, clicking it will sort the data base on value</p>
    <div id="chart" title="click to sort data"></div>

   
    <!-- 2. VBA example -->
    <!-- 3. imacro example (video) -->
</div>
  <!-- Contact Info -->
  <div id="contact">
      <i class="fas fa-map-marker-alt"></i> Hong Kong
      <i class="far fa-paper-plane"></i> yeung.kei.fung@gmail.com</a>
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
        css.innerHTML = ".typewrite > .wrap { border-right: 0.08em solid #fff}";
        document.body.appendChild(css);

    };

    //fix nav bar
    const nav = document.querySelector('#navbar');
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
    // const skillInfoButton = document.getElementById("skillInfo");
    // skillInfoButton.addEventListener("mouseover", ()=>{
    //   console.log("hello")
    // })

  
    // D3 example chart
//Width and height
function DrawD3Chart() {
	var w = 1080;
	var h = 300;
	
	var dataset = [ 5, 10, 13, 19, 21, 25, 22, 18, 15, 13,
					11, 12, 15, 20, 18, 17, 16, 18, 23, 25 ];
	var xScale = d3.scaleBand()
					.domain(d3.range(dataset.length))
					.rangeRound([0, w])
					.paddingInner(0.05);
	var yScale = d3.scaleLinear()
					.domain([0, d3.max(dataset)])
					.range([0, h]);
	
  
	//Create SVG element
	var svg = d3.select("#chart")
				.append("svg")
				.attr("width", w)
				.attr("height", h);
        console.log(svg)
        console.log("haha")
	//Create bars
	svg.selectAll("rect")
		.data(dataset)
		.enter()
		.append("rect")
		.attr("x", function(d, i) {
			return xScale(i);
		})
		.attr("y", function(d) {
			return h - yScale(d);
		})
		.attr("width", xScale.bandwidth())
		.attr("height", function(d) {
			return yScale(d);
		})
		.attr("fill", function(d) {
			return "rgb(0, 0, " + Math.round(d * 10) + ")";
		})
		.on("mouseover", function() {
			d3.select(this)
				.attr("fill", "orange");
		})
		.on("mouseout", function(d) {
			d3.select(this)
				.transition("restoreBarColor")
				.duration(250)
				.attr("fill", "rgb(0, 0, " + (d * 10) + ")");
		})
		.on("click", function() {
			sortBars();
			sortText();
		});
	//Create labels
	svg.selectAll("text")
		.data(dataset)
		.enter()
		.append("text")
		.text(function(d) {
			return d;
		})
		.attr("text-anchor", "middle")
		.attr("x", function(d, i) {
			return xScale(i) + xScale.bandwidth() / 2;
		})
		.attr("y", function(d) {
			return h - yScale(d) + 14;
		})
		.attr("font-family", "sans-serif")
		.attr("font-size", "11px")
		.attr("fill", "white");
	
	//Define sort function
	var sortOrder = false;

	var sortBars = function() {
		sortOrder = !sortOrder;
		svg.selectAll("rect")
			.sort(function(a, b) {						
			if (sortOrder){
				return d3.ascending(a,b);
				} else {
					return d3.descending(a, b);
				} 
			})
			.transition(sortBars)
			.delay(function(d, i) {
				return i * 50;
			})
			.duration(1000)
			.attr("x", function(d, i) {
				return xScale(i);
			});
	};		

	var sortText = () => {
		svg.selectAll("text")
			.sort( (a,b) => {
				if (sortOrder){
				return d3.ascending(a,b);
				} else {
					return d3.descending(a, b);
				} 
			})
			.transition()
			.delay(function(d, i) {
				return i * 50;
				})
			.duration(1000)
			.attr("x", (d,i) => { 
				return xScale(i) + xScale.bandwidth() / 2
			})
		};
}
DrawD3Chart()   

    function EUChart(tableType){
            var svg = d3.select('#'+tableType).append("svg").attr("width",1080).attr("height",250).attr("class",tableType),
			// var svg = d3.select("#chartcontainer").append("svg").attr("width",960).attr("height",150),
            margin = {top: 40, right: 40, bottom: 30, left: 40},
            width = +svg.attr("width") - margin.left - margin.right,
            height = +svg.attr("height") - margin.top - margin.bottom,
            g = svg.append("g").attr("transform", "translate(" + margin.left + "," + margin.top + ")"),
            title = svg.attr("title"),
            dataLink = d3.select('#'+tableType).attr("data-link"),
            chartTitle = d3.select('#'+tableType).attr("data-title"),
            qtyLineHeight = d3.select('#'+tableType).attr("data-qtyLineHeight");
            // dataLink = "https://s3-eu-central-1.amazonaws.com/dev03.h-oi/wp-content/uploads/sites/63/2018/07/EachTopProduct-num1.csv"
        
        //Formater for y axis and line
        var formatPercent = d3.format(".0%");
        //Formater for bar labels
        var siFormat = d3.format(".3s");
        var customTickFormat = function (d){
            return siFormat(d).replace("G", "B");
        };
        // this is for partner country / x axis
        var x0 = d3.scaleBand()
            .rangeRound([0, width])
            .paddingInner(0.1);
        //this is for two column for two quarter value
        var x1 = d3.scaleBand()
            // .padding(0.025);                      // this control the gap between rect

        //this is for value for y-axis
        var y0 = d3.scaleLinear()
            .rangeRound([height-10, 40]);               //-10 to set minimum height for rect label
        //this is for Qty% for y-axis
        var y1 = d3.scaleLinear()
            .rangeRound([height, 0]);

        var z = d3.scaleOrdinal()
        .range(["#1974fc", "#ff7028", "purple"]);


        
        //load data from csv
        d3.csv(dataLink).then((data) => {
        dataset = data
        //parse data from string to number
        dataset.forEach((d) => {
            d[dataset.columns[2]] = +d[dataset.columns[2]];
            d[dataset.columns[1]] = +d[dataset.columns[1]];
            d["Qty (100KG) c.p LY"] = +d["Qty (100KG) c.p LY"];
            Partner = d[dataset.columns[0]]
        })
        var keys = dataset.columns.slice(1,3); //Column this quarter value and last quarter value
        var legendKeys = dataset.columns.slice(1,4);
        x0.domain(dataset.map(function(d) {
          return d.Partner;  
        }));

        x1.domain(keys)
        .rangeRound([0, x0.bandwidth()]);

        y0.domain(
            [0, 
            d3.max(dataset, function(d) {                    //find the max value in all catergories and series
                return d3.max(keys, function(key) {  // find max value among top value of each series
                    return d[key];                   //find max value in each series
                    }); 
                })
            ]).nice();
        
        y1.domain(
            [
            d3.min(dataset, function(d) {
                return d["Qty (100KG) c.p LY"]*qtyLineHeight}),                   //* is the height control factor for line
            d3.max(dataset, function(d) {
                return d["Qty (100KG) c.p LY"]})
            ]
        );

        
        //Create rect
        g.append("g")
        .selectAll("g")
        .data(dataset)
        .enter()
        .append("g")
        .attr("transform", function(d) { 
            return "translate(" + x0(d.Partner) + ",0)"; 
            })
        .selectAll("rect")
        .data(function(d) { 
            return keys.map(function(key) { 
                return {key: key,
                        value: d[key]}; 
                }); 
            })
        .enter()
        .append("rect")
        .attr("x", function(d) { return x1(d.key); })
        .attr("y", function(d) { return y0(d.value); })
        .attr("width", x1.bandwidth())
        .attr("height", function(d) { return height - y0(d.value); })
        .attr("fill", function(d) { return z(d.key); })
        .on("mouseover", function(d) {
          d3.select(this).style("fill", d3.rgb(z(d.key)).darker(0.8));
         })
         .on("mouseout", function(d) {
          d3.select(this).style("fill", z(d.key));
          })
          ;

    // Create rect label
    g.append("g")
    .selectAll("g")
    .data(dataset)
    .enter()
    .append("g")
    .attr("transform", function(d) { 
          return "translate(" + x0(d.Partner) + ",-10)"; 
        })
    .selectAll("text")
    .data(function(d) { 
        return keys.map(function(key) { 
            return {key: key,
                    value: d[key]
                   }; 
            }); 
        })
    .enter()
    .append("text")
    .text(function(d) {
        return "$" + customTickFormat(d.value);
    })
    .attr("x", function(d) {
            return x1(d.key) + x1.bandwidth()/6 ;
    })
    .attr("y", function(d) {
        if (d.key === keys[0]) { return height+6} else {
            return y0(d.value) +5;}
    })
    .attr("font-family", "sans-serif")
    // .style("text-anchor", "left")
    .attr("font-size", "14px")
    .attr("fill", function(d) {
        if (d.key ===keys[0]) { return "white"} else {
            return "black" ;}
    });

    //Draw line
    var line = d3.line()
            .x(function(d) { return x0(d.Partner)+ x0.bandwidth()/2 })
            .y(function(d) { return y1(d["Qty (100KG) c.p LY"]); });

    var zeroline = d3.line()
            .x(function(d) { return x0(d.Partner)+ x0.bandwidth()/2 })
            .y(y1(0)); 

    g.append("path")
     .datum(dataset)
     .attr("class", "qtyLine")
     .attr("fill", "none")
      .attr("stroke", "purple")
      .attr("stroke-linejoin", "round")
      .attr("stroke-linecap", "round")
      .attr("stroke-opacity", "0.6")
      .attr("stroke-width", 1.5)
      .attr("d", line);

    g.append("g")
    .selectAll("text")
    .data(dataset)
    .enter()
    .append("text")
    .style("font-size", "16px")
    .attr("class", "shadow")
    .attr("x", function(d) {
        return x0(d.Partner) + x0.bandwidth()/2-10;
    })
    .attr("y", function(d) {
        return y1(d["Qty (100KG) c.p LY"]) -10 ;
    })
    .text(function(d) {
        return formatPercent(d["Qty (100KG) c.p LY"]);
    });

    g.append("g")
    .selectAll("text")
    .data(dataset)
    .enter()
    .append("text")
    .style("font-size", "16px")
    .attr("class", "qtyLineText")
    .attr("x", function(d) {
        return x0(d.Partner) + x0.bandwidth()/2-10;
    })
    .attr("y", function(d) {
        return y1(d["Qty (100KG) c.p LY"]) -10 ;
    })
    .text(function(d) {
        return formatPercent(d["Qty (100KG) c.p LY"]);
    });

    //Draw Zero dash line
    g.append("path")
     .datum(dataset)

     .attr("fill", "none")
      .attr("stroke", "black")
      .attr("stroke-linejoin", "round")
      .attr("stroke-linecap", "round")
      .attr("stroke-width", 1.5)
      .attr("stroke-dasharray", 3)
      .style("stroke-opacity", 0.2)
      .attr("d", zeroline);

    //add X-axis
    g.append("g")
      .attr("class", "axis")
      .attr("transform", "translate(0," + height + ")")
      .call(d3.axisBottom(x0)
              .tickSize(0)
              .tickPadding(10)
              );

    //add Y-axis
    g.append("g")
    .attr("class", "yaxis")
    .attr("transform", "translate(" + (width+10) + ",0 )")
    .call(
    d3.axisRight(y1)
        .tickFormat(formatPercent)
        .ticks(3)
        // .tickValues([-0.8,-0.4,0])
        .tickSize(0)
        .tickPadding(5));
    
    //Create Legend
    var legend = svg.append("g")
    .attr("font-family", "sans-serif")
    .attr("font-size", 10)
    .attr("text-anchor", "end")
    .selectAll("g")
    .data(legendKeys)
    .enter().append("g").attr("class", "legend")

     legend.append("rect")
      .attr("x", width -180)
      .attr("width", 19)
      .attr("height", 19)
      .attr("fill", z)
      .on("mouseover", function(d) {
        d3.select(this).style("fill", d3.rgb(z(d)).darker(0.8));
       })
      .on("mouseout", function(d) {
        d3.select(this).style("fill", z(d));
       });

     legend.append("text")
      .attr("x", width-158)
      .attr("y", 9)
      .attr("dy", "0.35em")
      .style("text-anchor", "start")
      .text(function(d) { return d; })
      .attr("font-size", "13px");

    var x_offset = 0;
    svg.selectAll(".legend")
       .attr("transform", function(d,i){
            var x_pos = d3.select(this).select("text").node().getComputedTextLength() + 30;  // tspace between each legend
            x_offset = x_offset + x_pos;
            return "translate(" + (x_offset - x_pos) + ", 0)"
        })

    //Add Chart title
    svg.append("text")
        .attr("class", "chartTitle")
        .attr("x", margin.left+5)             
        .attr("y", margin.top - 25)
        .attr("text-anchor", "left")  
        .style("font-size", "16px") 
        .text(chartTitle);
        // .text("Top 10 apparel countries export to the EU");
        });}

        EUChart("Top10_EU");
    </script>
  </body>
</html>
 
