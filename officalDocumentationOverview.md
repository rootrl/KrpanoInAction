# Offical documentation overview

### Tips

krpano uses simple xml text files for storing the settings for the krpano viewer. so you should respect the xml-syntax-rules;

### The krpano XML structure
    <krpano>
        <include>
        <preview>
        <image>
        <view>
        <autorotate>
        <plugin>
        <layer>
        <hotspot>
        <events>
        <action>
        <scene>
    </krpano>
    
    
any krpano viewer are build with this xml elements. so you should know what these xml elements means;

read [krpano xml reference][1]

### krpano Actions / Scripting Reference

> krpano has a small and simple dynamic scripting language. With it krpano can be customized in many ways. A command or function is called action in krpano. It's possible to use existing actions and also to define new ones. The scripting language is dynamic and basically untyped, only some predefined variables are typed, but that is normally not relevant because inside the scripts all type conversions will be done automatically.


This documentation is about global krpano variables and objects, about the actions calling syntax and about all pre-defined krpano actions / functions.

 - Documentation topics:
 - Global-Variables Reference
 - Actions / Functions Reference
 - Syntax and Usage
 - Expressions
 - Arrays

read detail:  [http://krpano.com/docu/actions/][2]

### krpano Plugin Interface
for more: [http://krpano.com/docu/plugininterface][3]


### javascript interface

#### Usage Example
Get the krpano HTML DOM Element:

    var krpano = document.getElementById("krpanoSWFObject");

Get and set a variable:

    var fov = Number( krpano.get("view.fov") );
    fov += 10.0;
    krpano.set("view.fov", fov);

Call a krpano action, e.g. to load an other pano.

    krpano.call("loadpano('pano2.xml',null,MERGE,BLEND(1));");


for more: [http://krpano.com/docu/js/][4]



  [1]: http://krpano.com/docu/xml/
  [2]: http://krpano.com/docu/actions/
  [3]: http://krpano.com/docu/plugininterface
  [4]: http://krpano.com/docu/js/