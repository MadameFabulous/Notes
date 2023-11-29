base64 -> xz
```
printf '/Td6WFoAAATm1rRGAgAhARwAAAAQz1jMAQBDIyBQcm9ncmVzcyBjb2RlICMyOiBuVjlMNmpHNUNzS1hpVEdONGY0V0FqdG0KCjxOZXh0IGNoYWxsZW5nZSBoZXJlPgoAJ7jOy71wf9oAAVxE+iI5Rx+2830BAAAAAARZWg==' | base64 -d | xz -cd
```

base64 -> hexidecimal->rot13/caesar 13
```
echo "NDcgNzUgNzIgMjAgNDMgNjUgNzYgNjEgNzAgNzIgNjYgNjYgMjAgNmMgNjIgNjggMjcgNjUgNzIgMjAgNzkgNjIgNjIgNzggNzYgNjEgNzQgMjAgNzMgNjIgNjUgMjAgNzYgNjYgMjAgNzYgNjEgMjAgNmUgNjEgNjIgNjcgNzUgNzIgNjUgMjAgNzAgNmUgNjYgNjcgNzkgNzIgMmU="|base64 -d|xxd -r -p|tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
