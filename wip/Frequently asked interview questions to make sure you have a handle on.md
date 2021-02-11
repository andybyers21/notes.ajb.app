# Frequently asked interview questions to make sure you have a handle on

Q: What’s the difference between .forEach and .map? – It’s easy to get these two confused when you’re first starting out, because in a way they are pretty similar. Both map and forEach are used to iterate over an array. The main difference here though is that .map returns a new array, while forEach just iterates through the original array.

So when should you use either?

A: The map() method is quite handy (especially in react) when you want to iterate over data in an array and manipulate it in some way. For example, say you’ve got an array of cities, and you want render them all as list items with the name of the city to the page. Example:

```
const Page = () => {
  const cities = ['Sydney', 'Los Angeles', 'Seoul'];

  return (
    <div className="container">
      <h1>Favourite Cities</h1>
      <ul>
        {cities.map(city => (
          <li>{city}</li>
        ))}
      </ul>
    </div>
  );
};
```

What’s happening here is you’re taking your original array of strings and returning an array of elements, which can then be rendered to the DOM.

So what about forEach()? This method is useful when you want to run an operation on each value in an array. For example:

```
const hasEvenNumbers = numbers => {
  let hasEvens = false;
  numbers.forEach(number => {
    if (number % 2 === 0) {
      hasEvens = true;
    }
  });

  return hasEvens;
};

console.log(hasEvenNumbers([1,3,5])) // false
console.log(hasEvenNumbers([1,3,5,6])) // true
```

Although you could still technically return an array of elements using a forEach, and you can map over an array of numbers and check if they contain evens, that doesn’t always mean it’s the best tool for the job. You can probably cut a steak with a spoon.. er you get the picture.

#tk/code