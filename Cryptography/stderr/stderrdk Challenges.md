11/26/23
```
IyBQcm9ncmVzcyBjb2RlICMxOiBZZDdBTThrckRCSUNqVTRaeDVyTFVFcFMKCk5leHQgY2hhbGxlbmdlOgovVGQ2V0ZvQUFBVG0xclJHQWdBaEFSd0FBQUFRejFqTUFRQkRJeUJRY205bmNtVnpjeUJqYjJSbElDTXlPaUJ1VmpsTU5tcEhOVU56UzFocFZFZE9OR1kwVjBGcWRHMEtDanhPWlhoMElHTm9ZV3hzWlc1blpTQm9aWEpsUGdvQUo3ak95NzF3ZjlvQUFWeEUraUk1UngrMjgzMEJBQUFBQUFSWldnPT0K
```
11/27/23(base64->xz->sqlite3)
```
"/Td6WFoAAATm1rRGAgAhARwAAAAQz1jM4B//ARRdACmURZ1gyBn4JmSIjib+MZX9x4eABpe77H+oCX4ENOqTjJ28OhWqqGO+kRFLn0FwxGy0KTG4Pnl9AIP/7hgkkcw/ZBtFFQI19zDVYOd9n5ZpgwXpI01+JmakruDp/EAc1ID7+9hx1+jgoxUqgyBvM6XHTxIgKcp8UsYY5OTYLifWSQnOcm90I5WJMHVxMGkBMcIIIYyZGBWWeUeORps1uCR02WvXFxq1e8cowdHZRt7U93/7DL3PODf64WYyAyjsq28l56FoeLnBKVpLMWesIDI+Z/fIXZgWXmiQtOSwhgkirIxxwsJZ09VEgbjz4d2zU2D7wJsB+wYrCuTL4smK0Vxap2fwG/ifb5pwotRyrCXE3JaAAADNh5uOIRcaOgABsAKAQAAAM6+cPrHEZ/sCAAAAAARZWg=="
```
Step One
```
echo "/Td6WFoAAATm1rRGAgAhARwAAAAQz1jM4B//ARRdACmURZ1gyBn4JmSIjib+MZX9x4eABpe77H+oCX4ENOqTjJ28OhWqqGO+kRFLn0FwxGy0KTG4Pnl9AIP/7hgkkcw/ZBtFFQI19zDVYOd9n5ZpgwXpI01+JmakruDp/EAc1ID7+9hx1+jgoxUqgyBvM6XHTxIgKcp8UsYY5OTYLifWSQnOcm90I5WJMHVxMGkBMcIIIYyZGBWWeUeORps1uCR02WvXFxq1e8cowdHZRt7U93/7DL3PODf64WYyAyjsq28l56FoeLnBKVpLMWesIDI+Z/fIXZgWXmiQtOSwhgkirIxxwsJZ09VEgbjz4d2zU2D7wJsB+wYrCuTL4smK0Vxap2fwG/ifb5pwotRyrCXE3JaAAADNh5uOIRcaOgABsAKAQAAAM6+cPrHEZ/sCAAAAAARZWg=="|base64 -d>stderr.xz|unxz>stderr
```
file stderr
![[Pasted image 20231128011749.png]]
```select base64 from codes order by number;```
![[Pasted image 20231128011954.png]]
11/28/23
```
iVBORw0KGgoAAAANSUhEUgAAAFIAAABSAQMAAAD94hHYAAAABlBMVEUAAAD///+l2Z/dAAABHklEQVQokZXTsaqkMQgG0ICt4KsItgFfPZBWyKsItoI3Owyz13+aXatThPBpzKhPrfEv9iF5wmBAd5TsxFSNh4HD5waWL4uDyben8EH4crEm1vv+v74ZXvXO8/ENi7YU3vk/dlc+S2/q7pwnmQ756S5mXbzW0O7IDB7B9bAfRTFyhe5aKYcAhbozaeA85vqwOvrQO8VuZ/KyyindSTUFCUO7g6SOL8rqzp0xfIdRdxCihLjIw17iaMOpu0gGMuKu7rC0lTAXdd8WPUKZoDv2beMgvs7/cjnpYRqvd/ztmYJ4Zy7dnmwIwIO6qyLi4Pbq9nFjyQrW7rvDaLl3yMMgbiIM8LT+yWzz23pXL6geLg60MqVuH2xikQzd//lPfwATWwAFktW4SgAAAABJRU5ErkJggg==
```
base64 to  png
```
echo "iVBORw0KGgoAAAANSUhEUgAAAFIAAABSAQMAAAD94hHYAAAABlBMVEUAAAD///+l2Z/dAAABHklEQVQokZXTsaqkMQgG0ICt4KsItgFfPZBWyKsItoI3Owyz13+aXatThPBpzKhPrfEv9iF5wmBAd5TsxFSNh4HD5waWL4uDyben8EH4crEm1vv+v74ZXvXO8/ENi7YU3vk/dlc+S2/q7pwnmQ756S5mXbzW0O7IDB7B9bAfRTFyhe5aKYcAhbozaeA85vqwOvrQO8VuZ/KyyindSTUFCUO7g6SOL8rqzp0xfIdRdxCihLjIw17iaMOpu0gGMuKu7rC0lTAXdd8WPUKZoDv2beMgvs7/cjnpYRqvd/ztmYJ4Zy7dnmwIwIO6qyLi4Pbq9nFjyQrW7rvDaLl3yMMgbiIM8LT+yWzz23pXL6geLg60MqVuH2xikQzd//lPfwATWwAFktW4SgAAAABJRU5ErkJggg=="|base64 -d>stderr.png
```

