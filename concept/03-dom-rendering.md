## dom node tree

##### 1. #text node is added between the elements.
![download](https://github.com/eileenjang/dom-basic/assets/82510378/708336ed-1ef0-4b7c-95cc-e7cf0f4283c8)

```
<div id=top>123
  <h1 id=one>DOM</h1>
  <div id=two>
    <p>Node Tree</p>
  </div>
</div>
```

```
const el = document.getElementById("top");
log(`length: ${el.childNodes.length}`);
let line = 0;
for (let node of el.childNodes){
  log(++line + `${node.nodeName}, ${node.nodeType}`);
};
```

##### 1) returns 5, not 3
##### 2) #text 3, H1 1, #text 3, DIV 1, #text 3

##### Not to contain #text?

```
const top = document.getElementById("top");
const els = top.children;
log(`length: ${els.length}`);
for (let el of els){
  log(`${el.nodeName}, ${el.id}`);
};
```
