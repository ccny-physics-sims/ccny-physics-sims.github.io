---
title: wavelength to RGB
refno: colors.8
width: 380
height: 200
---

<script>
// convert wavelength to RGB value
// based on http://www.efg2.com/Lab/ScienceAndEngineering/Spectra.htm

function setup() {
  createCanvas(380, 200);
  thecolor = getRGB(540);
  background(0);
  lambdaStart = 370;
  lambdaEnd = 750;
  for (i = lambdaStart;i<lambdaEnd;i++) {
    stroke(getRGB(i))
    line(0+i-lambdaStart,0,0+i-lambdaStart,height)
  }
  lambdaValue = createP('Wavelength = ')
  lambdaValue.position(width/2,height/2)
}

function draw() {
	lambdaValue.html('Wavelength = '+(mouseX+lambdaStart))
}


function getRGB(Wavelength) {

    if (Wavelength >= 380 && Wavelength<440)
    	{
        Red = -(Wavelength - 440) / (440 - 380);
        Green = 0.0;
        Blue = 1.0;
    	}
  		else if (Wavelength >= 440 && Wavelength<490)
      {
        Red = 0.0;
        Green = (Wavelength - 440) / (490 - 440);
        Blue = 1.0;
    	}
  		else if (Wavelength >= 490 && Wavelength<510)
      {
        Red = 0.0;
        Green = 1.0;
        Blue = -(Wavelength - 510) / (510 - 490);
  	  }
  		else if (Wavelength >= 510 && Wavelength<580)
      {
        Red = (Wavelength - 510) / (580 - 510);
        Green = 1.0;
        Blue = 0.0;
  	  }
  		else if(Wavelength >= 580 && Wavelength<645)
      {

        Red = 1.0;
        Green = -(Wavelength - 645) / (645 - 580);
        Blue = 0.0;
    	}
  		else if (Wavelength >= 645 && Wavelength<781)
      {
        Red = 1.0;
        Green = 0.0;
        Blue = 0.0;
    	}
  		else{

        Red = 0.0;
        Green = 0.0;
        Blue = 0.0;
    	};

    // Let the intensity fall off near the vision limits

    if((Wavelength >= 380) && (Wavelength<420)){
        factor = 0.3 + 0.7*(Wavelength - 380) / (420 - 380);
    }else if((Wavelength >= 420) && (Wavelength<701)){
        factor = 1.0;
    }else if((Wavelength >= 701) && (Wavelength<781)){
        factor = 0.3 + 0.7*(780 - Wavelength) / (780 - 700);
    }else{
        factor = 0.0;
    };
  return c = color(Red*255*factor,Green*255*factor,Blue*255*factor)
}</script>
