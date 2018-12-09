Steps to create Zuul API Gateway:
1. Add netflix-zuul dependency
2. Add @EnableZuulProxy annotation in the SpringBootApplication main class
3. Register this gateway in the registry server (@EnableDiscoveryClient)
4. Add Eureka Client default zone - eureka.client.serviceUrl.defaultZone=http://localhost:40002/server-naming/eureka
5. Since my Eureka Registry server is using a custom port, this Eureka client must specify it in the config by -  eureka.client.instance