# Value, Reference and Collections

This sprint will help you get used to examining, creating and manipulating the building blocks of data in JavaScript - arrays and objects (often referred to collectively as 'collections').

Remember:
* Two collections that contain the same information are nonetheless two different collections.
* Two different references to the same collection are nonetheless the same collection, and mutating information in one reference will mutate the information in the other reference too.

Your task is to write functions that solve the problems presented below. 
* Test your code in the spec folder.
* **Test for mutation!!!** - should you be mutating the original data or not? How can you test this?

You have all the Array and Object methods at your disposal - keep referencing MDN ([Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), [Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)).

We provide test data for some questions - for others you will have to create your own. Consider storing all the test data in a separate file and exporting it so it can be reused where appropriate.

After every successfully implemented solution, commit your code. After around half an hour, swap your pair roles so you each get a good spell driving and navigating.

### getEvenNums()

Write a function that takes an array of numbers and returns a new array of just the even numbers.

```js
const numbers = [4, 6, 7, 9, 99, 9900, 467999900]

getEvenNums(numbers) // [4, 6, 9900, 467999900]
```

### splitNums()

Write a function that takes an array of numbers and returns a new array of arrays containing the numbers split in two. Even numbers should return a pair of the halved number; odd numbers should return the integer either side of the halved number.

```js
const numbers = [4, 6, 7, 9, 99]

splitNums(numbers) // [[2, 2], [3, 3], [3, 4], [4, 5], [49, 50]]
```

### totalMultiples()

Write a function that takes two arguments: an array of numbers and another integer. It should return a total of all the number which are multiples of the given integer.

```js
const numbers = [4, 6, 7, 9, 99]

totalMultiples(numbers, 3) // 114
```

### capitalizeCatNames()

Write a function that takes an array of cat name strings and return a new array with the first letter of each name capitalised.

```js
const catNames = ['mr sniffles', 'mrs tiggles', 'senor wibblez'];

capitalizeCatName(catNames) // ['Mr Sniffles', 'Mrs Tiggles', 'Senor Wibblez'] 
```

### getOldCats()

Create an array of cat objects with `name` and `age` properties. Write a function that returns a **new array** of senior cat objects (cats at least 10 years old).

### getNonSnootyCats()

Add a `personality` property to each cat, and give it a value of an array of personality strings. Write a function that returns a **new array** without any 'snooty' cats.

### discardHomicidalCats()

Write a function that removes any homicidal cats from the same array, and returns the number of cats removed.

### flattenArrays()

Should take an array of arrays and return a flattened, single, **new array**, with the entries from each array returned in the same order. There are many ways of doing this, although we'd like you to do it with `.forEach`.

```javascript
flattenArrays([[1, 2, 3], ['a', 'b', 'c', 'd']]) 
// [1, 2, 3, 'a', 'b', 'c', 'd']
```

### mergeArrays()

Should take an array of arrays and return a flattened, single, **new array**, with the entries from each array returned in alternating order. If the arrays are not the same length, the shorter arrays should add `undefined` to the merged array until all values have been merged. Again, there are many ways of doing this - any is fine, as long as it's an array method (not a for loop).

```javascript
mergeArrays([[1, 2, 3], ['a', 'b', 'c', 'd']]) 
// [1, 'a', 2, 'b', 3, 'c', undefined, 'd']
```

### totalPopulation() 

Write a function that takes an array of place objects with properties `place` (string) and `population` (number). It should return the combined total population.

```js
const places = [
  {
    place: 'Java',
    population: 141370000
  },
  {
    place: 'Honchu',
    population: 104000000
  },
  {
    place: 'Great Britain',
    population: 61700000
  }, 
  {
    place: 'Luzon', 
    population: 53336000
  }
]

totalPopulation(places) // 360406000
```

### findNewLand()

Using the same dataset, write a function that takes your array of places and returns a **new array** of **new place objects** with the place name preceded by 'new' and 10% of the old population.

