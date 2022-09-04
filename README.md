# OSMAnd Car
OSMAnd render.xml for car based navigation

based on default.render.xml from: https://github.com/osmandapp/OsmAnd-resources/tree/master/rendering_styles, but without direct dependency on it.

The map style is WIP and should incorporate all traffic related stuff. Only when zooming in, it shall show more, unrelated to driving, POIs.

## At the moment the changes from default.xml are as follows:
* Better icons for highway=speed_camera and enforcement="maxspeed" (still unsure if these are the best shields) <br>
 <br> ![radar night](https://user-images.githubusercontent.com/87526889/188315183-0303d8bd-b558-49a5-b6cb-080b3b81e102.png) ![radar day 2](https://user-images.githubusercontent.com/87526889/188315292-48f2ea3e-26e7-4de1-9e62-21d7a84987df.png) ![radar day one](https://user-images.githubusercontent.com/87526889/188315270-48bb5902-8393-41ba-99f5-3841a19e3d3a.png) 

* Lowest possible zoom level increased to 15 for the above (minimum to show radars)
* More highway shields <br>
<br> ![a](https://user-images.githubusercontent.com/87526889/188315368-9257e77b-443f-4bfd-8d23-3cca694aaaf7.png) ![b](https://user-images.githubusercontent.com/87526889/188315370-2ce26016-a1fc-46d3-b287-6b0d4695937b.png)
* Hide small village names on lower zoom
* Hide some non driving related POIs at low zoom
* Minimal performance increase for OSMAns's old-school rendering algo (a bit less details to render)

<br>

## Aim for the future:
* Improve rendering speed, by finishing the cleanup of Car.render.xml (as it is derrived from default.render.xml), because it's code is a mess and hugely uncommented with a lot of branches
* Route line is displayed in solid color over every POI or traffic sign (OSMAnd issue, fixed in 4.3) <br>
  It could alternatively be translucent and dotted, but this also does not work. A bug report has been filed.
* Display only device node of the enforcement relation (I do not know any way to distinguish relation members based on their role=*)
  
<br>

## How to install:
* Download the [Car.render.xml](https://github.com/chereskata/osmandcar/raw/main/Car.render.xml) and open it with OSMAnd
