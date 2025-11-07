# Compiling-CoreProtect

Want the latest version of [CoreProtect](https://coreprotect.net)? Can't afford [$5USD](https://www.patreon.com/posts/coreprotect-v23-140238000)? Know what [Github](https://github.com/PlayPro/CoreProtect) is?
Then this is the guide for you!

1. Download JDK 11
2. Download Maven
3. Download Git
4. ```git git clone https://github.com/PlayPro/CoreProtect.git```
5. Edit ```pom.xml``` line 7 to: ```<project.branch>development</project.branch>```
6. Edit ```NetworkHandler.java``` line 88 to: ```if (remoteKey.length > 1 && remoteKey[1].equals("0") && remoteKey[0].length() > 1) {```
7. Edit ```VersionUtils.java``` line 107 to: ```return !isBranch("edge") && !isBranch("coreprotect") && !isBranch("development") && !validDonationKey();```
8. Compile with ```mvn clean install```
9. Move ```\target\CoreProtect-23.x.jar``` into your servers plugin folder
10. Edit ```config.xml``` in the plugin folder line 4 to: ```donation-key: eatcevapi```
11. Enjoy the paid donator edition! Note that the command ```migrate-db``` does not work.
    
![Paid](https://i.imgur.com/haHDF7z.png)

Steps 6, 7 & 10 are not really required but will remove any community edition annoyances.
