# Chart.js, Canvas
Responsive Charts
When it comes to change the chart size based on the window size, a major limitation is that the canvas render size (canvas.width and .height) can not be expressed with relative values, contrary to the display size (canvas.style.width and .height). Furthermore, these sizes are independent from each other and thus the canvas render size does not adjust automatically based on the display size, making the rendering inaccurate.

The following examples do not work:

<canvas height="40vh" width="80vw">: invalid values, the canvas doesn't resize (example)
<canvas style="height:40vh; width:80vw">: invalid behavior, the canvas is resized but becomes blurry (example)
Chart.js provides a few options to enable responsiveness and control the resize behavior of charts by detecting when the canvas display size changes and update the render size accordingly.

Configuration Options
Name	Type	Default	Description
responsive	Boolean	true	Resizes the chart canvas when its container does (important note...).
responsiveAnimationDuration	Number	0	Duration in milliseconds it takes to animate to new size after a resize event.
maintainAspectRatio	Boolean	true	Maintain the original canvas aspect ratio (width / height) when resizing.
onResize	Function	null	Called when a resize occurs. Gets passed two arguments: the chart instance and the new size.
Important Note
Detecting when the canvas size changes can not be done directly from the CANVAS element. Chart.js uses its parent container to update the canvas render and display sizes. However, this method requires the container to be relatively positioned and dedicated to the chart canvas only. Responsiveness can then be achieved by setting relative values for the container size (example):

<div class="chart-container" style="position: relative; height:40vh; width:80vw">
    <canvas id="chart"></canvas>
</div>
The chart can also be programmatically resized by modifying the container size:

chart.canvas.parentNode.style.height = '128px';
Printing Resizeable Charts
CSS media queries allow changing styles when printing a page. The CSS applied from these media queries may cause charts to need to resize. However, the resize won't happen automatically. To support resizing charts when printing, one needs to hook the onbeforeprint event and manually trigger resizing of each chart.

function beforePrintHandler () {
  for (var id in Chart.instances) {
    Chart.instances[id].resize()
  }
}
Chart.js
slack

#Installation
You can get the latest version of Chart.js from npm , the GitHub releases , or use a Chart.js CDN . Detailed installation instructions can be found on the installation page.

#Creating a Chart
It's easy to get started with Chart.js. All that's required is the script included in your page along with a single <canvas> node to render the chart.

In this example, we create a bar chart for a single dataset and render that in our page. You can see all the ways to use Chart.js in the usage documentation.

<canvas id="myChart" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById('myChart').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            y: {
                beginAtZero: true
            }
        }
    }
});
</script>
 
        Copied!
    
#Contributing
Before submitting an issue or a pull request to the project, please take a moment to look over the contributing guidelines first.

For support using Chart.js, please post questions with the chartjs tag on Stack Overflow .

#License
Chart.js is available under the MIT license .

Documentation is copyright © 2014-2021 Chart.js contributors.
 
  
  Responsive Charts
When it comes to changing the chart size based on the window size, a major limitation is that the canvas render size (canvas.width and .height) can not be expressed with relative values, contrary to the display size (canvas.style.width and .height). Furthermore, these sizes are independent from each other and thus the canvas render size does not adjust automatically based on the display size, making the rendering inaccurate.

The following examples do not work:

<canvas height="40vh" width="80vw">: invalid values, the canvas doesn't resize (example )
<canvas style="height:40vh; width:80vw">: invalid behavior, the canvas is resized but becomes blurry (example )
<canvas style="margin: 0 auto;">: invalid behavior, the canvas continually shrinks. Chart.js needs a dedicated container for each canvas and this styling should be applied there.
Chart.js provides a few options to enable responsiveness and control the resize behavior of charts by detecting when the canvas display size changes and update the render size accordingly.

#Configuration Options
Namespace: options

Name	Type	Default	Description
responsive	boolean	true	Resizes the chart canvas when its container does (important note...).
maintainAspectRatio	boolean	true	Maintain the original canvas aspect ratio (width / height) when resizing.
aspectRatio	number	2	Canvas aspect ratio (i.e. width / height, a value of 1 representing a square canvas). Note that this option is ignored if the height is explicitly defined either as attribute or via the style.
onResize	function	null	Called when a resize occurs. Gets passed two arguments: the chart instance and the new size.
resizeDelay	number	0	Delay the resize update by give amount of milliseconds. This can ease the resize process by debouncing update of the elements.
#Important Note
Detecting when the canvas size changes can not be done directly from the canvas element. Chart.js uses its parent container to update the canvas render and display sizes. However, this method requires the container to be relatively positioned and dedicated to the chart canvas only. Responsiveness can then be achieved by setting relative values for the container size (example ):

<div class="chart-container" style="position: relative; height:40vh; width:80vw">
    <canvas id="chart"></canvas>
</div>
 
        Copied!
    
The chart can also be programmatically resized by modifying the container size:

chart.canvas.parentNode.style.height = '128px';
chart.canvas.parentNode.style.width = '128px';
 
        Copied!
    
Note that in order for the above code to correctly resize the chart height, the maintainAspectRatio option must also be set to false.

#Printing Resizable Charts
CSS media queries allow changing styles when printing a page. The CSS applied from these media queries may cause charts to need to resize. However, the resize won't happen automatically. To support resizing charts when printing, you need to hook the onbeforeprint event and manually trigger resizing of each chart.

function beforePrintHandler () {
    for (var id in Chart.instances) {
        Chart.instances[id].resize();
    }
}
 
        Copied!
    
You may also find that, due to complexities in when the browser lays out the document for printing and when resize events are fired, Chart.js is unable to properly resize for the print layout. To work around this, you can pass an explicit size to .resize() then use an onafterprint event to restore the automatic size when done.

window.addEventListener('beforeprint', () => {
  myChart.resize(600, 600);
});
window.addEventListener('afterprint', () => {
  myChart.resize();
});
 