```js
//using the same dataset

findNewLand(places) /*
[
  {
    place: 'New Java',
    population: 14137000
  },
  {
    place: 'New Honchu',
    population: 10400000
  }
  // ...etc
]

*/
```

### doctorByDuration() 

Write a function that takes two arguments: an array of doctor objects and a number of years. It should return a **new array** of doctor objects containing doctors who were serving after this number of years. 

```js
const doctors = [
    { number: 1,  actor: "William Hartnell",      begin: 1963, end: 1966 },
    { number: 2,  actor: "Patrick Troughton",     begin: 1966, end: 1969 },
    { number: 3,  actor: "Jon Pertwee",           begin: 1970, end: 1974 },
    { number: 4,  actor: "Tom Baker",             begin: 1974, end: 1981 },
    { number: 5,  actor: "Peter Davison",         begin: 1982, end: 1984 },
    { number: 6,  actor: "Colin Baker",           begin: 1984, end: 1986 },
    { number: 7,  actor: "Sylvester McCoy",       begin: 1987, end: 1989 },
    { number: 8,  actor: "Paul McGann",           begin: 1996, end: 1996 },
    { number: 9,  actor: "Christopher Eccleston", begin: 2005, end: 2005 },
    { number: 10, actor: "David Tennant",         begin: 2005, end: 2010 },
    { number: 11, actor: "Matt Smith",            begin: 2010, end: 2013 },
    { number: 12, actor: "Peter Capaldi",         begin: 2013, end: 2017 },
    { number: 13, actor: "Jodie Whittaker",       begin: 2017, end: 2017 } 
];

doctorByDuration(doctors, 4) 
/* 
[
  {
    number: 3,  
    actor: "Jon Pertwee", 
    begin: 1970, 
    end: 1974
  },
  {
    number: 4,  
    actor: "Tom Baker",             
    begin: 1974, 
    end: 1981
  },
  { 
    number: 10, 
    actor: "David Tennant",  
    begin: 2005, 
    end: 2010 
  },
  { 
    number: 12,
    actor: "Peter Capaldi",
    begin: 2013,
    end: 2017 
  }
] */
```
### surnamesLongerThanForenames()

Should take the array of doctor objects and return a **new array** of the actor names whose surnames are longer than their fornenames.

### changeActorToPlayedBy()

Write a function that takes the array of doctor objects and returns a **new array** of **new doctor objects** with the `actor` key replaced by `playedBy`.

### findUpcomingGraduate()

Create an array of people objects with properties `firstName` (string), `lastName` (string), `age` (number) and `courseStage` (number less than 7) properties. Write a function that returns the name of the first student in the array who is currently at `courseStage` 6, or returns `null` if there is no such student.

### sortStudents()

Write a function that takes three arguments: the student information, the property by which to sort, and a boolean that determines whether to sort ascending or descending. It should return a **new array** with the original student objects sorted according to the criteria passed in.

### progressStudents()

Write a function that takes the same student information and returns a **new array** of **new student objects** with the courseStage property increased by 1. The `courseStage` property should not exceed 6; any student already on stage 6 should remain there and should receive a `graduate` property set to `true`.

### createStudentReport()

Write a function that takes the same information and returns an object with the following properties: `numberOnRole` (the total number of students in the array), `atStage1`, `atStage2` ... up to `atStage6` (an array of student names at each stage) and `averageAge` (the mean average age of all students).

Too easy? Use only `reduce` to compile your object and return it directly.

### calculateConfectioneryCosts()

Write a function that takes an array of pop star objects with information about the amount they have spent so far this year on confectionery at the cinema, and how much they have spent on today's visit. It should return a **new array** of **new objects** with a property for the pop star's `name` and the `yearlyCumulativeSpend` property updated to include today's costs.

