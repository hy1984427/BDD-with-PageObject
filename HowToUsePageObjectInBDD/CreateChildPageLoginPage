# Create child page - login page

And "login.rb":

`touch login.rb`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/CreateLoginRB.png "Create login.rb")

We need to copy following content to "login.rb" and delete them from "base_page.rb".

<pre><code>class Login < Page

	def loginAs (username,password)
		clickElementBy("id", "nav-signin-text")
		inputToElementWith("id", "ap_email", username)
		inputToElementWith("id", "ap_password", password)
		clickElementBy("id","signInSubmit-input")
	end

end
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditLoginRB.png "Edit login.rb")

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/EditLoginRBBasePageRB.png "Remove methods from base_page.rb")
