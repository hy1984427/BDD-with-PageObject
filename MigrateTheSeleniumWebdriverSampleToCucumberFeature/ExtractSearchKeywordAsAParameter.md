# Extract search keyword as a parameter

In "sample.feature", we need to change the step to:

`When I search a "Cheese!"`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleFeatureParameterized2.png "Parameterize Selenium-WebDriver sample.feature")

And in "sample.rb", we need to change the step to:

<pre><code>When /I search a "(.*?)"/ do |keyword|
    element = @driver.find_element :name => "q"
    element.send_keys keyword
    element.submit
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleRBParameterized2.png "Parameterize Selenium-WebDriver sample.rb")
