# Twin.js
A JavaScript library to make things move.


How Can I Use it?
Find the easing functions here:
https://zoqol.github.io/twin/
You can use the method Twin.go(id,obj,props,duration,ease,onFinish,onUpdate,easeProps)
the arguments are :

            id       : a unique string for identifying tween.
            obj      : the object which you want to change it's properties.
            props    : properties of the object that you want to change.
            duration : time interval  
            ease     : the type of motion( you can choose it from above the page)
            onFinish : the function callback when motion ends.
            onUpdate : the function callback when the motion updates.

        
See the following example :
```javascript
Twin.init();
var el=document.getElementById('id1');
     Twin.go('id',{x:el.offsetLeft},{x:200},80,Easing.elastic.eOut,onFinished,function (e){
          el.style.left= e.obj.x+'px';
     })
Twin.getObject('id').pause();
```

