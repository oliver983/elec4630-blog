#Figure print assignemnt 

This assignment came with a large code base for identifing and clasifying figurprints based off their minutia deatils.
the fist step was to understand the code that was supplied.
after reading the code I have a decent idea on what it is doing,

A main part of the code is idenifing minutia, this is done through three steps:
1. skeletonization 
2. Detection of minutia positions 
3. estomation of minutia directions 
##skeletonization
skeletonization is the prosses of turning a gradent of pixles that form a line into a sigle pixle thick line. this is requried for minutia detection and works by expanding the gradent to be one colour this expanding every line,
each line is then thinned at its middle point.
changing this: /../main/assets/images/lines.png
to this /../main/assets/images/lines2.png

