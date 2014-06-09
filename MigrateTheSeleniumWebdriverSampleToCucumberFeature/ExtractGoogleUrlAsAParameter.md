# Extract Google URL as a parameter

In "sample.feature", we need to change the step to:

`Given I opened "http://www.google.com"`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleFeatureParameterized.png "Parameterize Selenium-WebDriver sample.feature")

And in "sample.rb", we need to change the step to:

<pre><code>Given /I opened "(.*?)"/ do |site|
    @driver.get site
end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleRBParameterized.png "Parameterize Selenium-WebDriver sample.rb")
