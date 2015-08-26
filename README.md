# action_mailer

<h3>Action Mailer allows you to send email from your rails app! <b>WOW!</b></h3>


Once you've created a new rails app, you can generate the mailer similarly to any other controller. 
	
<pre> <code>	rails generate mailer new_mailer_name </code> </pre>


Just like other controllers, mailers use methods and views to structure content, but instead of rendering an HTML page, it fires off a email.

<br>
There are essentially 3 methods that make up any email. 
<ul>
	<li> headers - these are the atributes you want to pass in, name, email, url, etc. </li>
	<li> attachments - any files to send with email. </li>
	<li> mail - the actual text of the email. This can make use any of the headers that you've defined. </li>
</ul>

<b>Full list of user settable attributes</b>
![attr](/readme_images/user_set_attr.png)



<h3><b>Testing</b></h3>
To test your emails send you can use an app like MailCatcher. It runs on a second local server and allows you to see what your recipients will recieve. This is great so you can verify what you;re sending and who its going to.



<br>
<b>Important Notes:</b>

Action Mailer can send emails through an email app such as gmail, mailgun, or others.

Not all clients accept an email formatted with HTML, so it's best practice to create both and HTML and a text email. Action Mailer will automatically generate both.


Action Mailer is intgrateed with Active Job, so you decide when you want to send emails. Either immediately with 'deliver_now' or use 'deliver_later' to set a different delivery schedule.
