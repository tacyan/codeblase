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
