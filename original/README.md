# Environment #
1. JRE (7+)
2. MySQL (5+)
3. Redis
4. Maven (3+)
5. Tomcat (7+)

# Deployment #
1. Set up your MySQL and import [this schema](https://gist.github.com/chaoshxxu/a3cf7004759d41d79eb7)
2. Set up your [Redis](http://redis.io/) server
3. Download [http_client.json](https://gist.github.com/chaoshxxu/7a5deff639ff99475138) to your server disk, and configure it. It tells Virtual Judge how to visit remote OJs
4. Register accounts in remote OJs
5. Download [remote_accounts.json](https://gist.github.com/chaoshxxu/e9dac7eea72d2b781949) to your server disk, and configure it using accounts in step 4
6. Set up your [Maven3](http://maven.apache.org/index.html) environment
7. Clone the whole Virtual Judge [project](https://github.com/chaoshxxu/virtual-judge) and build it by "mvn clean package"
8. Deploy the WAR built in step 7 named "vjudge.war" to your Tomcat
9. Start Tomcat then find the file named "config.properties" in unzipped "vjudge" directory in your Tomcat webapps directory. Configure all the parameters in it, especially including the absolute path of "http_client.json" and "remote_accounts.json".
10. Restart Tomcat, then it should be OK.
