I've just converted some VRML files to X3D to display with X3DOM. They aren't showing up correctly, so I'm looking for some troubleshooting. Instead of typing up all the links and details, I've put up a tagged question here https://stackoverflow.com/questions/59920017/where-are-the-issues-in-this-conversion-from-vrml-to-x3d

Andreas Plesch @andreasplesch Jan 26 20:31
Hi Dave, the main issue is that the scenes use Protos which are not completely supported in x3dom. The good news is that the ProtoDeclarations here are effectively simple macros and probably work as x3dom inline in json format.

Andreas Plesch @andreasplesch Jan 26 21:38
https://gist.githack.com/andreasplesch/4fb27cb9f3db9ee423066ae74d4aaae1/raw/888eab5d133c1e3ff3a8e89b61bbd702995a41ce/t1.html has the scene as inline json.
https://gist.github.com/andreasplesch/4fb27cb9f3db9ee423066ae74d4aaae1 has the scene as vrml, x3d and json. The vrml was converted with view3dscene to x3d. view3dscene works better than the online instantreality converter. The x3d was then converted to json with http://xsltransform.net/ and the official stylesheet at https://sourceforge.net/p/x3d/code/HEAD/tree/www.web3d.org/x3d/stylesheets/X3dToJson.xslt

Andreas Plesch @andreasplesch Jan 26 21:44
Sorry, this is complicated but the json encoding is new and currently the only encoding which works with (simple) Protos in x3dom.

Andreas Plesch @andreasplesch Jan 26 23:10
There is an issue with the l, r, n, i protos . The x3dom expander does not deal with nested protos, it appears. You could define those protos without nesting, easiest in VRML and reconvert.

Andreas Plesch @andreasplesch Jan 27 00:39
https://gist.githack.com/andreasplesch/1709621326ec13282ea0204ca65c6301/raw/7c967403928a9fbdeb45eac0d1725951e26dbe88/t1mod.html has the modified protos. https://gist.github.com/andreasplesch/1709621326ec13282ea0204ca65c6301#file-t1mod-wrl is the modified vrml with the unnested l,r,n,i protos.

Andreas Plesch @andreasplesch Jan 27 01:35
For these macro type protos it is often possible to use DEF/USE instead which can be more concise. https://gist.githack.com/andreasplesch/1709621326ec13282ea0204ca65c6301/raw/4eea3a4fe4faae83e312c72a233521db99b1fbbe/t1defuse.html does that. No json is needed since there no protos in this x3d: https://gist.github.com/andreasplesch/1709621326ec13282ea0204ca65c6301#file-t1defuse-x3d