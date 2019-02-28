Day23 - 1.5hrs

JavaScript - Codewars Kata

Description:
Write Number in Expanded Form

You will be given a number and you will need to return it as a string in Expanded Form. For example:

### Example Outputs
```
expandedForm(12); // Should return '10 + 2'
expandedForm(42); // Should return '40 + 2'
expandedForm(70304); // Should return '70000 + 300 + 4'
```
#### Code
```
function expandedForm(num) {
  if(num < 10){
    return num.toString();
  }
  var arr = [];
  var result = [];
  var numStr = num.toString();
  var length = numStr.length;
  arr = numStr.split("")
  for(var i = 0; i < length; i++){
    if(arr[i] === "0"){
        continue;
    }
    if(i === length - 1 && i !== "0"){
      result.push(arr[i]);
      break;
    }
    else{
      var n = length-i;
      var a = [];
      for(var j = 1; j < n;j++){
        a.push("0");
      }
      result.push(arr[i] + a.join(""));
    }
  }
  return result.join(" + ")
}
```