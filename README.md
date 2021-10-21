# Introduction

This is a simple Taxi Fare Calculating Program in which the Distance Travelled and Time Taken to Cover the Distance is taken input from the user and the corresponding fare is outputted.

---

## File Structure

- `app.js` : This script is used to run the server.
- `server.js` : This script contains the get and post methods used in the program.

- `fareutils.js` : This script contains the logic behind calculating the fare.

---

## How - To - Use :

- `http://localhost:2222` : Go to the following link and enter the values . The <i>"Show Rates"</i> shows how the rates are calculated.

---

## Need of Unit Testing :

- Later in future if someone wanted to make changes (such as changing the rates of Taxi) then to make sure that the code would be working properly we do unit testing by giving the program various sample cases and it's expected outputs such that all of the logic of the program is covered.

- By doing this we can identify any future bugs which may show up when working with the program.

## How to do Unit - Testing ? 

### Enter <i>Mocha and Chai !!</i>

- [Mocha](https://mochajs.org/) is a JavaScript test framework running on Node.js and in the browser and does asynchronous testing . Mocha tests run serially, allowing for flexible and accurate reporting, while mapping uncaught exceptions to the correct test cases.

<u>How to install mocha</u> : `npm install mocha`

- `describe` : Helps us to group the various tests.
- `it` : Runs the actual tests.

---

- [Chai](https://www.chaijs.com/) is a BDD / TDD assertion library for node and the browser that can be paired with any javascript testing framework.

<u>How to install chai</u> : `npm install chai`

- Chai is used to makes assertions with various data types (array , string , integer etc) using `should` , `expect` etc.

## Steps :

- Create a folder called `test` which will contain all of the `example_test.test.js` files of the various test we want to run.

- In `package.json` create a new key (if it does not already exists) named `scripts` and in it write `"test : mocha"` and give `"start : node app.js"` so that mocha runs every test present in the test folder.

- Write `npm run test` in the terminal to start the tests . :)

- In the terminal we will be shown all of the passing and failing test cases along with the expected and actual (outputted) answers.
The two ways in which case there are failing cases are :
<t>1) We deliberately changed the logic of the code in which case we also have to change the test cases accordingly.
<t>2) If by some mistake our code gets changed which results in the error then we can rectify that error.

- To run the tests individually we can install the `mocha sidebar` 

---

## Code Coverage

- Code coverage is a metric that can help us understand how much of our source is tested. It's a very useful metric that can help us assess the quality of our test suite.

- Some useful links to know more about Code Coverage :
<t>1) [Atlassian Article](https://www.atlassian.com/continuous-delivery/software-testing/code-coverage)
<t>2) [StackOverflow](https://stackoverflow.com/questions/195008/what-is-code-coverage-and-how-do-you-measure-it)

### Code Coverage using `nyc` :

- Run `npm install nyc`
- Write `"cover" : "nyc mocha"` in the <i>"scripts"</i> of `package.json`.

### Code Coverage in IDE :

- To check code coverage in IDE itself install `Code Gutters`

- Write `"cover" : "nyc --reporter=lcovonly mocha"` in the <i>"scripts"</i> of `package.json`. 

---

## To test GET and POST Methods :

- Write `npm i request` in terminal to install it.
- More about [`request`](https://www.npmjs.com/package/request)
