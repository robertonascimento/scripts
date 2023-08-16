# This repository is intended for shell script examples

#### Content
* [Execute command passing parameter resulting from another command](#item1)

<br>
<a name="a"></a>

### Execute command passing parameter resulting from another command

&#09;This example will download the jpeg file getting the address of image from json response on the first command

&#09;To perform this is necessary use the ***jq*** and ***xargs*** commands

&#09;The ***jq*** helps to get the address of image on thumbnail attribute from json response of the first ***curl***

&#09;The ***xargs*** put the output from ***jq*** on second ***curl*** command

```bash
curl -s -X GET https://dummyjson.com/products/1 | jq '.thumbnail' | xargs curl  -O
```
