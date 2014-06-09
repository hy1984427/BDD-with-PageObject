# Print the browser's title twice

*In "irb", we probably won't see the differnce between the 1st and 2nd, but if we run the script, we will do shortly, we will see the difference.*

Print the browser's title in "Terminal" using `p "Page title is #{driver.title}"`.

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/PrintBrowserTitle1.png "Print Browser Title for the first time")

Then we can wait for browser titile is changed and start with "cheese!"

`wait = Selenium::WebDriver::Wait.new(:timeout => 10)`

`wait.until { driver.title.downcase.start_with? "cheese!" }`

And then print the browser's title again:

`p "Page title is #{driver.title}"`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/PrintBrowserTitle2.png "Print Browser Title for the second time")

