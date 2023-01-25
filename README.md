# Description

Week 5 of the General Assembly Software Engineering Immersive course was dedicated to an introduction to React. At the end of that week, we were assigned a project that consisted in building a React application that consumes a public API.

# Deployment link

https://gael-duchesne-cocktail-mixer.netlify.app/

# Timeframe & Working Team

The timeframe for the completion of the project was two days. We worked in a pair group. Below is the link to my partner’s GitHub repository.

https://github.com/sfladager/Cocktail-mixer

# Technologies Used

- HTML
- JavaScript
- React
- Sass
- Bootstrap
- Axios
- Excalidraw

# Brief

- Consume a public API
- Have several components
- Have a router
- Include wireframes
- Be deployed online


# Planning

We started by searching together for a free, suitable API on the internet and agreed on using TheCocktailDB.com which provides endpoints with quite simple, straightforward data such as cocktail images, descriptions and unique identifiers. This kind of data seemed practical given the short timeframe and the requirements of the project. However, the main drawback of this API is that they don’t provide an endpoint with a list of all the cocktails. They are instead categorised (either by name, identifier, main ingredients etc). For an average user it would sound more practical to have a visual overview of a variety of cocktails on one page, so we planned to find a way to achieve that. We drew our wireframe using Excalidraw (see sketches below).

The main elements of our application are:
- A header with a navigation bar common to our web pages
- A home page with a link to a random cocktail page:
![image](https://user-images.githubusercontent.com/113553373/213205929-84761cd8-7a40-4cf5-97fc-6d15d5d89ab7.png)



- A page with a list of cocktails, a burger menu and a search bar to narrow down the user selection:
![image](https://user-images.githubusercontent.com/113553373/213498549-a2439be9-39d3-480a-bc1f-9e2dee29ec8b.png)


- An error page for wrong routing
One page with only one cocktail displayed at a time with an attached description of the drink:
![image](https://user-images.githubusercontent.com/113553373/213498634-8b5bfc33-6151-457d-8209-cdc520c081e0.png)


- One last page with one single random cocktail using the same design.

We typed some pseudocode together, presented our plan to the instructional team, and got signed-off. We split our tasks in the following way: Shawn suggested to be in charge of coding/styling the cocktail list and the single-cocktail components parts which by the way sounded perhaps a bit more difficult than the rest, so I suggested that I should be in charge of all the other parts of the project (home page, navigation bar, error page, random cocktail page) to balance things out, and we agreed on that.
Shawn created the GitHub repository, and I added my components to his version afterwards.

# Build/Code Process

I started working on the navigation bar and the error components. I used the react router Link navigation tool component and Bootstrap classes to style them:
![image](https://user-images.githubusercontent.com/113553373/213498740-db19d914-b0a5-49b2-af59-eba75952dc0e.png)
![image](https://user-images.githubusercontent.com/113553373/213498819-56ca029a-2bee-4bbe-b417-f18847a9236a.png)


I worked on the random cocktail page following these steps:

- I used a useEffect function that retrieves the data from the API endpoint and stores it in the state. That useEffect function has a dependency of an empty array as second argument, so it runs as the page loads:
![image](https://user-images.githubusercontent.com/113553373/213498868-e8450a39-de1f-4888-85e4-a2517953693c.png)

- The endpoint directly provides a random cocktail data as an object containing an array. So I initialised the object drink to null:
![image](https://user-images.githubusercontent.com/113553373/213498906-df1fc8d6-404b-4a82-8650-09092059f372.png)

- My functional component returns a card (with a title, an image and some text). The key ‘drinks’ contains all the descriptive information, stored as an array of items) so I used a map array method through drink.drinks and destructured the keys that I needed:
![image](https://user-images.githubusercontent.com/113553373/213500050-81ef7599-5349-4e53-957f-fd5bc25ebcb4.png)

- I added a Link button generating another random drink.
To do so, I attached an event listener (click) to this button, triggering a callback function which simply makes a new get request to the same endpoint and sets the data to the drink object state.:
![image](https://user-images.githubusercontent.com/113553373/213499076-db9cc2c2-ccde-4646-a7fd-d9e839a38fb0.png)
![image](https://user-images.githubusercontent.com/113553373/213499161-13313401-3c33-4b02-9b66-f6221ab44f19.png)


Once our parts were finished, I added my components to his version and we both worked on the styling of the merged version.

# Challenges

1- Using React: for me, the main challenge of this project was the contrast between the timeframe (two days) and my short experience with this programming tool. We had only attended a few lessons on React, so it was already a difficult thing to get the routine going on (downloading the proper packages like axios, react router, bootstrap, write all of the functional components, linking then with the right routes in App.js, setting states and using useEffect etc). So the coding part in itself took me a substantial amount of time, even for tasks that I considered to be within my skill range. I overcame this challenge by pushing myself and drawing deadlines for my own parts on which I had to work on.
2- Working with a partner: I’m not used to working within a team. Keeping track of my partner’s work/pace/own challenges was new to me. I overcame this challenge by communicating with Shwan all along the project and I organised my work according to Shawn’s own progression/pace and coding issues so that we could help each other out whenever we faced a hindrance, for more efficient use of our short timeframe.

# Wins

The collaboration with my partner was smooth during this project. I’m really happy with what we presented to the class and what our final project visually looks like.
It was crucial to us to go progressively and not to have an over-ambitious minimum viable product and I think that something we did well was gauging our skills at the planning stage.
We also kept listening to each other’s potential issues/concerns throughout the project and we were able to help each other in an effective way multiple times.

# Key Learnings/Takeaways

Going through this project has made me feel more confident in:

Building a multi-page application using React
Manipulating data from an API
Using Bootstrap libraries
Styling using CSS
Working on a team project

As we were reaching the completion of our project I realised that our final result was a bit different than our initial sketch and it was not so easy to communicate about it with my partner and it also led to some uncertainty from time to time. This is actually one of the major takeaways, I have to work on taking more time on the wireframe and have a more structured/accurate plan to follow, otherwise it can lead to some confusion during the project.

# Future improvements

There are some styling improvements to be made to our project. Especially regarding the list-style page, whose visuals are not exactly consistent with the rest.
The code needs some refactoring and our functions and CSS-classes would need to be more wisely-named.
