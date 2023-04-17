The class Movie is stated below. An instance of class Movie represents a film. This class has the following three properties:

-   title, which is a String representing the title of the movie
-   studio, which is a String representing the studio that made the movie
-   rating, which is a String representing the rating of the movie (i.e. PG­13, R, etc)

**a) Write a constructor for the class Movie, which takes a String representing the title of the movie, a String representing the studio, and a String representing the rating as its arguments, and sets the respective class properties to these values.**

```js
class Movie {
  constructor() {
    this.title = 'Paiya';
    this.studio= 'Red jaint'
    this.rating= 'PG 13'
    console.log(Movie1.rating);
  }
}

const Movie1 = new Movie();
```
**b) The constructor for the class Movie will set the class property rating to "PG" as default when no rating is provided.**
```js
class Movie {
  constructor(title, studio, rating) {
    this.title = title;
    this.studio= studio;
    if(this.rating == undefined){
        this.rating='PG';
    }
  }
}

const Movie1 = new Movie('Paiya', 'Redjaint', true);

console.log(Movie1.rating);
```
**c) Write a method getPG, which takes an array of base type Movie as its argument, and returns a new array of only those movies in the input array with a rating of "PG". You may assume the input array is full of Movie instances. The returned array need not be full.**
```js
var movies= [{
  "title":"Harry Potter",
  "studio":"Warner Bros. Pictures",
  "rating":"PG"
  },
  {
  "title":"Avatar",
  "studio":"Nickelodeon Animation",
  "rating":"PG 13"
  },
  {
  "title":"Life of Pi",
  "studio":"Rhythm & Hues",
  "rating":"PG"
  }
]

function getPG(movies) {
  const pgMovies = [];
  for (let i = 0; i < movies.length; i++) {
    if (movies[i].rating === 'PG') {
      pgMovies.push(movies[i].title);
    }
  }
  return pgMovies;
}
console.log(getPG(movies));
```
**d) Write a piece of code that creates an instance of the class Movie with the title “Casino Royale”, the studio “Eon Productions”, and the rating “PG­13”**
```js
class Movie {
  constructor(title, studio, rating) {
    this.title = title;
    this.studio= studio;
    this.rating= rating;
  }
}

const Movie1 = new Movie('Casino Royale', 'Eon Productions', 'PG 13');

console.log(Movie1);
```
**2.Convert the UML diagram to Typescript class**
```js
class Circle{
  constructor(radius, color){
    this.setRadius(radius);
    this.setColor(color);
  }
  setRadius(radius){
    this.radius = radius;
  }
  getRadius(){
    return this.radius;
  }
  setColor(color){
    this.color = color;
  }
  getColor(){
    return this.color;
  }
  getArea(){
     return this.area=Math.PI * this.radius * this.radius;
  }
  getCircumference(){
      return this.circumference=2* Math.PI * this.radius;
  }
}
let a=new Circle(2, "Red");
console.log(a.getRadius())

a.setRadius(5);
console.log(a.getRadius())

console.log(a.getArea());
console.log(a.getCircumference());
```


**3.Write a “person” class to hold all the details.**
```js
class person{
    constructor(){
        this.firstname= "Nivetha";
        this.lastname = "Bharathi";
        this.age = 28;
        this.email = "nivethabharathi77@gmail.com";
        
        console.log(`My name is ${this.firstname} ${this.lastname},
My age is ${this.age},
My mailID is ${this.email}`);
    }
}
a = new person();
```

**4.write a class to calculate the uber price.**
```js
class Uber {
    constructor() {
      this.distance = 10;
      this.time = 25;
      this.bookingFare = 40;
      this.costPerMile = 35;
      this.costPerMinute = 15;
      this.baseFare = 80;
    }
    calculateFare() {
      const perMile = this.distance * this.costPerMile;
      const perMin = this.time * this.costPerMinute;
      const totalfare = this.bookingFare + perMile + perMin;
      return totalfare < this.baseFare ? this.baseFare : totalfare;
    }
}
let ride = new Uber();
console.log(ride.calculateFare());
```