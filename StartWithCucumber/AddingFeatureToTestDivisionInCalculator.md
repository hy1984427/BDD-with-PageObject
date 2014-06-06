# Add feature to test division in calculator

Create calculator division feature file as following:

`touch division.feature`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateDivisionFeature.png "Create division.feature file")

Edit the feature file to contain following content:

<pre><code>Feature: Division
In order to avoid silly mistakes
Cashiers must be able to calculate a fraction

Scenario: Regular numbers
	* I have entered 3 into the calculator
	* I have entered 2 into the calculator
	* I press divide
	* the result should be 1.5 on the screen
</pre></code>

*The steps in feature with asterisk will be ignored and marked as pass when cucumber runs.*

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/DivisionFeatureFile.png "division.feature content")
