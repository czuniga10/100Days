Day22 - 1hr

JavaScript - Codewars Kata

Description:
Encrypt this!

You want to create secret messages which can be deciphered by the Decipher this! kata. Here are the conditions:

Your message is a string containing space separated words.
You need to encrypt each word in the message using the following rules:
The first letter needs to be converted to its ASCII code.
The second letter needs to be switched with the last letter
Keepin' it simple: There are no special characters in input.

### Example Outputs
```
encryptThis("Hello") === "72olle"
encryptThis("good") === "103doo"
encryptThis("hello world") === "104olle 119drlo"
```
#### Code
```
var encryptThis = function(text) {
  if(text === ""){
    return "";
  }
  var answer = [];
  
  var textArr = text.split(" ");
  for(var el in textArr){
    var result = "";
    var first = textArr[el].charCodeAt(0);
    var temp2 = textArr[el][1];
    var tempL = textArr[el][textArr[el].length-1];
    var middle = textArr[el].slice(2,-1);
    if(textArr[el].length === 1){
      result = first;
    }
    else if(textArr[el].length === 2){
      result = first + temp2;
    }
    else if(textArr[el].length === 3){
      result = first + tempL + temp2;
    }
    else if (textArr[el].length >= 4){
      result = first + tempL + middle + temp2;
    }
    answer.push(result);
    
  }
  return answer.join(" ");
}
```