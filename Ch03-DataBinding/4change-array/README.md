# Chapter 3 DataBinding: Changing an array

## Objectives

- Overview in this lab, you will practice changing an array

## Steps

1. In your app.component.ts file, add a variable called numbers: number[];

2. Inside of **ngOnInit**, set numbers to [1,2,3]

3. Within app.component.html, after the jumbotron use interpolation to display the numbers using:

   ```html
   <p>Featured Albums: {{ numbers }}</p>
   ```

4. In the interval timer, add 4 to the to numbers using this.numbers.push(4) and then use a console.log to display numbers.

5. Run your code and open the console. You can refresh to see it start from the beginning. Notice the array of numbers is growing but the screen is not updating.

6. To address this, you can instead use the assignment operator to copy the current array to a new array. Add this line of code after the console.log - it uses the spread operator to copy values form the array to a new array - and assign it back to the original variable.

   ```javascript
   this.numbers = [...this.numbers];
   ```

7. Refresh the browser, you should now see the numbers showing on the screen.

8. Now, inside of the interval function, change the albumsArray[0] price property to be increased by ten dollars.

   ```javascript
   albumsArray[0].price += 10;
   ```

9. Can you see your changes on the screen? How did this compare to adding/removing items from an array?

10. Mark your work as complete
