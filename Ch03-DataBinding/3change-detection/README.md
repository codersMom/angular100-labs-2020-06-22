# Chapter 3 DataBinding: Display data in the template

## Objectives

- Overview in this lab, you will create an interval timer which makes changes to the array of albums

## Steps

1. Create a property titleCounter and set it equal to 1

2. In template html - use Albums Title # {{titleCounter }}

3. In ngOnInit create an interval timer, where every 2 seconds, you update the titleCounter by one.

   this.titleCounter = titleCounter + 1

4. You should see the screen get updated every second with the new value
