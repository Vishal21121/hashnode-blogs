---
title: "Part 1: Introduction to Google Dialogflow: What it is and Why You Should Use it"
seoTitle: "Introduction to Google Dialogflow"
datePublished: Thu Mar 09 2023 02:30:03 GMT+0000 (Coordinated Universal Time)
cuid: clf0hr7e300020alc2n706kzh
slug: part-1-introduction-to-google-dialogflow-what-it-is-and-why-you-should-use-it
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678304143488/0f5bfc97-d05b-4df0-bbb4-d50a143ec582.png
tags: chatbots, dialogflow, coderscommunity, googledialogflow

---

### What is Google Dialogflow?

[Dialogflow](https://cloud.google.com/dialogflow/docs) is a Google-owned framework that simplifies the process of creating and designing an NLP(Natural Language Processing) conversational chat & voice assistant which can accept voice or text data from the Dialogflow console. Dialogflow can decrypt users' input by analysing written words and phrases, or speech.

### Why Use Google Dialogflow?

Nowadays, Websites play a big role in the conversion of potential customers to sales. Businesses have realized that with the addition of chatbots to their web pages, visitors stay engaged for much longer, these chatbots give quick services and also help customers with their doubts.

So, building a chatbot for a business is a must. That's why here comes the need to discuss that what is the exact reason that one should know about Dialogflow. What the primary purpose of that would be..answering FAQs? Providing product information? Booking appointments? Helping build stronger and quicker interactions between the seller and the buyer..the applications are endless.

Dialogflow makes chatbots more human-like. It uses Machine Learning, which will allow your chatbot to keep improving by learning from interactions with clients.

Dialogflow can be deployed on multiple platforms and devices which makes it even more interesting. You will be able to publish high-performance chatbots on Facebook, Teams, Slack, and users will have the choice of utilising it on their computer, phone, or even tablet. On the other hand, you will always be able to keep an eye on your chatbot’s analytics and thus monitor your chatbot’s progress as Dialogflow has a built-in dashboard from which one can visualise all inputs and intents.

### What are the benefits of Google Dialogflow?

Now, if we talk about what are the fields of applications of this tool, we must say **that the applications are endless!** So to narrow our discussion let's modify this question a little bit. To be very precise our topic of discussion would be **why should we use DIALOGFLOW to build a chatbot.**

* ***Customer Service and Support*** - Building chatbots or virtual assistants that can provide customer service and support to users.
    
* ***E-commerce*** \- It is used to build chatbots for e-commerce websites and mobile apps. This helps customers to search for their desired products easily, helps them clear their doubts and also helps in better understanding of the user interface.
    
* ***Education and Training*** - Dialogflow can be used to build chatbots or virtual assistants that can help students with course materials, provide feedback on assignments, and answer questions. Especially in online teaching platforms, this has vast applications.
    
* ***Entertainment*** - Yes, you heard that right! In the entertainment sector also this has shown a massive impact. Entertainment services, such as recommendations for movies, TV shows, music, or games. By understanding user preferences and providing personalized recommendations, these chatbots can provide a unique and engaging user experience.
    
* ***Healthcare*** - We have seen many hospitals use chatbots on their official websites and mobile applications for appointment scheduling. These chatbots can make it easier for patients to access quality healthcare services.
    

So, we can say Dialogflow has vast applications in various fields. Especially, its flexibility and customization options make it a popular choice for businesses and developers alike.

### Terms you need to know to get started with Dialogflow

‘***User****‘* – A user is any human being who uses the chatbot. They can play different roles such as owning the chatbot, developing the bot, or interacting with the same. As long as they are human, they are termed ‘users’. 

***Text/Voice(Input)*** – These are the modes used to communicate the input or the output. The user interacts with the bot through text or voice. The text would be anything that is typed into the chatbot window and the voice would be any message spoken into the chatbot window.

Different chatbots support different inputs/outputs. Though it is very common to use text since it does away with issues of microphone access, noisy surroundings, diction issues, etc., it is becoming increasingly popular for bots to support both.

***Agent*** – An agent is another term used to refer to the chatbot. This has been discussed below in detail.

***Expressions*** – Expressions/Training Phrases are the dialogues/utterances that people say when they interact with a bot. They are often in the form of a question. For example – 

*“Is this product available in your store?”*

*“Can I change my appointment time?”*

*“Where is my order?”*

One of the first rules to accept when working with Expressions in Chatbot Development is that the same thing, can and will be said in different ways.

See our three dialogues above. Let’s rephrase them:

*“What are the available products in your store?”*

*“Change my appointment time.”*

*“My order is late.”*

Different people say the same things in different ways. It is, therefore, very important to predict/collate a set of Expressions (often referred to as FAQs), when you are training your chatbot to answer them. These FAQs will be laying the groundwork when you start developing your bot.

***Intent* –** ‘Intents’ are how a chatbot understands Expressions. 

We just saw how varied Expressions can be while still meaning the same thing. This *meaning* is termed as an *Intent*, wherein we extract what the user i*ntends* to say through his/her Expression. 

It is the simple process of grouping expressions into their one meaning, thereby making it easier to program.

Let’s determine an Intent from the following Expressions in the following example:

*“Are you closed on Sundays?”*

*“What time do you open?”*

*“What are your store timings?”*

All these Expressions want to know about the Store Timings. The Intent can therefore be, ‘*Store Timings*‘.

Ok cool! If it's a little bit confusing let's take an easy example of t-shirt sizes.

Have a look at the following example:

*"XS"*

*"S"*

*"M"*

*"L"*

*"XL"*

These Expressions are all about T-shirt sizes. The Intent can therefore be, ‘*T-shirt Sizes*‘. Well, if you're thinking that if someone writes "Small" instead of "S"...don't worry you can add synonyms too! If you intend to capture the user's intent to buy a particular product, you can add training phrases such as "I want to purchase \[product name\]," "buy \[product name\]," "get \[product name\]," and so on.

By using Intents you don’t have to teach your chatbot how to respond to every Expression. Instead, you can just categorise Expressions into Intents that the bot can easily tackle. It is a lot simpler for both the developer and the chatbot this way.

Ultimately, Intents determine the bot’s responses.

***Responses -*** This is the chatbot’s output that is aimed at satisfying the user’s intent.

For example, if the Expressions trigger the Intent ‘Store Timings’, the chatbot can respond by saying, 

*“The store is open every day from 10:00 hrs to 23:00 hrs, except Sundays.”*

**The most accurate responses occur when a proper range of expressions have been correctly grouped into Intents**. Accurate and simple responses are important traits of a good chatbot.

***Entities*** *-* ‘Entities’ are Dialogflow’s mechanism for identifying and extracting useful data from natural language inputs. 

An Intent limits the bot to the scope of the user input. Entities enable it to extract specific pieces of information from your users. If there is any important data you want to get from the user, you will use a corresponding entity. 

***Actions & Parameters* -** These too, are Dialogflow mechanisms. They serve as a method to identify/annotate the keywords/values in the training phrases by connecting them with Entities.

They also provide prompts that extract information from the user. For example:

“When do you want an appointment?”

“What toppings would you like?”

***Annotate* -**The ability of Dialogflow to recognize and link keywords/values between Parameters, Expressions and Entities.

### What does a Dialogflow Console look like?

Dialogflow Console is designed to be intuitive and user-friendly, allowing developers to quickly and easily create powerful conversational AI agents without needing extensive programming experience.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678303287176/214459a7-fbfe-46aa-843e-cb8797086e3c.png align="center")

