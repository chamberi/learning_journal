# LJ Code 201 - Day 12

## Code Review
using while testing validation with ||, if numbers equal, re-roll, otherwise push latest number to array  
left.src = filepath  
Listener: imgContain.addEventListener('click', handleimgclici);  
if (event.target.id === 'left') {do stuff}  

## Chart.js // Canvas  
— Canvas:  
  
HTML:  
< canvas id="tutorial" width="150" height="150" >< /canvas >  
block element  
  
JS:  
var canvas = document.getElementById('tutorial’);  
var ctx = canvas.getContext('2d’);  
  
function draw() {  
      var canvas = document.getElementById("canvas”);  
      if (canvas.getContext) {  
        var ctx = canvas.getContext("2d”);  
  
        ctx.fillStyle = "rgb(200,0,0)”;  
        ctx.fillRect (10, 10, 50, 50);  
  
        ctx.fillStyle = "rgba(0, 0, 200, 0.5)”;  
        ctx.fillRect (30, 30, 50, 50);  
      }  
    }  
  
x |  
   |____    
    y  
- fillRect(x, y, width, height) <— draws filled rectangle  
- strokeRect(x, y, width, height) <— Draws a rectangular outline.  
- clearRect(x, y, width, height) <— Clears the specified rectangular area, making it fully transparent.  

- Drawing Shapes: https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes  
- Applying Styles: https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors  

Versioning:   
Major.Minor.Patch  
- Major (2.0 to 1.0)  - breaks former releases  
- Minor (1.0 to 1.1) - incremental change  
- Patch (1.0 to 1.0.1) - bug fix

var buyers = document.getElementByID(‘buyers’).herContext(‘2d’);
new Chart(buyers).Line(buyerData);

Chaining methods together via dot notation:  
  
HTML:  
< h1 id=“woo”>WOO</ h1>  
  
JS:  
document.getElementByID(‘woo’).addEventListener(‘click, function() { do something }  
  
## Libraries and Lab
  
var ctx = document.getElementById("myChart”);  
var myChart = new Chart(ctx, {  
    type: ‘bar’,  
    data: {  
        labels: ["Red", "Blue", "Yellow", "Green", "Purple", "Orange”],  
        datasets: [{  
            label: '# of Votes’,  
            data: [12, 19, 3, 5, 2, 3],  
            backgroundColor: [  
                'rgba(255, 99, 132, 0.2)’,  
                'rgba(54, 162, 235, 0.2)’,  
                'rgba(255, 206, 86, 0.2)’,  
                'rgba(75, 192, 192, 0.2)’,  
                'rgba(153, 102, 255, 0.2)’,  
                'rgba(255, 159, 64, 0.2)’  
            ],  
            borderColor: [  
                'rgba(255,99,132,1)’,  
                'rgba(54, 162, 235, 1)’,  
                'rgba(255, 206, 86, 1)’,  
                'rgba(75, 192, 192, 1)’,  
                'rgba(153, 102, 255, 1)’,  
                'rgba(255, 159, 64, 1)’  
            ],  
            borderWidth: 1  
        }]  
    },  
    options: {  
        scales: {  
            yAxes: [{  
                ticks: {  
                    beginAtZero:true  
                }  
            }]  
        }  
    }  
});  
</script>  
  
Use reset in HTML head file.  
< link rel=“stylesheet” href=“reset.css”>  
< link rel="stylesheet: href=“style.css”>  
< script src=“chart.js mini link”></script>  

