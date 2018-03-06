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

<pre><code>var Emitter=function(){function a(b){this._evt={};
this._ctx=b||this}a.extend=function(b){return new a
(b)};a.prototype.on=function(b,c){(this._evt[b]||(t
his._evt[b]=[])).push(c);return this};a.prototype.o
nce=function(b,c){return this.on(b,function d(){thi
s.off(b,d);c.apply(this,arguments)})};a.prototype.o
ff=function(b,c){if(0===arguments.length)this._evt=
{};else if(1===arguments.length)delete this._evt[b]
;else if(1===arguments.length){var a=this._evt[b],d
=a?a.indexOf(c):-1;-1<d&&a.splice(d,1)}return this}
; a.prototype.emit=function(b){var c=this._evt[b];i
f(c&&0<c.length){c=c.slice();for(var a=c.length,d=1
<arguments.length?Array.prototype.slice.call(argume
nts,1):[],e=0;e<a;e++)c[e].apply(this._ctx,d)}retur
n this};a.prototype.hasListeners=function(b,a){var 
c=this._evt[b];return c?1<arguments.length?-1<c.ind
exOf(a):!0:!1};return a}();</code></pre>