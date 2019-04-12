# Chapter 11 Testing

## Objectives

- Practice testing various parts of Angular

## Steps

1. Visit this link and save the zip on your c:\ drive.

   https://angular.io/generated/zips/testing/specs.testing.zip

2. Right click to unzip this zip. Open this folder in a command window and use **code .** to open to this location.

3. From the integrated terminal execute the script **ng test --code-coverage**. This will run all of the tests and give you a report in a Chrome window due to the configuration in karma.

4. We will examine different types of tests now.

5. Testing a Pipe.

   1. Open the file **src\app\shared\title-case.pipe.ts**
   2. Notice how the pipe works to transform the data. Pipes are easy to test because they are simply a function.
   3. Open the file **src\app\shared\title-case.pipe.spec.ts**
   4. Note the different tests being run. Calling the transform function with different data.
   5. Change describe on line 3 to be **fdescribe**.
   6. This will give this describe block focus and will be the only tests run now.
   7. Run the tests using _npm run tests_
   8. Notice only 5 tests are now run.
   9. Remove the f from describe

6. Testing a Service

   1. Open the file **src\app\demo\demo.ts**
   2. Notice its contents contain various items. Find the **ValueService**. (In a real-project you would have these as separate files.)
   3. The **ValueService** has no dependencies. This makes it even easier to test.
   4. Note the different tests being run.
