# Add taking screenshot to the assertion step

In the assertion step, we just need to add one line in "verifyItemAddedShownInShoppingCart" in "buy_book.rb":

`@driver.save_screenshot ("screenshot.png")`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/AddScreenshot.png "Add screenshot")

*The scrrenshot will be named as "screenshot.png" under "Cucumber" folder.*

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/Screenshot.png "Screenshot")
