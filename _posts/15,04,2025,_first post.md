# Figure print assignemnt 

This assignment came with a large code base for identifing and clasifying figurprints based off their minutia deatils.
the fist step was to understand the code that was supplied.
after reading the code I have a decent idea on what it is doing,

A main part of the code is idenifing minutia, this is done through three steps:
1. skeletonization 
2. Detection of minutia positions 
3. estomation of minutia directions 
## skeletonization
skeletonization is the prosses of turning a gradent of pixles that form a line into a sigle pixle thick line. this is requried for minutia detection and works by expanding the gradent to be one colour this expanding every line,
each line is then thinned at its middle point.  
changing this:  
 ![fingerpint pre skeletonization](/images/lines.png)
to this ![fingerpint post skeletonization](/images/lines2.png)

## Detection of minutia positions
minutia is calssified through three methods, two lines converging, two lines splitting and a line ending.
The poresses is comlpeated by tracing allong each line and checking for one of these three situations. 
at each of these lacations a minutia point was placed.

## estomation of minutia directions 
The function will start at the outside of the fingerprint and trace along the ridge lines in a clacuated diection to each minutia, after reaching a minutia it logs the direction.
when it comes aponn a intersection or a speoration, the code would calculate three angles, the output/ input angle (based on if its divergance or convergance). for convergance the output angle is found by taking the mean of the two imput angles then compard with the points along the out put line to find the output angle.
for divergance the prosses is the same but in reverse.
![angle clacuation example](/images/anglecalc.png)

