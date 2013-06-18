This is a GitHub mirror of http://unixpapa.com/js/querystring.html

Usage:

``` javascript
var str = "key1=&key2&search=Rock+%26+Roll&rock%26roll=here+to+stay&key3=dog&key3=cat&key3=mouse&weird=%26%CE%A8%E2%88%88";
var qs = new QueryString(str)
```

```
Key       | Last Value    | All Values
=========================================
key1      |               |
key2      |               |
key3      | mouse         | dog,cat,mouse            
rock&roll | here to stay  | here to stay
search	  | Rock & Roll   | Rock & Roll
weird     | &Ψ∈           | &Ψ∈
```

``` javascript
>>> jQuery.param(qs.dict, true)
"key1=&key2=&search=Rock+%26+Roll&rock%26roll=here+to+stay&key3=dog&key3=cat&key3=mouse&weird=%26%CE%A8%E2%88%88"
```
