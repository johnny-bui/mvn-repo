My first maven repository in github
Thanks to Matt's Blog for this post: 

http://blog.rueedlinger.ch/2012/09/use-github-as-maven-remote-repository/

Add this repo in to your `repositories`-Tag in `~/.m2/settings.xml` to use my repo.

    <repository>
      <id>com.github.verylazyboy</id>
      <url>https://github.com/verylazyboy/mvn-repo/raw/master</url>
      <!-- use snapshot version -->
      <snapshots>
          <enabled>true</enabled>
          <updatePolicy>always</updatePolicy>
      </snapshots>
    </repository>


To use the maven plugins in my repo:

    <pluginRepository>
      <id>com.github.verylazyboy</id>
      <url>https://github.com/verylazyboy/mvn-repo/raw/master</url>
      <!-- use snapshot version -->
      <snapshots>
          <enabled>true</enabled>
          <updatePolicy>always</updatePolicy>
      </snapshots>
    </pluginRepository>

All my plugins are in beta. And even if I release it, use it with your own risk. The artifact sablecc and objectmacro
are just a re-distribution of the binary files in the original project sablecc (http://sablecc.org). Thank you, 
Étienne Gagnon for SableCC and ObjectMacro. 
