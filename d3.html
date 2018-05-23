
var svgWidth = 1000;
var svgHeight = 500;

var margin = {
  top: 20,
  right: 40,
  bottom: 60,
  left: 100
};

var width = svgWidth - margin.left - margin.right;
var height = svgHeight - margin.top - margin.bottom;

// Create an SVG wrapper, append an SVG group that will hold our chart, and shift the latter by left and top margins.
var svg = d3.select(".chart")
  .append("svg")
  .attr("width", svgWidth)
  .attr("height", svgHeight)

var chartGroup = svg.append("g")
  .attr("transform", `translate(${margin.left}, ${margin.top})`);

// Import Data
d3.csv("data/data.csv", function (err, doctorData) {
  if (err) throw err;

  // Step 1: Parse Data/Cast as numbers
   // ==============================
  doctorData.forEach(function (data) {
    data.income = +data.income;
    data.doctor = +data.doctor;
  });

  // Step 2: Create scale functions
  // ==============================
  var xLinearScale = d3.scaleLinear()
    .domain([25000, d3.max(doctorData, d => d.income)])
    .range([0, width]);

  var yLinearScale = d3.scaleLinear()
    .domain([0, d3.max(doctorData, d => d.doctor)])
    .range([height, 0]);

  // Step 3: Create axis functions
  // ==============================
  var bottomAxis = d3.axisBottom(xLinearScale);
  var leftAxis = d3.axisLeft(yLinearScale);

  // Step 4: Append Axes to the chart
  // ==============================
  chartGroup.append("g")
    .attr("transform", `translate(0, ${height})`)
    .call(bottomAxis);

  chartGroup.append("g")
    .call(leftAxis);


    var boxes = chartGroup.selectAll("g")
    .data(doctorData)
    .enter()
    .append("g")
    .attr("transform", function(d,i) {
        return "translate(" + (xLinearScale(d.income) - 10) +",0)";
    })    
   // Step 5: Create Circles
  // ==============================
  var circlesGroup = boxes
//   .selectAll("circle")
//   .data(doctorData)
//   .enter()
//   .append("g")
  .append("circle")
  //.attr("cx", d => xLinearScale(d.income))
  .attr("cy", d => yLinearScale(d.doctor))
  .attr("r", "15")
  .attr("fill", "pink")
  .attr("opacity", ".5")
  
  
  
  var labels = boxes
    //.data(doctorData)
    //.enter()
    .append("text")
    .attr("x", - 10)
    .attr("y", d => yLinearScale(d.doctor) + 5)
    .text(d => d.abbr)
    

  // Step 6: Initialize tool tip
  // ==============================
  var toolTip = d3.tip()
    .attr("class", "tooltip")
    .offset([10, -10])
    .html(function (d) {
      return (`${d.state}<br>Mean Income: $${d.income}<br><hr>Percentage affected: ${d.doctor}%`);
    });

  // Step 7: Create tooltip in the chart
  // ==============================
  chartGroup.call(toolTip);

  // Step 8: Create event listeners to display and hide the tooltip
  // ==============================
  circlesGroup.on("mouseover", function (data) {
      toolTip.show(data);
    })
    // onmousein event
    //.on("mousein", function (data, index) {
      //  toolTip.show(data);
    // onmouseout event
    .on("mouseout", function (data, index) {
      toolTip.hide(data);
    });

  // Create axes labels
  chartGroup.append("text")
    .attr("transform", "rotate(-90)")
    .attr("y", 0 - margin.left + 40)
    .attr("x", 0 - (height / 2))
    .attr("dy", "1em")
    .attr("class", "axisText")
    .text("Respondants Financially Unable to Visit A Doctor When Needed [%]");

  chartGroup.append("text")
    .attr("transform", `translate(${width/2}, ${height + margin.top + 30})`)
    .attr("class", "axisText")
    .text("Mean Income Per Household [$]");
});
