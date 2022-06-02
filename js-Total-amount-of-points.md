Our football team finished the championship. The result of each match look like "x:y". Results of all matches are recorded in the collection.

For example: ["3:1", "2:2", "0:1", ...]

Write a function that takes such collection and counts the points of our team in the championship. Rules for counting points for each match:

    if x > y: 3 points
    if x < y: 0 point
    if x = y: 1 point

Notes:

    there are 10 matches in the championship
    0 <= x <= 4
    0 <= y <= 4


**my solution**

```js
function points(games) {
  let points = 0
  for (game of games) {
    if (Number(game[0]) > Number(game[2])) {
        points += 3;
    }else if 
      (Number(game[0]) < Number(game[2])) {
       points += 0;
    } else {
        ++points
    }   
  }
  return points
}

```

another solutions:

```js 
const points=games=>games.reduce((output,current)=>{
    return output += current[0]>current[2] ? 3 : current[0]===current[2] ? 1 : 0;
  },0)
  
  
function points(games) {
  let total = 0;
  games.map(game => {
    if (game[0] === game[2]) {
      total += 1;
    } else if (game[0] > game[2]) {
      total += 3;
    }
  });
  return total;
}


const points = g => g.reduce((a, [x, _, y]) => a + (x > y ? 3 : x == y), 0)

const points = games => games.reduce((sum, [x, , y]) => sum + (x > y ? 3 : x == y), 0)

const points = games => games
  .map(str => str.split(':').map(Number))      // parse
  .map(([x, y]) => x > y ? 3 : x < y ? 0 : 1)  // determine points
  .reduce((sum, points) => sum + points, 0);   // sum points
```

