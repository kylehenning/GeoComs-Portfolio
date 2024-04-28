![GeoComs Logo](public/pwa-192x192.png)

# GeoComs

GeoComs is a location-based chat application that I am actively working on as my Senior Capstone project at GCU. This application provides a space for individuals to digitally connect with peers around them. GeoComs attempts to solve the problem of being able to digitally connect with those who are physically around you.

GeoComs will actively obtain a user's location and use that location to create or join chat rooms. When a chat room is created, the location that the user was at is stored along with the rest of the chat room information. When joining a chat room, GeoComs will find all chat rooms that are within 50 meters of the user and they will be made available to join. Once the user joins a chat room, they will be able to participate in Realtime messaging with other members in the chat room.

GeoComs is hosted on the Contend Delivery Network (CDN) Netlify, and can be accessed at https://geocoms.app.

## Technologies

- Vue.js
- JavaScript
- HTML 5
- CSS
- Supabase
- PostgreSQL
- Vite
- Pinia
- Netlify

I chose Vue.js as my JavaScript framework for this project because of its simplicity and effectiveness in developing code on the client. With this project, I was able to further extend my knowledge of Vue.js by pairing it with the global state management system Pinia. For the backend of the project I chose to use the back-end-as-a-service platform Supabase. While using this platform I learned about row level security (RLS), triggers, and PostgreSQL functions. This platform also allows GeoComs to update data in Realtime.

## Functional Requirements

- **Registration**
- **Login**
- **User Controls**
  - Edit User
  - Promote to Admin
  - Promote to Owner
  - Demote to Chat Room Member
  - Remove from Chat Room
- **Get Location Data**
- **Chat Rooms**
  - Create Chat Room
  - Join Chat Room
  - Leave Chat Room
  - Edit Chat Room
  - View Available Chat Rooms
  - Delete Chat Room
- **Chat Messages**
  - Create Message
  - View Chat Message
  - Edit Chat Message
  - Delete Chat Message

## Non-Functional Requirement

- GeoComs was developed as a Progressive Web Application (PWA). Meaning that it can be installed natively from a WebKit browser and can operate like any platform-specific application.

## Risks and Challenges

While developing this project I understood that I was taking a risk in requiring a user's location to be so important in the overall functionality of the application. This meant that I needed to get familiar with the JavaScript GeoLocation API and understand what constraints I might face when accessing this data. One of the obvious constraints is that when you are given a user's location data you are also given their location accuracy. This data property represented the accuracy in meters that their exact longitude and latitude could be within. This was clearly a challenge that I needed to think about when writing the logic that relies so heavily on a user's distance away from chat rooms. To overcome this challenge I factored in location accuracy into my equation that calculates maximum and minimum latitudes and longitudes within the set 50 meter distance that GeoComs is set at.

## Issues

There are currently no outstanding issues with the GeoComs application.

While my Capstone Project is complete, I do plan on adding further enhancements to the application in the future.