```js
const celebs = [
    {
        name : 'Beyonce Bowls',
        yearlyCumulativeSpend : '£44',
        purchaseToday : {
            item : 'White mice',
            costPerItem : '£3',
            amountBought : 17
        }
    },
    {
        name : 'Kray-Z',
        yearlyCumulativeSpend : '£28',
        purchaseToday : {
            item : 'Flying saucers',
            costPerItem : '£2',
            amountBought : 28
        } 
    },
    {
        name : 'Matey Terry',
        yearlyCumulativeSpend : '£36',
        puchaseToday : {
            item : 'Cola bottles',
            costPerItem : '£4',
            amountBought : 81
        } 
    },
    {
        name : 'Justine Klimberbake',
        yearlyCumulativeSpend : '£30',
        purchaseToday : {
            item : 'Giant jelly snakes',
            costPerItem : '£103',
            amountBought : 2
        } 
    }
]

calculateConfectioneryCosts(celebs)
/*
[
    {
        name: 'Beyonce Bowls',
        yearlyCumulativeSpend: £95
    },
    // ...etc
*/
```

### reduceConfectioneryCosts()

All this positive press is leading to a boost in sales and means prices can be reduced. Write a function that takes the same celebrity informationand returns a **new array** of confectionery with new prices after a 10% price reduction. Express the new cost in pence.

```js
//using same dataset

reduceConfectioneryCosts(celebs)
/*
[
    {
        item : 'White mice',
        newCostPerItem : 270p
    },
    // ...etc.
]
*/
```

### Reimplementation

Reimplement the following higher-order JavaScript array functions. Each function should take as arguments an array and an iteratee function. They should produce the same output and have the same effect on the input as the Javascript version. (And no, you can't just use the JavaScript version...)

#### map()

#### filter()

#### every()

#### some()

#### includes()

#### slice()

#### splice()

### refurbishCentresOfPower()

All the world leaders are in a race to refurbish their homes. Please move them next door (up one houseNo) whilst they redecorate. You should test to ensure that none of your objects are mutated, so the leaders can find their original homes.

```js
const leaders = [
  {
    name: 'Donald Trump',
    address: {
      houseNo: 1600,
      road: 'Pennsylvania Avenue',
      city: 'Washington D.C.'
    }
  },
  {
    name: 'Theresa May', 
    address: {
      houseNo: 10, 
      road: 'Downing Street',
      city: 'London'
    },
  },
  {
    name: 'Maha Vajiralongkorn',
    address: {
      houseNo: 10200,
      road: 'Na Phra Lan Road',
      city: 'Bangkok'
    }
  },
  {
    name: 'Kim Kardashian',
    address: {
      houseNo: 3145, 
      road: 'Abington Drive',
      city: 'Beverly Hills'
    }
  }
]

refurbishCentresOfPower(leaders)
/*
[
    {
        name: 'Donald Trump',
        address: {
            houseNo: 1601,
            road: 'Pennsylvania Avenue',
            city: 'Washington D.C.'
        }
    }
    // ...etc
]
*/
```

### bringPeaceToSpace()

All the world leaders have decided to move to a space station so they can bring peace to the wider galaxy. Write a function that takes the array of leader objects and *either* the string address *or* an object with a starting address, and move each leader to consecutive addresses on the station.

```js
let startingAddress = '1 Pale Blue Dot View, Lunarcyville';
//OR
startingAddress = {
  houseNo: 1, 
  road: 'Pale Blue Dot View', 
  city: 'Lunarcyville'
}

bringPeaceToSpace(leaders, startingAddress) 
/*
[
  {
    name: 'Donald Trump',
    address: '1 Pale Blue Dot View, Lunarcyville'
  },
  {
    name: 'Theresa May', 
    address: '2 Pale Blue Dot View, Lunarcyville'
  },
  {
    name: 'Maha Vajiralongkorn',
    address: '3 Pale Blue Dot View, Lunarcyville'
  },
  {
    name: 'Kim Kardashian',
    address: '4 Pale Blue Dot View, Lunarcyville'
  }
]

*/
```