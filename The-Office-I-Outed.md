Your colleagues have been looking over you shoulder. When you should have been doing your boring real job, you've been using the work computers to smash in endless hours of codewars.

In a team meeting, a terrible, awful person declares to the group that you aren't working. You're in trouble. You quickly have to gauge the feeling in the room to decide whether or not you should gather your things and leave.

Given an object (meet) containing team member names as keys, and their happiness rating out of 10 as the value, you need to assess the overall happiness rating of the group. If <= 5, return 'Get Out Now!'. Else return 'Nice Work Champ!'.

Happiness rating will be total score / number of people in the room.

Note that your boss is in the room (boss), their score is worth double it's face value (but they are still just one person!).

The Office II - Boredom Score
The Office III - Broken Photocopier
The Office IV - Find a Meeting Room
The Office V - Find a Chair

my solutions:

```js
function outed(meet, boss){
  let total = 0
  for (const [key, value] of Object.entries(meet)) {
    if (key === boss) {
    total += value * 2
  } else {
    total += value
  }
  }
  const avg = total / Object.keys(meet).length
  if ( avg <= 5) return 'Get Out Now!'
    return 'Nice Work Champ!'
}

/* ----------------------------- */

function outed(meet, boss){
  let total = Object.values(meet).reduce((acc, value) => acc + value, 0)
  total += meet[boss]
  
  const avg = total / Object.keys(meet).length
  if ( avg <= 5) return 'Get Out Now!'
    return 'Nice Work Champ!'
} 


```

```js

function outed(c, b) {
  return Object.keys(c).reduce((s, e) => s + c[e] * (e === b ? 2 : 1), 0) / Object.keys(c).length > 5 ? "Nice Work Champ!" : "Get Out Now!";
}

/* ----------------------------- */

const outed = (meet, boss, arr = Object.values(meet)) => 
  arr.reduce((sum, rating) => sum + rating, meet[boss]) / arr.length > 5 ? 'Nice Work Champ!' : 'Get Out Now!';
  
```

