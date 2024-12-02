# **Tech Stack for Champion Manager Idle Bot**

## **1. Backend Language and Frameworks**

### **Primary Language**

- **C# (using .NET Core)**
  - **Why C#?**: C# is well-suited for performance-intensive tasks, making it ideal for simulating battles, handling concurrent user actions, and managing guild features. The **Discord.Net** library is a mature, powerful choice for building Discord bots, providing rich features and strong community support.

### **Framework**

- **ASP.NET Core** can be used if you decide to implement REST APIs to interact with the bot for storing data or building an external user interface.

## **2. Discord Library**

### **Discord.Net**

- This library allows easy integration with Discord, providing capabilities for creating commands, managing user interactions, and handling event-driven activities in the bot.

## **3. Data Management**

### **Database**

- **MongoDB**: A document-based NoSQL database like MongoDB is a natural fit for this type of project. It allows flexibility when storing champion data, player inventories, item details, and guild structures. It’s easy to extend as the game grows, which is useful for adding new champions or items without significant schema changes.
- **Redis**: Redis will be used for **in-memory caching** and **quick data access**. It will store information that needs to be accessed frequently, like player current states, cooldown timers, and match data, significantly improving response time.

## **4. Real-time Processing & Scheduling**

### **Task Scheduling**

- **C# Native Tools**: `Task.Delay()` or **System.Timers** can be used for simple cooldowns and short-term delays (e.g., death timers, item crafting).
- **Quartz.NET**: A robust job scheduling library for managing more complex, recurring tasks. This will be useful for scheduling daily quests, resetting events, and managing guild activities with cron-like precision.
- **Hangfire**: Another excellent option for managing background jobs and delayed tasks, **Hangfire** can be used in combination with Redis for recurring events and cooldown management.

## **5. Game State Management**

### **In-Memory Cache with Redis**

- Redis will act as a **task queue** and in-memory storage for events like cooldowns, death timers, and champion state data. It’s efficient and helps to offload some load from the database for frequently accessed data, keeping latency low.

## **6. Champion Data and Balancing Approach**

### **Custom Champion Values**

- Instead of syncing with Riot’s API, all champion stats, spell values, and items will be stored locally.
  - **Champion Base Stats**: Define core stats (e.g., health, attack damage, abilities) in **JSON files**. This allows for easy modification and balancing without having to dive into the main bot code.
  - **Simplified Spells**: Champion abilities will be tweaked for text-based gameplay, and some complex effects will be generalized to make coding easier and balance manageable.

## **7. User Interface**

### **Web Interface**

- You can create a **React**-based frontend for players to view their champions, stats, inventory, guild status, and leaderboards. This provides an easy and visual way to interact with the game aside from Discord commands.
- Use **ASP.NET Core** for developing APIs that interact with MongoDB to serve data to your React frontend.

## **8. Deployment and Containerization**

### **Docker**

- A **Dockerfile** can be created for the entire bot, allowing easy local deployment and ensuring consistent environments across different systems.
- **Docker Compose**: Use **Docker Compose** to manage all services together, including the C# bot, MongoDB, and Redis instances. This setup will make it easy to manage dependencies during development and later for testing.

## **9. Future Cloud Deployment (Optional)**

### **Cloud Options**

- **Azure**: As .NET Core integrates well with **Azure**, this would be a natural choice for cloud deployment if needed later. Azure provides services like **Azure Cosmos DB** (for MongoDB) and **Azure Functions** for handling event-driven tasks.
- **Kubernetes**: If scaling becomes necessary, **Kubernetes** can orchestrate multiple containers, allowing you to run several instances of the bot for better load balancing.

## **Next Steps for Implementation**

### **1. Initial Setup**

- Set up **Discord.Net** in a C# environment to create the basic structure of the bot.
- Implement **MongoDB** as the main data store, and integrate **Redis** for caching frequently used information.

### **2. Core Features**

- Start by building simple champion selection and battle features, including minion fights and basic spell use.
- Implement **basic timers** for cooldowns and respawn delays using `Task.Delay()`.

### **3. Champion and Combat System**

- Define champions in **JSON files** and build the combat logic for at least one or two champions. Focus on basic attacks and abilities to get the core mechanics working.
- Expand combat to support more champions and different spell interactions.

### **4. Progressive Features**

- Add **task scheduling** using **Quartz.NET** or **Hangfire** for managing more complex events like scheduled guild battles or daily quests.
- As the bot grows, use Redis to manage queued tasks and quick access data.

### **5. User Interface**

- Develop a **React-based web interface** to make viewing champion progress and stats more intuitive.
- Set up APIs with **ASP.NET Core** to serve the front-end data.

### **6. Deployment**

- Create a **Docker setup** for local deployment, ensuring the environment is consistent and ready for easier cloud migration later on.
