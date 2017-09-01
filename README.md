# Intro To Rails And React

## Objectives

* Discover how to connect services
* Differences between Client Side Apps and Web API Services
* Introduce Rails 5 API mode

## Introduction:

Congratulations we made it to the home stretch of the React and Redux section. Let's take a moment and inventory the skills that we've learned:

1. Building components
2. Connecting components
3. Dynamic forms
4. Component State
5. Redux State 
6. Actions -> Reducers -> Store
7. Connecting components to Redux 
8. Async Actions with Redux Thunk
9. React Router Dom
10. Getting cats from a Cats API

That is a ton of knowledge, so now we need to take all of these skills and build a real application with a backend!!

### Web API App Layer and Client App Layer

When designing applications there are many different ways to build a full stack app. We can use full server side rendering, like we did with our previous Rails' apps using .erb files, we could design a service with no client facing views (similiar to a database service like firebase) or we can design an app in layers that allows for exandable interfaces. Let's assume for a minute that we need to build an application that supplies data for mobile phones, a web browser, an apple watch, Roku, AppleTV, desktop application, and....... some distant client in Norway needs our endpoint for his shpping app. Building an app that just serves static content with Rails and .erb would not be an option, so we need to look at how to build gateway application that allows us to send, create, update and delete (CRUD) data for many unique services. 

To build an app like this we need to build an an API layer for our data. To better understand this lets look at an example. 

![Web API Layer](https://s3.amazonaws.com/learn-verified/api-layer-image.png)

In the photo above we have 2 layers:

1. The Client Layer

    - This is where our clients will view and consume our data we build in the API layer. 
    - Think of this as the V of MVC. 

2. The API Layer

    - This is where most of the app logic will live it will take all of the HTTP requests (GET, POST, PUT, DELETE, HEAD, etc).. and return the needed data as JSON, XML, HTML, etc. 
    - Think of the API endpoints as the C of MVC
    - Since The API endpoint is the entry point, it will need business logic to handle the endpoints and will interact with the business logic (Models, DB, services, etc). 
    - Think of the business logic as the M of MVC

When we start seperating our app out in this manner it allows us to expand our app to meet the needs of more than just a website. So let's start learning how to build an API layer and a client layer.

### Rails 5 API Template

Wait what?? How are we supposed to do this? So we use used a backend for our Cats API lab, but we didn't really go over how that worked. Basically we had an app serving our endpoints and our React app consumed them. In this section of the course we are going to introduce a tool that allows us to create endpoints easily. One of the tools that allows us to do this easily is `Rails 5 API Template`.

To use Rails 5 API Template mode we need to upgrade to Rails 5 ( I would recommend using the current stable release ). 

```
gem install rails
```

To test which version of Rails we have lets run 

```
rails -v 
```

We should see something like 

```
Rails 5.1.3
```

Make sure that our version is at least at Rails 5.1!

Now that we have Rails 5 we should build a small application with it. In the next section we will use a Rails 5 API template generator and build out a small API. 

### Summary 

In this lesson we learned about seperating an application into 2 layers. An API layer to create content that is consumed by a Client Layer (Mobile, Web, TVs, etc..). This allows us to expand our application to multiple services and seperate our applications concerns.

<p class='util--hide'>View <a href='https://learn.co/lessons/intro-to-rails-and-react'>Intro To Rails And React</a> on Learn.co and start learning to code for free.</p>