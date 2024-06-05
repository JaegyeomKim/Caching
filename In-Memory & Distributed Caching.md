# What is In-Memory caching & Distributed caching?

In-Memory Caching
- It's the normal way of caching. In this cache is stored in the memory of a single server which is hosting the application.
- It can be implemented with the IMemoryCache interface in ASP.NET core.

Distributied Caching
- When you want to handle caching outside of your app. A different srever is used for store cached data.
- It can be implemented with the help of Redis Cache.

* Redis is an open-source, highly replicated, performant, mon-relational kind of db and caching server.
  ![image](https://github.com/JaegyeomKim/Caching/assets/77129961/cbbec469-0661-4843-b4a7-69d56b3e7515)


# When to use In-Memory caching & Distributed caching?

In normal cases where the app size is small, use in-memory cache.
However, where the app is very big or it's a microservice based architecture, then use distributed caching
