# Homework 1
For the first homework assignment, we were asked to use Git (from the command line), HTML, CSS, and Bootstrap. I am familiar with all of these though it has been a while since I have started web projects from the ground up. Lately, I've mostly had to use ASP.NET MVC with Razor views. 

* [Assignment page](http://www.wou.edu/~morses/classes/cs46x/assignments/HW1.html)
* [Final website](https://shaynuhcon.github.io/ConnerShayna_CS460/HW1/index.html)
* [Code repo for final assignment website](https://github.com/shaynuhcon/ConnerShayna_CS460)
* [Back to main page](https://shaynuhcon.github.io/)

---

## Setup
There wasn't much for me to setup software/tooling wise. I currently have Visual Studio, Visual Studio Code and [cmder](http://cmder.net/) already installed to my local machine. I've used quite a few command line interfaces before and have stuck with [cmder](http://cmder.net/) for the past couple of years at work and at home. It just looks better than others I have used, plain and simple  (in my opinion, anyway). I am familiar with how Git works and have used it for GitHub and for Visual Studio Team Services (now Azure DevOps) but never for BitBucket. Per the instructions on this assignment, I went with GitHub.  

---

## Git Commands
To start off, I created an empty repository on GitHub called ConnerShayna_CS460 then I just created a local folder by the same name to store local code files. The requirements summary stated that Git operations should be done from command line only so I initialized my code repository locally first using the following commands:

```
cd C:\Source\ConnerShayna_CS460
touch README.md
git init
git config --global user.email "sconner15@wou.edu"
git config --global user.name "Shayna Conner"
```

Then to get my local code to my GitHub repo I ran the following commands:

```
git add -A
git commit -m "first commit"
git remote add origin https://github.com/shaynuhcon/ConnerShayna_CS460.git
git push -u origin master
```

The ```-A``` option in ```git add -A``` just adds all files to staging. There's several different ways of doing this but that's just how I've always done it so it's habit now. After the first push, I made a small change to the README file to run the ```git status``` command then did another add, commit, and push then verified that change made it to my GitHub repo. Then I ran the ```git fetch``` and ```git pull``` commands but my local repo was already caught up. The ```git log``` command shows both commits made (screenshot below):

![git log](gitlog.png)

---

## The Website

I used Visual Studio Code as my HTML/Markdown/CSS editor. Once I figured out what I wanted to make the page about, it was mostly about just getting the components on there. I went with food recipes because that's the first thing that came to my mind when I thought of ```ol``` and ```ul``` lists. Didn't think I needed to get too fancy but I did still want the website to have some actual content.

Here's a screenshot of the home page (index.html) of my website which shows the navbar:

![Home page](homepage.PNG)

The website itself has 4 pages and one CSS style sheet: home page, two recipe pages, and a contact page. Bootstrap was used on all pages and they all have consistent styles and header/navbar components. The home page is a single column layout and the recipe pages are two column layout pages. 

I used the list components on the recipe pages as shown below in the screenshot and code snippet:

![Ordered and unordered list](recipepage.PNG)

```html
<div class="container">
    <div class="row">
        <div class="col-md">
            <b>Ingredients:</b>
            <!-- Unordered list -->
            <ul>
                <li>2 pounds chicken thighs</li>
                <li>4 tablespoons mochiko flour</li>
                <li>4 tablespoons cornstarch</li>
                <li>4 tablespoons sugar</li>
                <li>4 tablespoons shoyu (soy sauce)</li>
                <li>2 cloves minced garlic</li>
                <li>1/2 teaspoon grated ginger</li>
                <li>1/2 teaspoon thinly sliced green onions</li>
                <li>1 tablespoon sesame seeds</li>
                <li>1/2 teaspoon salt</li>
                <li>2 eggs (beaten)</li>
            </ul>
        </div>
        <div class="col-md">
            <b>Instructions:</b>
            <!-- Ordered list -->
            <ol>
                <li>Cut chicken into bite size pieces</li>
                <li>In a bowl, mix together all ingredients except for the chicken.</li>
                <li>Once mixed, mix in the cut chicken</li>
                <li>Marinate for 5 hours or overnight in the refrigerator</li>
                <li>Fry pieces in hot oil until cooked and golden brown</li>
                <li>Serve and eat!</li>
            </ol>
        </div>
    </div>
</div>
``` 

Then I used a table on the contact page as shown below in the screenshot and code snippet:

![Table](contactpage.PNG)

```html
<!-- Table -->
<table class="table">
    <tbody>
        <tr>
            <th scope="row">Email</th>
            <td>sconner15@wou.edu</td>
        </tr>
        <tr>
            <th scope="row">Phone</th>
            <td>555-555-5555</td>
        </tr>
    </tbody>
</table>
 ```

 ---           

## GitHub Pages/Portfolio
Never made a GitHub page so struggled for a few minutes there. Thought I was supposed to create the GitHub page from the master branch of the repository that I've been working off of but I actually needed to create a separate repository where I could edit the content/display of the GitHub page and then enable that feature. Found that information here: https://guides.github.com/features/pages/. Then to link my github.io repository to my code repository, I also enabled GitHub pages for the code repository. This seemed easier than duplicating my HTML/CSS files between both repositories. 