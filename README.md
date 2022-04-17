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

* User sees app icon in home screen and styled launch screen
* Users can sign up and login
* Users can create groups and view and send messages
* Users can create polls within groups
* Users can view a schedule of their group travel plan
* Users can flow between each of these pages

**Optional Nice-to-have Stories**

* Users can view and mark shared maps within their groups 
* Users can allocate a budget for their group
* Users can see their previous trips and reload if 

### 2. Screen Archetypes

* Login
    * Users can login.
* Register 
   * Users can create a new account and login.
* Feed
   * Users can see the a list of the travel groups that they are in.
   * Users can tap on a group to view details.
* Group Creation
    * Users can invite other users to form a new group
* Group Chat
    * Users can view and send messages with each other.
* Schedule
    * Users can view a schedule that lists events and associated times on the travel plan.
    * Users can add suggestions to the schedule.
* Poll Creation
    * Users can create a poll which other group members can vote on.
    * Polls appear in the chat window


### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Group Chat
* Schedule
* Poll Creation

**Flow Navigation** (Screen to Screen)

* Login
   * Feed
   * ...
* Register
   * Feed
* Feed
    * Group Creation
    * Group Chat
* Group Creation
    * Feed

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
