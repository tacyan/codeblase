# 参考

https://developer.mozilla.org/ja/docs/Web/API/Document/getElementsByClassName

## htmlでid指定する場合

```
<div id="map"></div>
document.getElementById('map')
```

## classで指定する場合

```
<div class="name"></div>
elements = document.getElementsByClassName(name)
```

'test' クラスを持っている要素の全てを得ます。

```
document.getElementsByClassName('test')
```

'red' クラスと 'test' クラスを持っている要素の全てを得ます。

```
document.getElementsByClassName('red test')
```

main' ID を持っている要素内で、'test' クラスを持っている要素の全てを得ます

```
document.getElementById('main').getElementsByClassName('test')
```

## 使い方サンプル

```
<body>
<ul>
	<li class="hoge">りんご</li>
	<li class="hoge foo bar">みかん</li>
	<li class="hoge foo">メロン</li>
	<li class="hoge bar">スイカ</li>
</ul>
<hr>
<div id="result"></div>
<script>
var element = document.getElementById( "result" ) ;
var elements = document.getElementsByClassName( "hoge" ) ;

console.log( elements ) ;
element.textContent = elements + "\n\n" ;

element.textContent += elements[0].outerHTML + "\n" ;
element.textContent += elements[1].outerHTML + "\n" ;
element.textContent += elements[2].outerHTML + "\n" ;
element.textContent += elements[3].outerHTML + "\n" ;
</script>
</body>
```
