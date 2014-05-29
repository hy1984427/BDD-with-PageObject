# Abstract the setup and tire down steps into features/support/env.rb

To move the setup and tire down steps

<pre><code>Before do
    @driver = Selenium::WebDriver.for :firefox
end

After do
    @driver.quit
end
</pre></code>

into "features/support/env.rb", we need to remove them in "sample.rb". The modified "sample.rb" should look like:

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleRBRemoveSetupAndTireDown.png "Removed the setup and tire down steps in Selenium-WebDriver sample.rb")

Add add them into "features/support/env.rb":

`cd features`

`mkdir support`

`cd support`

`touch env.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/SeleniumWebDriverSampleAssertionResult.png "Selenium-WebDriver sample with assertion Cucumber Result")
