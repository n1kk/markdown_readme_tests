<code>var Emitter=function(){function a(b){this._evt={};<br>
this._ctx=b||this}a.extend=function(b){return new a<br>
(b)};a.prototype.on=function(b,c){(this._evt[b]||(t<br>
his._evt[b]=[])).push(c);return this};a.prototype.o<br>
nce=function(b,c){return this.on(b,function d(){thi<br>
s.off(b,d);c.apply(this,arguments)})};a.prototype.o<br>
ff=function(b,c){if(0===arguments.length)this._evt=<br>
{};else if(1===arguments.length)delete this._evt[b]<br>
;else if(1===arguments.length){var a=this._evt[b],d<br>
=a?a.indexOf(c):-1;-1<d&&a.splice(d,1)}return this}<br>
; a.prototype.emit=function(b){var c=this._evt[b];i<br>
f(c&&0<c.length){c=c.slice();for(var a=c.length,d=1<br>
<arguments.length?Array.prototype.slice.call(argume<br>
nts,1):[],e=0;e<a;e++)c[e].apply(this._ctx,d)}retur<br>
n this};a.prototype.hasListeners=function(b,a){var <br>
c=this._evt[b];return c?1<arguments.length?-1<c.ind<br>
exOf(a):!0:!1};return a}();</code>

<pre><code>
</code></pre>


| `var Emitter=function(){function t(t){this._evt={},this._ctx=t||this}return t.extend=function(e){var n;return e&&"object"==typeof e&&(n=new t(e),["_evt","_ctx","on","off","once","emit","triggers"].forEach(function(t){e[t]=n[t]})),e},t.prototype.on=function(t,e){var n;return t&&e&&((n=this._evt[t])?(this.off(t,e),n.push(e)):n=[e],this._evt[t]=n),this},t.prototype.once=function(e,n){return n?this.on(e,function t(){this.off(e,t),n.apply(this,arguments)}):this},t.prototype.off=function(t,e){var n,i,o=arguments.length;return 0===o?this._evt={}:1===o?delete this._evt[t]:2===o&&-1<(n=(i=this._evt[t])?i.indexOf(e):-1)&&(i.splice(n,1),i.length||delete this._evt[t]),this},t.prototype.emit=function(t){var e,n,i=arguments,o=this._evt[t];if(o&&(n=o.length))for(o=o.slice(),i=1<i.length?[].slice.call(i,1):[],e=0;e<n;e++)o[e].apply(this._ctx,i);return this},t.prototype.triggers=function(t,e){var n;return t?!!(n=this._evt[t])&&(!(1<arguments.length)||-1<n.indexOf(e)):!!Object.getOwnPropertyNames(this._evt).length},t}();` |
|---------|

| ES3, 1017 Bytes |
|---------|
| `var Emitter=function(){function t(t){this._evt={},this._ctx=t||this}return t.extend=function(e){var n;return e&&"object"==typeof e&&(n=new t(e),["_evt","_ctx","on","off","once","emit","triggers"].forEach(function(t){e[t]=n[t]})),e},t.prototype.on=function(t,e){var n;return t&&e&&((n=this._evt[t])?(this.off(t,e),n.push(e)):n=[e],this._evt[t]=n),this},t.prototype.once=function(e,n){return n?this.on(e,function t(){this.off(e,t),n.apply(this,arguments)}):this},t.prototype.off=function(t,e){var n,i,o=arguments.length;return 0===o?this._evt={}:1===o?delete this._evt[t]:2===o&&-1<(n=(i=this._evt[t])?i.indexOf(e):-1)&&(i.splice(n,1),i.length||delete this._evt[t]),this},t.prototype.emit=function(t){var e,n,i=arguments,o=this._evt[t];if(o&&(n=o.length))for(o=o.slice(),i=1<i.length?[].slice.call(i,1):[],e=0;e<n;e++)o[e].apply(this._ctx,i);return this},t.prototype.triggers=function(t,e){var n;return t?!!(n=this._evt[t])&&(!(1<arguments.length)||-1<n.indexOf(e)):!!Object.getOwnPropertyNames(this._evt).length},t}();` |





