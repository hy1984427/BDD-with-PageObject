# Add feature file to test addition in calculator

Create calculator addition feature file as following:

`cd features`

`touch addition.feature`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateAdditionFeature.png "Create addition.feature file")

Edit the feature file to contain following content:

<pre><code>Feature: Addition
	In order to avoid silly mistakes
	As a math idiot
	I want to be told the sum of two numbers

	Scenario Outline: Add two numbers
		Given I have entered <input_1> into the calculator
		And I have entered <input_2> into the calculator
		When I press <button>
		Then the result should be <output> on the screen

		Examples:
		| input_1 | input_2 | button | output |
        | 20      | 30      | add    | 50     |
        | 2       | 5       | add    | 7      |
        | 0       | 40      | add    | 40     |
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/AdditionFeatureFile.png "addition.feature content")
