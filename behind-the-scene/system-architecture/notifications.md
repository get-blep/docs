---
description: Blep Notification Service's Backend Architecture
---

# Notifications

Notifications play a vital role in enhancing the Blep user experience by keeping users informed about various activities within the platform. Whether it's updates from their communities, new Bleps, friend activities, or nearby communities, notifications are the lifeline of user engagement. Blep leverages the pub-sub (publish-subscribe) model of **AWS SNS (Simple Notification Service)** to deliver real-time and rapid notifications.

## **Key Components of the Notification Architecture:**

### **1. Notifications Manager**

This component serves as the bridge between the Blep platform and the user's device. It allows users to subscribe to the notification service seamlessly. Users provide their unique device IDs, generated by AWS SNS integrated into the application. The Notifications Manager also manages the delivery of notifications in real-time to users' devices. It triggers notifications for events such as the creation of new Bleps in a user's joined community, acceptance of joining requests by community admins or Blep creators, receipt of follow requests, and the discovery of new nearby communities of interest. To efficiently send notifications to multiple users, the manager employs AWS SNS "topics," managed by the Topics Manager.

### **2. Topics Manager (Create and Subscribe to Topics)**

Topics are key to delivering notifications to specific components of the Blep system efficiently. Each topic is associated with a unique identifier for a component. Blep utilizes the component's name along with its unique system ID to create new topics. The Topics Manager generates topics for various parts of the Blep system that require bulk notification delivery. When a user subscribes to the notification service or updates their device ID, they are automatically subscribed to topics related to the components they are part of. This ensures a seamless and continuous flow of real-time notifications to users.

### **3. Device Manager**

Device IDs are crucial for providing users with personalized and real-time notifications. The Device Manager is responsible for efficiently managing and storing all user device IDs. It ensures rapid retrieval when needed, allowing for a highly responsive notification system. Device IDs serve as the unique identifiers that enable users to receive personalized and real-time notifications, contributing to an enhanced Blep user experience.

In summary, the Blep Notification Service's backend architecture leverages AWS SNS and a well-structured system of managers to provide users with real-time, personalized, and efficient notifications, fostering user engagement and community interaction within the platform.