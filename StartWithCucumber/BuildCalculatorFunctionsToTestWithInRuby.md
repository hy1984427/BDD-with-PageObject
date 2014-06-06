# Build calculator functions to test with in Ruby

To start with, we need to create "Cucumber" folder with `mkdir Cucumber` in "Terminal".

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateCucumberFolder.png "Create Cucumber Folder")

Open "Cucumber" folder and create "lib" folder to hold calculator functionality file.

`cd Cucumber`

`mkdir lib`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateLibFolder.png "Create lib Folder")

Now, we need to open "lib" folder and add a file "calculator.rb".

`cd lib`

`touch calculator.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateCalculatorRB.png "Create calculator.rb")

Then edit it as following and save:

<pre><code>class Calculator
    def push(n)
        @args ||= []
        @args << n
    end

    def add
        @args.inject(0){|n,sum| sum+=n}
    end

  	def divide
        @args[0].to_f / @args[1].to_f
    end
end</code></pre>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditCalculatorRB.png "Edit calculator.rb")
