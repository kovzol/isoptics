# Experiments on isoptics by dynamic coloring

Please see http://www.nebrija.es/~pvelez/ACA2019/dana-picard.pdf for an overview.

This piece code uses [CindyJS](https://cindyjs.org) for visualizing and
[Giac](https://www-fourier.ujf-grenoble.fr/~parisse/giac.html) for computing some preliminary calculations.

# Usage

Start the file (isoptics.html) in your browser and enter one of the following functions:

* `x^2+2-y`
* `x^2-x*y+1`
* `1-x*y`

Then drag the point *C* and learn the isoptic angles *ACB* where *A* and *B* are tangent
points to the input curves. Angles above 90 degrees are colored with blue, above 90
degrees with red. Black points correspond to 90 degrees, therefore the orhoptic curve
of the given input will be shown as a black curve. White points have no meanings
to be selected for point *C*.

A black screen is shown if the formula cannot be interpreted correctly and therefore there 
is no way to completely calculate the initial equations in Giac.

A gray screen is shown if there is some internal error during the main computation
process inside CindyJS.

# Authors

* Thierry Dana-Picard <ndp@jct.ac.il>
* Zoltán Kovács <zoltan@geogebra.org>

# Acknowledgments

* Aaron Montag and the CindyJS Develoment Team for CindyJS and WebGL
* Bernard Parisse for Giac
* The GeoGebra Team for providing a JavaScript version of Giac

# Known bugs

* The software tool cannot decide if the input or its opposite function should be used.
* Some formulas give the wrong output, including the following ones:
  * `x^2+y^2-5`, `x^2+2*y^2-5` (circle, ellipse: the wrong tangent point is computed, a sign problem occurs)
* If there is no way to compute the roots symbolically, no numerical approach is forced.

# Technical details

This project currently uses http://dev.geogebra.org/maven2/fr/ujf-grenoble/giac-gwt/68505/.
