# Future Frontend Developer Process

## Howdy future friend & developer! Get familiar with our hiring process at COBE:

1. The first step is to solve an assignment. You will find it below with detailed instructions.
2. Then comes the technical meeting with your future team lead and one more team member. 
3. To finalize the process, you will have a short call/meeting with our HR.  

For the assignment, we will provide you with a rough concept and an idea of what the app should do - the rest is up to you. Covering edge cases is NOT a must, but it's a bonus.   
Once you create a repository, please make sure to commit it in iterations with meaningful commit messages, not all at once.      
We will provide you with mockup designs but know that it is not necessary to follow the exact colours or spacings. You can be as creative as you want, just make sure you are consistent. 
I would advise you to read everything first so you get an idea of everything you need to do, and then dive in.   
All necessary information, such as **contentful_access_token** and **space_id**, will be sent to you via email.  
#### Good luck!


The first step is to set up the project and architecture. Using CRA or anything to bootstrap is **forbidden**. Create a webpack (or another desired tool) configuration from scratch.

Once you are done with setting up the project, you should start with the main screen. 

### **Main screen**  

![Screenshot 2022-01-21 at 17 09 44](https://user-images.githubusercontent.com/56973272/150560704-eeeba817-8e9f-4420-be7f-2aabd0c9211c.png)


- As a user, I want to have a top navigation so I can navigate between the homepage and player creating page
- The Player's list should be rendered on the main screen, so the maximum amount of players, at first load, is 10
- At the bottom of the main screen should be a **Load more** button. Clicking on it should load 6 more (API provides 11 overall) so it's okay to load only 11 but logic should cover load 6 by 6 after the first 10
- As a user, I should be able to sort players alphabetically or to do a reset, as it is coming from API
- As a user, I should be able to search the players by name. A basic local search through click is enough. The players' list on the main screen should update once we click the search button 
- As a user, I should be able to delete the entry inside of search, and to reset the view to see all players again

### **Player screen**

![Screenshot 2022-01-21 at 17 34 22](https://user-images.githubusercontent.com/56973272/150564731-dcb0aa7d-2465-44cd-854c-6426d93a5110.png)

*Create a single page just for **Dendi**, the rest should lead to an error*

- As a user, I want to be able to click on Dendi, which should lead me to the Details page
- As a user, I want to be able to **go back** to the previous page
- If I click on any other player except Dendi, I should get an error
- The Details page should have the player's name and description

### **Player creation**

*On this page I should be able to create a new player with all the necessary fields (name, country and country flag, photo, nickname and total earning (use a random number)). For the purposes of this assignment, create yourself as a PRO player and add simple inputs for the user, like where he can enter information to create a player. You don't need to send an actual request to contentful since contentful API is read-only, writing logic*

- As a user, I want to be able to enter all required data for a player
- As a user, I want to be able to click the **Create** button at the bottom of the page to create a mocked user(this will just console log imaginary request)
- As a user I should be able to open the console and see the created user and data I entered
- As a developer, I should be able to see the logic for creating a new user (mutation)

### **General**

- The project should be delivered alongside README.md file where the scripts are documented (project run, tests, etc...)
- Fetch request and mutation should be covered with **unit tests**(**react-testing-library** and **jest** must be used)
- You should deploy the app to a place of your choice and it should be up and running (preferably AWS, but it's not a must)
- **Typescript** is a MUST
- Styles have to be written with **CSS-IN-JS** or **styled-components/emotion**


### **Bonus points**

- Using prettier/linter
- Storybook is up and running
- Atomic design is used for architecture
