####1.创建pom文件，重度使用spring boot,完整pom.xml

    <?xml version="1.0" encoding="UTF-8"?>
    <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
        <modelVersion>4.0.0</modelVersion>
    
        <groupId>me.iwang</groupId>
        <artifactId>aip</artifactId>
        <version>0.0.1-SNAPSHOT</version>
        <packaging>war</packaging>
    
        <parent>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-parent</artifactId>
            <version>1.3.0.BUILD-SNAPSHOT</version>
        </parent>
    
        <!-- Additional lines to be added here... -->
        <properties>
            <java.version>1.7</java.version>
        </properties>
        <dependencies>
            <dependency>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-starter-web</artifactId>
            </dependency>
            <dependency>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-starter-logging</artifactId>
            </dependency>
            <dependency>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-starter-tomcat</artifactId>
                <scope>provided</scope>
            </dependency>
        </dependencies>
        <!-- (you don't need this if you are using a .RELEASE version) -->
        <repositories>
            <repository>
                <id>spring-snapshots</id>
                <url>http://repo.spring.io/snapshot</url>
                <snapshots>
                    <enabled>true</enabled>
                </snapshots>
            </repository>
            <repository>
                <id>spring-milestones</id>
                <url>http://repo.spring.io/milestone</url>
            </repository>
        </repositories>
        <pluginRepositories>
            <pluginRepository>
                <id>spring-snapshots</id>
                <url>http://repo.spring.io/snapshot</url>
            </pluginRepository>
            <pluginRepository>
                <id>spring-milestones</id>
                <url>http://repo.spring.io/milestone</url>
            </pluginRepository>
        </pluginRepositories>
        <build>
            <plugins>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-compiler-plugin</artifactId>
                    <version>3.1</version>
                    <configuration>
                        <source>1.7</source>
                        <target>1.7</target>
                    </configuration>
                </plugin>
                <plugin>
                    <groupId>org.springframework.boot</groupId>
                    <artifactId>spring-boot-maven-plugin</artifactId>
                </plugin>
            </plugins>
        </build>
    </project>

####2.添加web支持,去除embed支持
            <dependency>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-starter-tomcat</artifactId>
                <scope>provided</scope>
            </dependency>


####3.增加Tomcat Server支持
            <dependency>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-starter-tomcat</artifactId>
                <scope>provided</scope>
            </dependency>


####4.增加spring maven插件，repackage进行servlet 3打包

                <plugin>
                    <groupId>org.springframework.boot</groupId>
                    <artifactId>spring-boot-maven-plugin</artifactId>
                </plugin>