```
file stderr
```
	
![[Pasted image 20231128145925.png]]
Bonus - extract the sexcret key from the totp, base 32 decode
```
echo "HQWS2ICIMVWGY3ZMEBLW64TMMQQC2LJ6"|base32 -d
```
<-- Hello, World -->
11/29/23
```
echo "H4sIAAAAAAACA0WMQQ4CIRAEv9I3LsRvGC/GL4xLI0QYEph1g68X48FbpZKqi6uw1lDkPRegypMQKA9sSUqhPuhx3w05YrYdSV6EJeJ2PSP2VjE5jD3I9F/f6cYaDG6dK9Kf8ziIkIM6Q8wa/tHpA3Bx1OuCAAAA"|base64 -d>stderr.gz&&gunzip stderr.gz&&cat stderr
```
11/30/23
```
echo "H4sIAMLlaGUCAwsw4bI0U7DgSqtLSLBhYDhmU5NQk5aQkJAGZKelJaQhs+sqwOxraTVw8X9pOVA2D8M7sPq6ujobHqA5aXU1DCAgASYZALyuLDtoAAAA"|base64 -d>stderr.gz&&gunzip stderr.gz&&display stderr
```
Wireshark Weirdness - 1
```
H4sIAEAQaWUCA1u4ycaXgYmBhQEOloQCCcbUSQz11rNO/geytUD4PxgwZaTm5ORzsDEwcjCwsTAwQvgr/zEwQvQCWUxQnf9gOiFqmMrzi3JS4DqZIHyQeoQZAE3Jp7GMAAAA
```
Wireshark Weirdness - 2
```
H4sIAEAQaWUCA1u4ycaXgYmBhQEOloQCCcbUSQz11rNO/geytUD4PxgwZaTm5ORzsDEwcjCwsTAwQvgr/zEwQvQCWUxQnf9gOiFqmMrzi3JS4DqZIHyQeoQZAE3Jp7GMAAAA
```

Packet Challenge
```
echo "H4sIAO4UaWUCA1u46fAVBiYGFgY4WBIKJBhTJzHUM/A72QPZWiD8HwyYMlJzcvI52BgYORjYWBgYIfyV/xgYIXqBLCaoTjuYTogapvL8opwUuE4mCB+kHmEGACzHfFaMAAAA"|base64 -d>stderr.gz&&gunzip stderr.gz&&mv stderr stderr.pcap
```

```
tcpdump -r stderr.pcap --nano
```
![[Pasted image 20231206170254.png]]
```
tcpdump -r stderr.pcap -nttttvvXX
```

Filesystem
```
sudo mount ~/Documents/stderr/trshpuppy /mnt/stderr
```

12/13/23
```
echo '/Td6WFoAAATm1rRGAgAhARwAAAAQz1jM4AcgAGhdABBjvT6qRn3bSjjuxHMO4ndwdEVSOpq7T2+C6c5by523r1zOG1fWbFugXWXLiyQEJW0y8GzqPaJqZMQzY0TPBz715+9RFSrxDTKBYB8KmACCRRkqpNhwZAdoh+i0IyeDEQdX+AGSSSawANhrlcxJfyh8AAGEAaEOAADJ+F2EscRn+wIAAAAABFla'|base64 -d>out.xz&&unxz out.xz&&cat out&&rm -rf out
```


1/17/24
```
ATTFPB2CA43UOJSWC3JANFZSA33OEB2GQZJAGEYHI2BMEBZGSZ3IOQ7Q | base32 -d | xxd -c0 -ps | cut -c2-69 | xxd -r -ps
```


3/20/24 -- OpenSSL Salted Password
```
echo "U2FsdGVkX19TDGVBUTFsYy5u9gxepz1ngi/Wt7XiKLDAUmq9yUv6HAFGWr8XnB/II0OLU5J4IfokvrmvOJfEqefiOWVt583LvCqZi3q+w275N0X1lSSTvQ4F/aQrTWxI"|base64 -d|openssl enc -d -k 'Tiddies!' -pbkdf2 -aes-256-cbc -out decrypted&&cat decrypted&&rm -rf decrypted package main
```


3/22/24
```
echo "D6FQQAAAAAAAAAQDGM3EMAJGVBOGGCZUXYMTFBYLRBGXCKBQGPDA5YHSLQDITBEU4AYMUCDCGNXDXDGQ7ADKQXBOMNJ2BXIGM2DGRSWMRFYQOFY6BVDIJQQCVQM4LX7ILYYMC3JEYRTEGJB7TFA7SBSASYQ4QQYGRFOAA7W45LI5AAIAAA======"|base32 -d|gzip -cd|xxd -r -p|xxd -r -p|xxd -r -p|xxd -r -p|xxd -r -p
```

![[Pasted image 20240323120236.png]]