1. ***Navigation menu:*** The left-hand side of the console contains a navigation menu that provides access to different areas of the console, such as Intents, Entities, Integrations, and Fulfillment.
    
2. ***Agent dashboard:*** The centre of the console displays the agent dashboard, which provides an overview of the agent's performance, training status, and recent interactions with users.
    
3. ***Intents:*** The Intents section allows you to define the different intents that your agent can handle, along with the corresponding training phrases and responses.
    
4. ***Entities:*** The Entities section allows you to define the entities that your agent can recognize, along with the possible synonyms and reference values for each entity.
    
5. ***Integrations:*** The Integrations section allows you to connect your agent with different messaging platforms, such as Google Assistant, Facebook Messenger, and Slack.
    
6. ***Fulfillment:*** The Fulfillment section allows you to configure the backend logic that processes user requests and generates responses.
    
7. ***Test Console:*** This is the best part! The Test Console allows you to simulate user interactions with your agent and test its responses in real-time.
    

### How to create an account on Dialogflow?

1. Go to [https://dialogflow.com/](https://dialogflow.com/)
    
2. Click ‘Go to console’ in the top right corner.
    
3. Login with a Gmail account when prompted.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678300447281/4d8dc9f0-5be0-4601-a3b6-752a548606d2.png align="center")
    

### What is a Dialogflow Agent?

A [Dialogflow agent](https://cloud.google.com/dialogflow/es/docs/agents-overview) is merely another term used to refer to the chatbot. We can say that a Dialogflow agent is similar to a human call centre agent.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678300500028/71ef9783-7b9a-4cb8-9c4b-99f1a4f3f450.png align="center")

While using Dialogflow, you will find that many people start by asking you to ‘name the agent.’ This just means giving your chatbot a name, so even in this context, it's the same.

Now let's create an agent to get a clear insight into the Dialogflow UI. The first thing you’ll need to do is log in to DialogFlow. To do that, go to [https://dialogflow.cloud.google.com](https://dialogflow.cloud.google.com) and log in with your Google Account and if you don't have an account on Dialogflow create one.

Once you’re logged in, click on ‘Create Agent’ and give it a name.

![Dialogflow Interface: Creating an Agent ](https://cdn.hashnode.com/res/hashnode/image/upload/v1678298087352/d9b60b2b-31e6-4e42-b31c-c8450b9de126.png align="center")

Sometimes people say ‘agent’ when referring to the processing module within the application that enables discussions with the chatbot. And sometimes, it is another way to refer to the bot since it functions ‘like a support agent’. The context will always be clear enough for you to know what they mean.

Now, the creation of our agent would be the very first step of making a chatbot using Dialogflow. After creating this agent we will try to create a fully functional chatbot and also see how it helps to grow a business in every aspect.

### Coming up next

1. Understanding Dialogflow Agents
    
2. Designing Conversational Flows with Dialogflow Intents
    
3. Creating Dialogflow Entities for Accurate Intent Recognition
    
4. Dialogflow Fulfillment: How to Build Custom Actions for Your Agent
    
5. Integrating Dialogflow with Third-Party APIs
    
6. Best Practices for Dialogflow Development
    

I hope the discussion we had so far helped you to get an idea about what Dialogflow is and for which purpose it is used.

In conclusion, I hope you found this article informative and useful in a basic understanding of Dialogflow. However, this is just the beginning of what I have to share with you on this topic. In the next part of this series, we'll delve deeper into the creation of bots and provide even more insights and tips. So stay tuned and be sure to check out our next article.

Thank you for reading!