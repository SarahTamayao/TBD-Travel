Original App Design Project - README Template
===

# TBD: Travel App

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
TBD allows users to coordinate group plans and trips through its combination of real-time chat, group polls, and shared map and calendar.

### App Evaluation
- **Category:** Travel/Social Networking
- **Mobile:** This application would be a mobile-first app. A desktop app version may be built in the future.
- **Story:** Allows users to create group chats that can help coordinate travel plans. Members in a group can vote  on or suggest travel decisions, which are then added to a running schedule. 
- **Market:** This application would be geared towards a young adult audience, but could be used by anyone who is looking to connect with friends through travelling.
- **Habit:** This app could be used at different frequencies based on how often they travel. It would mostly likely be used throughout a week to plan the weekend, and during vacation times  
- **Scope:** This app would start as an app used between existing friend groups and help with coordination, but could grow to help users to offer suggestions and help people find new groups. 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* Users can sign up and login


### 2. Screen Archetypes

* Login
    * Users can login.
* Register 
   * Users can create a new account and login.


### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Group Chat



## Wireframes
[Add picture of your hand sketched wireframes in this section]
<img src="YOUR_WIREFRAME_IMAGE_URL" width=600>

### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 

### Models
**Users**
| **Property** | **Type** | **Description** |
|--------------|----------|-----------------|
|userID | String | unique ID for each user
|username | String | name associated with unique user |
|password | String | password used for authentication |


**Messages**
| **Property** | **Type** | **Description** |
|--------------|----------|-----------------|
| content | String | actual text to be sent |
| author | String | username of User sending message |
| createdAt | DateTime | date when message is sent |


**Group Chats**
| **Property** | **Type** | **Description** |
|--------------|----------|-----------------|
| users | Pointer to User | list of all included users |
| messages | String | messages sent in groupchats |

**Polls**
| **Property** | **Type** | **Description** |
|--------------|----------|-----------------|
| question | String | description of voting question |
| options | Object | object of options for poll |
| optionCount | Number | count of votes for each option |

**Schedules**
| **Property** | **Type** | **Description** |
|--------------|----------|-----------------|
| event | String | description of activity |
| time | DateTime | date of event occurrence |
| createdAt | DateTime | time event was created |
| authorID | Pointer to User | User who created event |
| isAdopted | Boolean | True if event is confirmed by vote |

### Networking
* Login
    * (Read/GET) Authenticate user if they log in
* Register 
   * (Create/POST) Create new user if they sign up
* Feed
   * (Read/GET) Query all groups that user is a part of
* Group Creation
    * (Create/POST) Create new group chat with added users
* Group Chat
    * (Read/GET) Query previous messages
    * (Create/POST) Post a new messages to send
* Schedule
    * (Read/GET) Query events for current schedule
    * (Update/PUT) Add new event to schedule 
* Poll Creation
    * (Read/GET) Query polls in chat with proposal, options, and current votes for each
    * (Update/PUT) Add numbers for new votes

GIF of storyboard: 

<img src="http://g.recordit.co/PpGCSsn2Ky.gif" width=250><br>

GIF of Login and Register:

http://g.recordit.co/4ktcf6CPmR.gif

<img src="http://g.recordit.co/4ktcf6CPmR.gif" width=250><br>

GIF of Sample Chat:

<img src="http://g.recordit.co/y6xy0jaPk9.gif" width=250><br>
* Note: still needs to be integrated into main app

GIF of Database Updates for Schedule Feature:

<img src="http://g.recordit.co/nb5V6hhcZS.gif" wdith=250><br>

<img src="<img width="482" alt="Screen Shot 2022-05-08 at 8 54 20 PM" src="https://user-images.githubusercontent.com/92946878/167333638-3c20e802-3a8d-4dac-a2b9-dc21faea4077.png">

<img width="482" alt="Screen Shot 2022-05-08 at 8 53 37 PM" src="https://user-images.githubusercontent.com/92946878/167333663-9b6cb909-68da-4d8f-8e28-ded7b8ffe736.png">

<img width="482" alt="Screen Shot 2022-05-08 at 8 53 53 PM" src="https://user-images.githubusercontent.com/92946878/167333670-6ba10976-06d5-482a-a1d7-54a13fda7e6a.png">


<img width="482" alt="Screen Shot 2022-05-08 at 8 54 34 PM" src="https://user-images.githubusercontent.com/92946878/167333676-6fe31e49-392e-454b-80cb-6a316cee222b.png">

