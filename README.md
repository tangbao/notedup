# NoteDup - Duplicate or Migrate Your Evernote / YinXiangBiJi Account

## Quick Start

You need to [download](https://www.openlogic.com/openjdk-downloads) and install JDK 8 or higher version first.

[Download](https://github.com/tangbao/notedup/releases) the latest release of NoteDup, then run

```shell
java -jar notedup.jar
```

Login both of your accounts, give NoteDup the permissions, and then start the migration.

![](/pic/example.jpg)

## Build Your Own

Clone all the codes first.

```shell
git clone https://github.com/tangbao/notedup.git
```

Use JDK 1.8 or newer for the project, and add the following required Libraries:

1. [Evernote SDK for Java 1.25.1](https://mvnrepository.com/artifact/com.evernote/evernote-api/1.25.1) 
2. [Scribe 1.3.5, the simple OAuth Java lib](https://mvnrepository.com/artifact/org.scribe/scribe/1.3.5)
3. [JAXB API 2.3.1](https://mvnrepository.com/artifact/javax.xml.bind/jaxb-api/2.3.1) (JDK 1.8 only)

Obtain [Evernote](https://dev.evernote.com/doc/) / [YinXiangBiJi](https://dev.yinxiang.com/doc/) api key and api secret,
and put them in ```Constants.java```.

Use ```MANIFEST.MF``` for the artifact (i.e., .jar).

## Trouble Shooting

While building your project, if you meet ```java.lang.NoClassDefFoundError: javax/xml/bind/JAXBException```, 
please refer to 
[this link](https://stackoverflow.com/questions/43574426/java-how-to-resolve-java-lang-noclassdeffounderror-javax-xml-bind-jaxbexceptio) 
for more information.

## Features

Using the NoteDup note migration tool, you can quickly and easily migrate your ntoes between Evernote / YinXiangBiJi
accounts, while retaining the content, format, attachments, notebooks, tags, GPS coordinates and original links of each
note and other information in your original account.

Supports Windows, Mac and Linux systems.

- Supports copying notes from
  - one Evernote account to another Evernote account
  - one YinXiangBiJi account to another YinXiangBiJi account
  - an Evernote account to a YinXiangBiJi account
  - an YinXiangBiJi account to an Evernote account
- Multi-threading is supported, and multiple notes can be copied in parallel.
- You can choose to copy only the notes in one or more specified notebooks.
- You can choose to copy only the notes with one or more specified tags.
- Supports resumable transfer with a breakpoint, and automatically skips the successfully copied notes when copying
  again after interruption.
- You can limit the upload data usage to ensure the normal use of your account.


## Disclaimer

Use at your own risk if you are in China and want to migrate to/from an Evernote account
(i.e., the Evernote international version).