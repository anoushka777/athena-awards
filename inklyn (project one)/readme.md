# inklyn | custom cnc pen plotter
> <em><b>project one</b> aka my first submission for #athena-awards (a part of hack club's athena initiative) :D </em><br>

designed and building a low-cost, fully 3d-printable, foldable, beginner-friendly cnc pen plotter for [#athena-awards](https://athena.hackclub.com/) that can be assembled/run without soldering, plots svg to g-code extracted from vector drawings and uses standard components while running on open-source grbl firmware 

## features
> <em> this project has me setting goals that are definitely very ... ambitious (to say the least). its very very likely that i will fall flat on my face but i do want to challenge myself this summer, pick up a lot of practical experience and make projects that are somewhat do-able (and workable) and i definitely feel like this might be something that could help me get there. oh i am fully aware that i’m in over my head but like... artistically (plus my mom didn't raise a quitter, she raised a caffeinated ball of delusional confidence) — gotta make it work bcs a girl’s gotta rep the hardware girlies in tech, can't let the boys hack all the fun (pls laugh i spent 5 mins coming up w that) !!! </em>
- compact, foldable and can be stored easily
- frame, arms, pulleys, carriage, and pen holder are all 3d-printed
- uses arduino uno + nema 17 steppers + cnc shield + a4988 drivers + sg90 servo
- plots svg to g-code extracted from vector drawings (using inkscape & gcodetools)
- pen lift (servo powered z-axis enables pen up/down control)
- beginner-friendly and can be assembled and run without any soldering

## documenting my progress
>**estimated time spent on build:** still a work in progress <br>
**what it includes:** cad in fusion, circuit diagram, trial prints, firmware setup, testing, troubleshooting and lots of prayers

### ⚝ day one - sketching <em>[ 23 may '25 | time spent: 2.5 hours ]</em> <br>
started with vague plotter goals: foldable, <220mm print envelope, paper clamp optional, servo for pen. browsed old builds and remixes for clues. sketched layout in a paper notebook. made a bounding box in fusion to represent folded state. arms must collapse inward like a laptop. began modeling a basic baseplate — mostly rectangles lol. found a 2d drawing of lmbuu dimensions & modeled a placeholder bearing block.

### ⚝ day two - rod + belt layout assumptions <em>[ 24 may '25 | time spent: 3 hours ]</em> <br>
decided to use gt2 belts + 8mm rods — cheapest and most documented. laid out y-rails first. assumed 215mm rod length for y, 160mm for x. set center spacing to 45mm (just enough to let a carriage ride with stability). made up a belt path that might work. assumed a ~100mm x-carriage with a backplate to tie both rods together. used belt tensioner models from thingiverse into the timeline 


### ⚝ day three - x-arm folding geometry <em>[ 25 may '25 | time spent: 3 hours ]</em> <br>
main challenge: hinge that lets the x-axis arm rotate down for flat storage. modeled a simple 2-part hinge with a 3mm shaft hole, spacing set based on arm thickness (assumed 10mm print walls). real struggle: ensuring the hinge clears the y-rails when folded. had to reposition origin point and offset arm by 15mm vertically. added a "stop block" feature to avoid over-rotation. fusion refused to apply motion limits and i had to scream into my pillow to remain sane.

