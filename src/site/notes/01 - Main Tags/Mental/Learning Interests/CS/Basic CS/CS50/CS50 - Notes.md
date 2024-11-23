---
{"dg-publish":true,"permalink":"/01-main-tags/mental/learning-interests/cs/basic-cs/cs-50/cs-50-notes/","created":"2024-10-11T12:57:27.469+05:30","updated":"2024-10-12T00:49:29.000+05:30"}
---

<style> .container {font-family: sans-serif; text-align: center;} .button-wrapper button {z-index: 1;height: 40px; width: 100px; margin: 10px;padding: 5px;} .excalidraw .App-menu_top .buttonList { display: flex;} .excalidraw-wrapper { height: 800px; margin: 50px; position: relative;} :root[dir="ltr"] .excalidraw .layer-ui__wrapper .zen-mode-transition.App-menu_bottom--transition-left {transform: none;} </style><script src="https://cdn.jsdelivr.net/npm/react@17/umd/react.production.min.js"></script><script src="https://cdn.jsdelivr.net/npm/react-dom@17/umd/react-dom.production.min.js"></script><script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@excalidraw/excalidraw@0/dist/excalidraw.production.min.js"></script><div id="CS50_-_Notes_2024-10-12_0049.29.excalidraw.md1"></div><script>(function(){const InitialData={"type":"excalidraw","version":2,"source":"https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.5.1","elements":[],"appState":{"gridSize":null,"viewBackgroundColor":"#ffffff"}};InitialData.scrollToContent=true;App=()=>{const e=React.useRef(null),t=React.useRef(null),[n,i]=React.useState({width:void 0,height:void 0});return React.useEffect(()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height});const e=()=>{i({width:t.current.getBoundingClientRect().width,height:t.current.getBoundingClientRect().height})};return window.addEventListener("resize",e),()=>window.removeEventListener("resize",e)},[t]),React.createElement(React.Fragment,null,React.createElement("div",{className:"excalidraw-wrapper",ref:t},React.createElement(ExcalidrawLib.Excalidraw,{ref:e,width:n.width,height:n.height,initialData:InitialData,viewModeEnabled:!0,zenModeEnabled:!0,gridModeEnabled:!1})))},excalidrawWrapper=document.getElementById("CS50_-_Notes_2024-10-12_0049.29.excalidraw.md1");ReactDOM.render(React.createElement(App),excalidrawWrapper);})();</script>[[01 - Main Tags/Mental/Learning Interests/CS/Basic CS/CS50/CS50\|CS50]]

A computer is physically built on transistors, a bunch of tiny little switches. By turning these on and off, a computer can count from 0 to 1 and higher.

Perhaps a given transistor, in an ''off'' position, represents 0, whereas in an ''on'' position, it represents a 1.
Now to count higher, we'll use even more transistors, and the pattern in which these transistors have electricity flowing through them "on" or not flowing through them "off" can be used to perform ever more complicated tasks in binary language (just zeros and ones). It uses this pattern system, because it is far more sophisticated and efficient than the unary system (say, 1 transistor in the ''on'' position being 1, a second transistor in the ''on'' position being 2, and so on.) Each of these transistors (on (1) or off (0) ) represents a BIT. Each binary digit is represent by a BIT.

Now, the way in which these combinations represent different numbers follows a pattern.

In the decimal system, since all numbers are counted in multiples of ten, using 10 digits (0,1,2,3,4,5,6,7,8,9) we used a positioning system with the ''ones place'', the ''tens place'', the ''hundreds place'' and so on. What are each of these? Clearly, each of these ''places'' are simply powers of 10.

![Pasted image 20241010235649.png](/img/user/07%20-%20Media/Pasted%20image%2020241010235649.png)

In the binary system, since we count in multiples of two digits (the two digits being 0,1). Thus, we can simply  replace the bases in the above scenario with 2 instead of 10.

![Pasted image 20241010235712.png](/img/user/07%20-%20Media/Pasted%20image%2020241010235712.png)


So any digit in the 1s place represents a multiple of 1, in the middle place is that multiple of 2, and in the third place is that multiple of 4.

Thus, any three digit binary number of the form xyz = 4x + 2y + z, where x, y, and z can ONLY BE 1/0 and each of these x,y,z… are a BIT.

Like this, this can be extrapolated to the left hand side to the 8th column, the 16th column, the 32nd column, the 64th column and so on. Generally, computers today at a bare minimum for even the simplest operations involve 8-9 bits (which is almost nothing because they have between 500 million and 2 BILLION transistors (bits) in them)

Now, all this number business makes computers seem like excellent tools for number crunching, but how do they do the other stuff? Generate images, text, etc.?, if at the end of the day, all they have are these switches (bits) (transistors).

Well, what we've done is we've universally agreed to code a number to a particular letter. We can have variations on these by assigning different numbers to different cases of these letters, and so on. For example, capital A has been standardised as the number 65, and capital B as the number 66, and so on.

So A would be 01000001

Notice the first one is in the 6th place (0,1,2,3,4..) so that would be 2^6 which is 64. The other 1 is in the 0th place, where 2^0 = 1. So 64+1 = 65 = A.

Now, this brings up a dilemma. How would you use the number 65, or 66 ordinarily, for purposes like math, if the computer instinctively assumes it to be the capital letter A, or B?

You, as a programmer, will in fact give the computer hints as to exactly what to interpret it as. This is done using ASCII (The American Standard Code for Information Interchange)

And this can be remembered by a nifty little ASCII chart as given below

![Pasted image 20241010235749.png](/img/user/07%20-%20Media/Pasted%20image%2020241010235749.png)


And pretty much all modern devices know this mapping by heart.

A Byte is 8 Bits.

With a byte, you can count until 256 (0 is included), so 256 symbols can be represented. However, there are a lot more than 256 things we need to be able to represent.

The newer standard used is Unicode, which is a superset of ASCII, and includes emojis and whatnot.

Similarly, RGB is used to produce images, where numbers are used to represent different values of R, G, and B to be assigned to a pixel, to produce a wholly new colour. You can thus come up with (in a Byte) 255 different values of R, G, and B to mix together to create any new colour you want, where each pixel thus uses a total of 24 bits, or 3 bytes. A video is similarly just a continuous change in the values of this R, G, and B, with a number of discrete change taking place a number of times per second, which is the frame rate.

Audio is a similar concept. Different frequencies/wavelengths of sound can be assigned different values, and the number of gradations in this is really just dependent on how many bits/bytes of processing power we choose to give it.