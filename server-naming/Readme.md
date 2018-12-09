Steps to create the naming server:
1. Add netflix-eureka-server dependency
2. Add @EnableEurekaServer in the SpringBootApplication main class
3. By default, eureka server will register itself to be discovered by others. Since I'm running a single Eureka server, I will disable this by setting the registerWithEureka = false.
4. I don't need to fetch registry info so I'll turn it off by setting fetchRegistry = false.
5. I will not use the default port 8761 so I need to set the default zone to the custom port (and context path if applicable) so that Eureka will not keep on trying to replicate 8761 which is not used.
