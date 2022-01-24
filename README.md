# Future frontend developer process

## Howdy future friend/developer, I will explain in few short steps the whole process until being hired so you can know what to expect

1. First you will resolve assingment which you can find here ith detailed instructions
2. Then you will have technical meeting with your future team lead and one more developer
3. Last step is to have short call with HR to finilize process.

We will provide you rough concept and an idea what app should do, rest is up to you. Covering edge cases is not MUST but its a bonus.   
Once you create a repository, please make sure to commit in itterations with meaningful commit messages, not all at once.      
As you are developing, mockup designs are provided, theres no need to follow actual colors, spacings etc.. those stuff are irelevant, be creative and do it as you want, just make sure you are consistent.
I would advice to read everything first to get the idea what needs to be done and then dive in.   
#### Good luck


First step is to setup the project and arhitecture, using CRA or anything to bootstrap is **forbiden**, create a webpack (or other desired tool) configuration from scratch.

Once you are done with setting up project, you should start with main screen. 
### **necessary info**
- CONTENTFUL_ACCESS_TOKEN: wO9AhZ3Ig3-aFGAJ3SEj1vtKJ6DuYhvnwDHTJfsQX5w
- CONTENTFUL_ENVIRONMENT: master
- CONTENTFUL_SPACE_ID: ojpqlra32uom

To access graphi use following url:
*https://graphql.contentful.com/content/v1/spaces/[YOUR_SPACE_ID]/explore?access_token=[YOUR_ACCESS_TOKEN*

### **Main screen**  

![Screenshot 2022-01-21 at 17 09 44](https://user-images.githubusercontent.com/56973272/150560704-eeeba817-8e9f-4420-be7f-2aabd0c9211c.png)


- As a user I want to have top navigation where I can navigate between homepage and player creating page
- Players list should be rendered on main screen, maximum amount of players at first load is 10.
- At the bottom of main screen should be **Load more** button, clicking on it should load 6 more(api provides 11 overal) so its okay to load only 11 but logic should cover load 6 by 6 after first 10
- As a user I should be able to sort players by alphabet or reset back as its coming from API
- as a user I should be able to search players by name. Basic local search on click is enough. Players list on main screen should update once search button is clicked.
- As a User I should be able to delete entry inside search and reset view to see all players again

### **Player screen**

![Screenshot 2022-01-21 at 17 34 22](https://user-images.githubusercontent.com/56973272/150564731-dcb0aa7d-2465-44cd-854c-6426d93a5110.png)

*Create single page only for **Dendi**, rest should lead to error*

- As a User I want to be able to click on Dendi and it should lead me to details page
- As a user I want to be able to **go back** to previous page
- If I click on any other player except Dendi, I should get error
- Details page should have player name and description

### **Player creation**

*At this page I should be able to create new player with all necesary fields(name, country and country flag, Photo, nickname and totalEarning, put some random number). For purposes of this assingment and simplicity, create yourself as a PRO player and just add simple inputs where user can enter info to create player. You dont need to send actual request to contentful since contentful API is read only, writing logic*

- As a User I want to be able to enter all required data for a player
- As a User I want to be able to clikc **Create** button at the bottom of the page to create mocked user(this will just console log imaginary request)
- As a User I should be able to open console and see that created user and data I entered
- as a Developer I should be able to see logic for creating a new user(mutation)

### **General**

- Project should be delivered alongside README.md file where scripts are documented.(project run, tests etc...)
- Fetch request and mutation should be covered with **unit tests**(**react-testing-library** and **jest** must be used)
- App should be deployed to place of your choice, up and running, preferably AWS, but its not a must, up to you
- **Typescript** is a MUST
- Styles has to be written with **CSS-IN-JS** or **styled-components/emotion**


### **Bonus points**

- Using prettier/linter
- Storybook is up and running
- Atomic design is used for arhitecture
