+++
showonlyimage = false
draft = false
image = "img/portfolio/reno_rome.png"
date = "2025-01-16T01:00:00+00:00"
title = "(Reno - Rome)/2"
weight = 0
+++

### Sleep Book

Not as common now, but I read the "Sleep Book" by Dr. Seuss. On one page there is a line about a machine that listens and looks into everyone's home. It's supposed to be on a mountain halfway between Reno and Rome. I was kind of curious if this place actually exists. The midpoint for the short way and the long way are both in the ocean, but there are other cities named Reno and Rome, not just the ones in Nevada and Italy.

<iframe src="/midpoints_map.html" style="width: 100%; height: 500px; border: none;"></iframe>

You can also view as a [full-screen map](/midpoints_map.html).

### Elevation

So which midpoint is closest to being on a mountain? I queried an elevation API for all 70 midpoints (35 city pairs with 2 routes each).

<table>
  <thead>
    <tr>
      <th>Rank</th>
      <th>Reno</th>
      <th>Rome</th>
      <th>Elevation</th>
      <th>Location</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>1</td><td>Nevada</td><td>Wisconsin</td><td>5,200 ft</td><td>Eastern Wyoming</td></tr>
    <tr><td>2</td><td>Nevada</td><td>Georgia</td><td>3,694 ft</td><td>Western Kansas</td></tr>
    <tr><td>3</td><td>Nevada</td><td>Ohio</td><td>3,012 ft</td><td>Nebraska</td></tr>
    <tr><td>4</td><td>Ohio</td><td>Georgia</td><td>2,306 ft</td><td>Kentucky/Tennessee border</td></tr>
    <tr><td>5</td><td>Ohio</td><td>New York</td><td>1,972 ft</td><td>Northern Pennsylvania</td></tr>
  </tbody>
</table>

The winner is the midpoint between Reno, Nevada and Rome, Wisconsin at 5,200 feet in eastern Wyoming near Guernsey. 

### Nearest Peaks

Maybe it was referring to an actual mountain that was nearby though? I queried OpenStreetMap for the closest peaks to each midpoint:

<table>
  <thead>
    <tr>
      <th>Midpoint</th>
      <th>Nearest Peak</th>
      <th>Distance</th>
      <th>Peak Elevation</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Nevada ↔ Wisconsin</td><td>Squaw Rock</td><td>35 km</td><td>6,844 ft</td></tr>
    <tr><td>Nevada ↔ Georgia</td><td>Rock Hill</td><td>68.8 km</td><td>3,888 ft</td></tr>
    <tr><td>Nevada ↔ Ohio</td><td>Giant Hill</td><td>16.5 km</td><td>3,389 ft</td></tr>
    <tr><td>Ohio ↔ Georgia</td><td>Fox Knob</td><td>4.4 km</td><td>3,271 ft</td></tr>
    <tr><td>Ohio ↔ New York</td><td>Red Hill</td><td>2.5 km</td><td>1,640 ft</td></tr>
  </tbody>
</table>

The midpoint between Reno, Ohio and Rome, New York is only 2.5 km from Red Hill in northern Pennsylvania. For something more mountain-y, Fox Knob in the Appalachian foothills of Kentucky is just 4.4 km from the Reno, Ohio to Rome, Georgia midpoint. The Wyoming area near the highest midpoint has Squaw Rock (6,844 ft) about 35 km away — probably the most mountain-like candidate for the book.
