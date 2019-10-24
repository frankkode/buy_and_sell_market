# [buy-and-sell-market](http://buy-and-sell-market.herokuapp.com/)

- DEPLOYED APP CAN BE FOUND HERE: http://buy-and-sell-market.herokuapp.com/
- CODE CAN BE FOUND HERE: https://github.com/frankkode/buy_and_sell_market

INTRODUCTION:
In this project I have created a FREE MARKET website to demonstrate my understanding of the flask-python microframework and mongodb databases. From a user perspective the website should allow them to view, add and edit posts and  also to view other peoples posts on the main page 
## UX
This project is the assessment of the flask-python modules for the Full Stack Software Development  at Code Institute. I chose to create a web application that allows users to benefite from it. Each user should be able to Create, Read, Update, and Delete (CRUD) their own posts. Users can also be able to contact each other for free and features for a fee.

User Stories
"As a user, I want:"

to view the site on my preferred device (mobile, tablet, desktop).
to create my own account
to update my posts
to create posts
to edit my own posts
to delete my own posts
to sell my items free of charge
to view posts of others

## Technologies Used

### Languages

- **[HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5)** was used to set up the templates for the site.
- **[CSS3](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS3)** was used to style the site content.
- **[JavaScript](https://www.javascript.com/)** 
I have used Javascript in the add/edit post forms to power the logic behind the 'Add information' and 'Remove information' buttons. I have also used this to create a validation error for the Materialize select component 
JS has also been used to power the sliding side menu action on smaller screen sizes
was used to initialise some of the Materialize elements and ensure that they worked correctly.
- **[Python](https://www.python.org/)** was used to write the app's logic.
- **[MongoDB](https://www.mongodb.com/)** was used as the database .


### Frameworks/Libraries

- **[Flask](http://flask.pocoo.org/)** was used to create routes and render the HTML templates.
- **[Materialize](https://materializecss.com//)** was used as the basis for the site's design and responsiveness.


### Tools

- **[Git](https://git-scm.com/)** was used for version control.
- **[Heroku](https://www.heroku.com/)** was used to deploy the project.
- **[MongodbAtlas](https://docs.atlas.mongodb.com)** was used to set up the database.
- **[Balsamic](https://balsamiq.cloud/spsngzf/pe97rf5/r2278)** was used to create the wireframes.
- **[unittest](https://docs.python.org/2/library/unittest.html)** was used for automated testing of the Python code.


## Testing

### Code Validity

- I used the [W3C Markup Validation Service](https://validator.w3.org/) to check the HTML 
- I used [W3C CSS Validation Service](https://jigsaw.w3.org/css-validator/) to check the CSS. 
  The W3C Markup Validation Service gives error messages for Flask Jinja code in the HTML files.
- i used pip8 online formatter (http://pep8online.com/) to check python indentation


### Automated Tests

I conducted automated testing of the app routes with unittests, and the tests are in test_app.py at the root directory. Run the tests by entering ```python3 test_app.py``` in the terminal.
![Wireframe / Site Diagram](static/images/test.png "test") 

  
### Manual Tests

I conducted manual tests of the application as follows:

1. Cross-browser and Device Compatibility
    1. Test the app on Chrome, Edge, Firefox Opera and Safari browsers to ensure that it works on all of them.
    2. Test the app on a desktop, laptop, tablet and smartphone to ensure that it works on all devices.

2. Responsiveness
    1. View the app in responsive mode with Chrome Developer Tools to ensure that the size and position of elements adjusts correctly.
    2. View the app on a desktop, laptop, tablet and smartphone to ensure that it displays correctly.

3. Registration
    1. Navigate to the registration page.
    2. Enter a username and password.
    
    3. get login form
     
4. Login
    1. Navigate to the login page.
    2. Enter a correct username and password.
    
    3. Ensure that I can add recipes and edit and delete posts submitted under that username, and that I can't edit or delete other users' posts.
    5. Ensure that, when I click on the "My posts" link in the navbar, I see the list of my posts and no others.
    6. Click on the Logout link in the navbar and ensure that I'm logged out.
    7. Enter a username that's not in the database and a password.
    8. Ensure that I see a message saying that I've entered an incorrect username/password combination.
    9. Enter a username that's in the database and an incorrect password.
    10. Ensure that I see a message saying that I've entered an incorrect username/password combination.

5. Adding posts
    1. Click on the "Add item" link in the navbar.
    2. Ensure that the form appears correctly.
    3. Attempt to submit the form with required fields blank and ensure that I'm prompted to fill them.
    4. Submit a fully completed form.
    5. Click on the link to the new post on the main page of posts insure that all information was submited correctry.
    6. Ensure that the page showing that post loads correctly, with all entered details appearing.
    7. Ensure that all the posts details have been saved in the database.


 
7. Viewing categories
    1. Click on the 'category' link in the navbar.
    2. Ensure that all posts in the database are listed on the page that loads.
    3. Click on each post in the list in turn
    4. Ensure that all the posts details are displayed correctly on the page that loads.

8. Editing post
    1. Click on the Edit button at the bottom of a post displaying in your account.
    2. Ensure that the form for editing the post loads.
    3. Edit the post details.
    4. Click the Submit button.
    5. Ensure that the post reloads and the edits have been saved to the database.
    6. Repeat for all posts.

9. Deleting posts
    1. Click the Delete button at the bottom of the post on your acount page.
    2. Ensure that a warning button appears, along with  cancel button 
    3. Click Cancel.
    4. Ensure that the page reloads correctly.
    5. Click the Delete button again.
    5. Click Confirm.
    6. Ensure that the post is deleted from the database.
    7. Repeat for all posts.

## WIREFLAME BY BALSAMIQ
### Main Page
![Wireframe / Site Diagram](static/images/calling-page.png "main page")
### Edit Item
![Wireframe / Site Diagram](static/images/edit-post.png "edit and my items")
### Contact Us
![Wireframe / Site Diagram](static/images/contact-us.png "contact us")
### About us
![Wireframe / Site Diagram](static/images/about-us.png "about us")
### Database schema
![Wireframe / Site Diagram](static/images/data-base.png "data-base schema")

## Deployment

I deployed the project on Heroku as follows:
1. Create a new app on Heroku and name it buy-and-sell-market.
2. Create a Heroku remote.
Deploy to Heroku using git:
$ git add .
$ git commit -m "commit message"
$ git push heroku master
3. Ensure that the project included a Procfile and requirements.txt.
4. Push the project to the Heroku remote.
5. Start a web process by entering the following in the terminal: ``heroku ps:scale web=1``
6. Set the IP to 0.0.0.0 and the PORT to 5000 in the Heroku config vars.
7. Set the MONGO_URI,DATABASENAME,EMAIL,PASSWORD environment variable in the Heroku config vars.
8. Restart all dynos.
9. Open the app on Heroku and check to ensure that it's working correctly.


### Running the Code Locally

Steps 1-6 were copied from [here](https://github.com/frankkode/buy_and_sell_market)
1. Under the repository name on GitHub, click Clone or download.
2. In the Clone with HTTPs section, click the icon beside the URL to copy the clone URL for the repository.
3. Change the current working directory to the location where you want the cloned directory to be made.
4. Type git clone, and then paste the URL you copied in Step 2.
5. Press Enter. Your local clone will be created.
6. Set up a virtual environment.
7. Install the packages in requirements.txt by typing pip install -r requirements.txt in the CLI.
8. Set the IP address to 127.0.0.1 and the PORT to 5000.

## App Image
### main page
![Wireframe / Site Diagram](static/images/main-page.png "main page")
### Edit Post 
![Wireframe / Site Diagram](static/images/edit-post-app.png "edit post")
### Sign up Form
![Wireframe / Site Diagram](static/images/signup.png "signup")
### Login Form
![Wireframe / Site Diagram](static/images/login.png "login")
### About us
![Wireframe / Site Diagram](static/images/about-us-app.png "about us")
### Contact us
![Wireframe / Site Diagram](static/images/contact-us1.png "contact us")
### Contact us
![Wireframe / Site Diagram](static/images/contact-us2.png "contact us")
### Edit item
![Wireframe / Site Diagram](static/images/post-and-edit-form.png "post and edit form")

## Credits

### Media&code
## The website images were taken from the following sources:

- contact and about us background  images  was taken from: (https://unsplash.com/)
- pics on items was taken from : Google Image Search (https://www.google.com)

- contact form was taken from flask-mail


### Acknowledgements
- Many thanks to my mentor Anthony Ngene (https://app.slack.com/team/UDNCUURHU) for his helpful feedback and support during this project
- Many thanks to CODE INSTITUTE tutorial team mainly Niel,Haley and Samantha 