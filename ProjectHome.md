## Links ##

Thanks to Klaumi Klingsporn for creating a debian package available here:
http://apt.klaumikli.de/testing

Installation instructions for 64 studio available here:
http://www.64studio.com/node/892

## LEET LADSPA Plugins v0.2 ##

So, you want to world-pwn3d the airwaves, do you?  \x/elcome to the platform.

Carefully crafted LADSPA plugins, reprogrammed from other plugins to have 2 inputs and 2 outputs especially for use with ardour.

Version 0.2:
  * Eq's were actually criss-crossing the lines a bit, this is fixed.
  * Further optimizations added... all plugins should be a bit faster.
  * Removed "special code" for P3 / PowerPC archictectures from modified TAP/SWH Ladspa code.
    * _Was causing unknown difficulties._
    * _takes more processing anyway, screw them_
  * Adjusted Chorus volume so it matches the volume without the Chorus
> > # Any saved sessions using v0.1  should have their volume #
> > # adjusted cuz of this Chorus change #
> > # (should be 3dB louder with version 0.2) #
  * Ardour version 2.5 automatically turns 1x1 plugins into 2x2s.. but these "true 2x2s" should still use less processor than ardour "doubling" the plugins.
  * Eq's don't process when gain is set between 0.01 dB to -0.01 dB now... this should help processing efficiency for the 8 band eq.

Version 0.1:

  * A 2x2 1 band Eq with Bandwidth settings (modified from TAP Plugins)
  * A 2x2 8 band Eq with Bandwidth settings (modified from TAP Plugins)
  * A 2x2 FULL STEREO Chorus (modified MCP Plugins)

NOTES:

Why only 3 plug-ins?  Well, I read on the ardour fora something like "So many ladpsa plugins, and all sux0rz!"  So, I thought, why cram up the maintenance and listings with experimentals and just release the elitest of them plugins programmed.

Ardour2 needs some good 2 input / 2 output plugins for general use.

The CAPS 2x2 Eq have something wrong with them, according to watching their output on Jamin when using them through ardour2.  Hence, I made these new ones.

The 8 band Eq (modified from TAP) uses a lot of processing, even though there is a check to see whether the dB for each band is 0 or not; which ought to make it "processing efficient", but such didn't seem to be the case.  I assume a rounding error until pr0v3n otherwise.  Hence the 1 band Eq.

I reprogrammed about 6 different LADSPA choruses and only put in the BEST chorus for this 2x2.  Full stereo 180 degree phase shift between the ears.

FOR THE FUTURE:
A 2x2 version of GVerb would be nice, as i think GVerb is probably the best existing LADSPA reverb.  However, GVerb's code is pretty complex so I haven't gotten far with that.

-> Apparently, this 2x2 gverb was already done by Fons Adriaensen, which I had just missed the installation of.  So, I recommend that one for 2x2 recordings.

BTW - I never check the damned email address for this "Google Code" - please contact me via email address inside source c0d3z
