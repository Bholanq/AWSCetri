**Amazon CloudFront** is a **Content Delivery Network (CDN)** that delivers your content (websites, APIs, videos, images) to users with **low latency and high speed** by caching it at edge locations around the world.

Instead of every user hitting your origin server (like S3 or EC2), CloudFront:

1. Stores (caches) copies of content at **edge locations**
2. Serves users from the **nearest location**

Result: Faster load times + reduced load on origin
![[Pasted image 20260506141103.png]]

CloudFront - High performance, high scale only for viewer request and response.

