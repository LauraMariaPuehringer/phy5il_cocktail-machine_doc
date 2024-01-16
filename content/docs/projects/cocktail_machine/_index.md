---
title: Cocktail Machine
type: docs
---

# Liquid Rhythm Station 🎚 🎵
## Chindogu Cocktail Machine
# 🍹 🍋 🌴 

## Abstract

The __Liquid Rhythm Station__ is a mobile Cocktail Machine. It can mix cocktails with a maximum of three ingredients on the go 💨<br>  
{{< video src="first_try.gif" autoplay="true" loop="true" muted="true" >}}

## Introduction

*A detailed description of the concept and sketches of the planned implementation.*

*If a section grows too large or handles a very specific part of the project it can be put into [subpages]({{< ref "roboexotica" >}}).*

The main concept was, to build a carriable cocktail machine with interaction🍹 

Some use cases could be a (home)party, a festival, a concert and many more situtations, where alcohol is going to be consumed... 🍸

### Chindogu
To make it more *chindogu*, the radius of carrying around should have been limited to the length of an extension cable.🔌Furthermore the weight was also a factor for making it *chindogu*-like.

### Interaction
At the beginning the interaction was planned to happen through a button that needs to be pushed for pouring out liquid. The longer the buttons get pushed, the more liquid comes out. The problem was, that the ratio of different liquids couldn't have been controlled, so the team decided to choose sliders instead of a button -- one slider per bottle. With that the idea of creating something similar to a DJ mixing desk was born! 🪩

### Pouring out liquids
The first idea was to pour out the liquids by using a pulley, which raises the bottles.
But later the project team decided to use pumps instead of a pulley 🤓

### Making it fancy
The project team has noticed, that the prototype strongly relies on the presentation and look. So the plan was to fix some RGB LED's at the crate. The team also had the idea to give some auditory feedback... 


## Related work 

*References to related concepts, projects, books, websites, stories, systems, fruits, etc. and their relation to the project at hand.*

- The in german so called *Bauchladen* was the reference for making a __mobile__ cocktail machine.
{{< figure src="ref_bauchladen.jpg" alt="A Man is carriyng a BBQ station in front of his chest.">}}
- The __three sliders__ for controlling the liquid outflow should remind on a DJ mixing desk. 🎚🎚🎚
{{< figure src="mixpult.jpg" alt="a DJ mixing desk.">}}
- The liquids are getting pumped out with the concept of a [peristaltic pump](https://www.albinpump.com/de-at/news/how-peristaltic-pumps-work) and hoses. With the hoses some fancy stuff should happen (loops etc.).
{{< figure src="pumpe.jpg" alt="a cocktail machine using pumps">}}


## Implementation 

*A detailed description of your prototyping process.*

### Iteration №1 -- Pulley

The first idea was to pour out the liquids by using a pulley and lifting the bottles.
This idea has been discarded because of the weight of bottles. Also the possible splashing when pouring out the liquids has been considered 💦

{{< figure src="pulley.JPG" alt="a cocktail machine using pumps">}}
{{< video src="first_prototype.gif" autoplay="true" loop="true" muted="true" >}}

### Iteration №2 -- Peristaltic Pump

On the second try the concept of [peristaltic](https://www.albinpump.com/de-at/news/how-peristaltic-pumps-work) has been used for pouring out liquid. Using peristaltic pumps had the follwing advantages:
- no splashing of liquids -- the hoses are 100% dense! 💦
- less need of space because of the small size of the pumps (6L x 4W x 4H centimetres) 🤏🏻
- looks more fancy because of the transparent hoses ✨
- not such a powerful engine is needed 🏍
- the fixation of the bottles is much easier 😵‍💫🍾

#### Electronical components, that were used:
- 3 [Peristaltic Pumps, DC 12 V Mini Peristaltic Pump](https://www.amazon.de/dp/B087NSVDFY?ref_=cm_sw_r_apan_dp_BB6S1T8NNNB911D0TY39&language=en-GB&th=1)
- 3 meters [Silicone hose](https://www.amazon.de/Silikonschlauch-Meterware-Industriequalit%C3%A4t-Schlauch-Transparent/dp/B08CQ3JBP7/ref=asc_df_B08CRYGLF4/?tag=googshopde-21&linkCode=df0&hvadid=479990169759&hvpos=&hvnetw=g&hvrand=14415734970619313292&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=1030894&hvtargid=pla-1031347789108&mcid=d5dd0a2dc1f23213b9314ab19e4c39b7&th=1)
- 1 Toggle Switch
- 3 Sliders with linear resistance
- [RGB LED Stip](https://www.amazon.de/Streifen-Individuell-Adressierbar-DIY-Design-Heimdekoration/dp/B0BTVBTHQ5/ref=sr_1_5?keywords=Ws2812b%2BLed%2BStrip&qid=1701095616&sr=8-5&th=1)

{{< video src="pumpe2.mp4" autoplay="true" loop="true" muted="true" >}}

#### Electronical construction ⚡

The process was:
1. testing the power/strength of the peristaltic pumps
2. testing the resistance of the sliders
3. measured the pins on the sliders
4. tested analog output on the arduino board
5. measured the mosfet in/outputs and tested them with LED's
6. prototyping the electrical circuit with one pump
7. construction of the layout with 3 circuits

{{< figure src="aufbau.jpg" alt="a scribble of a arduino board">}}

#### Physical construction 🛠

To bring the idea of a mobile cocktail machine into a good physical shape, the project team decided to use a *beer crate* and modify it. The main reason for choosing a beer crate was the little weight 💪🏻

A plywood plate was fixed on top of the crate. It was used to fix the three sliders, the on/off toggle and the three pumps on top of it. The electronical components have been placed underneath the plate, for beauty reasons.

Inside the crate -- underneath the upper plywood plate -- some space for three bottles has been kept free. A second plywood plate has been used to stabilize the bottles and to create a bracket for the mugs.

{{< figure src="physical_construction.jpg" alt="a beer crate modified to a *Bauchladen*" caption="The physical construction 👆🏻">}}

{{< figure src="elektronik.jpg" alt="plywood plate with electronical components" caption="The electronic underneath the upper plate 👆🏻">}}

For making the crate *wearable*, a strap has been wrapped around the crate. The carrier has to put on the strap like a *back belt*.

{{< figure src="lukas.jpg" alt="a man who is carriyng a crate" caption="Lukas the carrier 👆🏻">}}

## Conclusion

*A reflection on your prototyping process and the project outcome. What happens to the prototype after the project?*

After finishing the project, the project team travelled to Vienna and visited the [Roböxotica 2023 Festival]({{< ref "roboexotica" >}}). It was a great way to connect to other __makers!__ The team gained a lot of valuable feedback and inspiration! For example that it is a wellknown issue to pump __liquids inlcuding carbonic acid__ through hoses.

Some __changes__ that the project team would do after finishing the prototype are...

... to simplify the process of changing the bottles e.g. by using adapters for the hoses 🍾

... to NOT use liquids with carbonic acid 🫧

... to make more fancy stuff with the hoses! 🪄

... to let the LED's give optical feedback about the amount of liquid that is poured out 🚥


The __prototyping process__ itself was very straighforward. The first idea has been discarded in a very early state so there was enough time to focus on the second one, which has lead -- with a bit of luck -- to a very good result! 🙌🏻