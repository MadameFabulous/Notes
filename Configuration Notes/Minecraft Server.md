```
sudo apt install openjdk-21-jre-headless
```

Forge Specific Arguments   
```
java -jar {forge_installer.jar} --installServer
```

[Big problem forge - Server-Software / Forge - MineOS Forum (codeemo.com)](https://discourse.codeemo.com/t/big-problem-forge/5762/18)

![[Pasted image 20240308005844.png]]


# Gradle Deprecation Issues for Folia Build
Add the following two directories to the Folia repo instead of creating them on build. This will resolve the Gradlew deprecation error related to the directories not existing.
```
mkdir Folia-API
mkdir Folia-Server
```
