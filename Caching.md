# Caching

# Caching use cases and benefits

![image](https://github.com/JaegyeomKim/Caching/assets/77129961/84532dcc-973b-4d24-b4bd-4971ab72eca7)

Can retrieve the same data from the cache
- reduced latency
- reduce load on the database
- reduce network costs


# Types of caches level
- client cacging: Http caching
- CDN caching
- web server caching
- Database caching
- Application caching (The most important layer)

# Types of caches by Design

Global Cache

![image](https://github.com/JaegyeomKim/Caching/assets/77129961/d04c16e9-60ea-4617-8556-e5b65c758d57)

Distributed Cache

![image](https://github.com/JaegyeomKim/Caching/assets/77129961/06264a20-39ff-428c-9858-e5ddabb78d38)

# Caching Strategies & Invalidation

Write-Around Cache (cache-aside, lazy-loading)
1. try to read the data from the Cache
2. If the data is in the cache, it retrns to client. If the data is not in the cache, make a request to storage
3. get data from storage.
4. Every time user make "write" request, update to the cache

![image](https://github.com/JaegyeomKim/Caching/assets/77129961/2399ebab-8bd0-45f7-bf3f-15ebe4dbc2f2)

Reactive Approach 
- Cache stays slim and contatins data that it really needs
- Straightforward implementation and immediate gains
- Cons: Cache gets filled only after a cache miss, meaning 3 trips.


Write-Through Cache : Proactive approach

![image](https://github.com/JaegyeomKim/Caching/assets/77129961/f41c6f3f-c79b-4a83-a12b-990b213b3e6b)

- Well-synced with the DB, resulting in fewer reads
- Cons: Infrequently-requested data is also written to the cache, resulting in a larger cache
  
Write-Back Cache

![image](https://github.com/JaegyeomKim/Caching/assets/77129961/b497b089-587c-4de6-a07b-58b76130302a)

These kind of strategies are not enough.

![image](https://github.com/JaegyeomKim/Caching/assets/77129961/23564db0-658d-4fb3-b758-d6aec98cbf72)

Keep in mind, that this is a bad practice. In a microservice architecture, each database and cache should only be connected to it's own service.


# Eviction Policies

- Least Recently Used (LRU)
- Least Frequently Used (LFU)
- Last In Frist Out (LIFO)
- Random Replacement (RR)


# When not to use caching?

- Adding a caching layer amkes on difference
- High readomness of requests





ref - https://www.youtube.com/watch?v=bP4BeUjNkXc


