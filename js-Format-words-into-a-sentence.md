Complete the method so that it formats the words into a single comma separated value. The last word should be separated by the word 'and' instead of a comma. The method takes in an array of strings and returns a single formatted string.

Note:

Empty string values should be ignored.
Empty arrays or null/nil/None values being passed into the method should result in an empty string being returned.
Example: (Input --> output)

['ninja', 'samurai', 'ronin'] --> "ninja, samurai and ronin"
['ninja', '', 'ronin'] --> "ninja and ronin"
[] -->""


´´´js

function formatWords(words){
    let str = ""
    if (!words || words === []) {
      return "" 
    } else if (words.length === 1) {
        return words[0] 
    }else {
    for (let i=0; i < words.length; i++){
      if (words[i].length >0){
      str = str +", " +words[i]
      }
    }
}
   let newStr = str.slice(2,str.lastIndexOf(",")) 
    if (newStr.length === 0) {
      return str.slice(str.lastIndexOf(" ") +1)
    } else {
    return  newStr +" and" +str.slice(str.lastIndexOf(" "))
  }
}
