# GPS Unlocked — Find yourself
A browser-based interactive 2D model of GPS ranging and position estimation. Open index.html locally or deploy the four files at the root of a public GitHub Pages repository. No dependencies, external services, keys or sign-in.

## Explore
Add one, two, then three satellite signals; tap the diagram to move the simulated receiver; introduce a timing delay; reveal or hide the true position. In the deep dive, change receiver clock bias, toggle bias estimation, cluster satellites and introduce an extra signal delay.

## Mathematics
The simulator creates ranges from Euclidean distance and time offsets (c = 0.299792458 m/ns). The estimator receives satellite coordinates and ranges only. Two ranges are solved by circle intersection. Three or more ranges use damped iterative Gauss–Newton least squares, with multiple starting points. Clock bias is optionally an additional unknown in metres, converted to nanoseconds for display. The solver is approximate when measurements conflict. The diagram clips positions outside the visible grid. Negative corrected radii are clipped to zero for display.

## Limitations
This is a scaled flat 2D analogue, not a full 3D orbital GPS model. Real GPS generally needs four satellites for three coordinates and clock bias. The model excludes atmospheric delay, satellite motion and other corrections. Geometry effects depend on the particular noise and receiver position; there is no claim of guaranteed accuracy.

## Authorship
This revision was generated with ChatGPT assistance. The team should document its own contributions, changes, testing and AI use accurately according to the event fairness rules, and understand the code before submission.
