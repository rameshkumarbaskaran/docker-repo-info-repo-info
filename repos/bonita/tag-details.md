<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:2021.2`](#bonita20212)
-	[`bonita:2021.2-u0`](#bonita20212-u0)
-	[`bonita:2022.1`](#bonita20221)
-	[`bonita:2022.1-u0`](#bonita20221-u0)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.4`](#bonita7114)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:7.13`](#bonita713)
-	[`bonita:7.13.0`](#bonita7130)
-	[`bonita:7.14`](#bonita714)
-	[`bonita:7.14.0`](#bonita7140)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:1aa769ecc00ae2b5c94abf43883615b7c7ecd1f9ce357edf98aeade1d04680c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:df8cf9e551041c9b64a92897b8f09852931bb461310a2bea028079ad1f76ceb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237364091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf789abfc5873ffe54f271066d876604059e84486a3bd32e099ee5be9b65ad5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:19:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:33 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:33 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:19:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:36 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:38 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:38 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:38 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1e620e691728aa8e311d14914ec09747afbb5aaeec58bb9193cba97fc5095c`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebc08e65dc3c4eeacdad4edb70beb111efdbecd2ba5e89264439a6688429d22`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b082f1b87e265e1650946efdffa368afae8fabc94d6052443a1374b67339ad`  
		Last Modified: Fri, 01 Apr 2022 18:20:38 GMT  
		Size: 116.4 MB (116415397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49cefa2fd083cf2bb942e5719e1803efaeb34805e0ce25941398e88c3b2cdd4`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5e8bfa1bea97aea8fd6ee350306915d56359c018acfaf9dcdba64cb07a57fe63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226465705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf86b4639fef9e908a16c016adca244ecf977d8379a40104883adb6ccf6ab9b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:11 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:12 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:13 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 17:40:14 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 17:40:15 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 17:40:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:40:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:40:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:40:22 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 17:40:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:40:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:40:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:40:31 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:40:33 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:40:33 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fcbe56664f56946aa07983e069a083de259a29bfa9ef3858bf4f29f2115946`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4333fdc06cc2fe3bb9e8b58460e52d8f18721e1dd9340fb2efeceb3d6574c62`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8822883e9f9b1dd8295edd1c12f56ae99da080e7c2b60482b62ba9c5ad87390`  
		Last Modified: Fri, 01 Apr 2022 17:42:34 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2eae74ce6c5c1fffd3623b25345c19d17b670976a8ef37a51e930049c58914`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:441d16032bb82790f2bf1bd068c2e14ad0cb1728534112edb792ed82e187e834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233968439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441ae7d5b88efbb9ef80dde708dacedd48f8bd7513ce74f06f5f7b83086b5988`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:17:28 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:17:31 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:17:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:17:43 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:17:45 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:17:47 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:17:49 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:17:52 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:17:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:18:02 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:18:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:18:26 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:18:31 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:18:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:02 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:21 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:23 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:25 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10028fad124e32bc756473a00b8f22e2df94b0731ef00a5962eaf2a5994b799`  
		Last Modified: Fri, 01 Apr 2022 18:23:50 GMT  
		Size: 546.8 KB (546752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bef34d8256bab1909b18380c3a7b42dd9a30fea6371ea571211879d17b46f1`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e079322111e356dd264e0548ccb1632f08ce9c3733978ec1b6a61ae8fee667d`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674c15496e13a6c3071fccd77808f458d2d3e07de9c7ff16a770915ddd896703`  
		Last Modified: Fri, 01 Apr 2022 18:24:00 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b37451ec93d4c6282ae4f1f3c0bb596a7ee8dc13e8c42744d0b5bfc819264a`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:1dc812cf6152a1dbd7dd664e0764032b903cc57c50cff56b29cd4aca4225acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:b8b90f3f8aa8a5a5a0ec94c45447c20d7e2653088cd2f92fadc0fc1adbdfe9c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15d1ac77f073ff34cd4af6e8870392ef73eb84279d0aeb4e35641c72b1ae3d4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:34:48 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:34:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 22:35:07 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 22:35:07 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 22:35:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:09 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 22:35:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 22:35:18 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 22:35:18 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 22:35:19 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 22:35:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 22:35:19 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 22:35:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918014104c9ad49400ad5b9cc91d4bcbae82a73fa5abc7a409bf899c6c43f707`  
		Last Modified: Sat, 19 Mar 2022 22:36:36 GMT  
		Size: 93.7 MB (93654889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dbdd5fbdd128de63982a3bcd426031fd93f653efb545091ac58b78a211fe`  
		Last Modified: Sat, 19 Mar 2022 22:36:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b04accad0ea54945a94640fe15c4f18217ac339546430605562903bb6e198c`  
		Last Modified: Sat, 19 Mar 2022 22:36:23 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ddf332606cb830b506954d33ba501b217b0cf296e237e53ef52a6a9a64c442`  
		Last Modified: Sat, 19 Mar 2022 22:36:22 GMT  
		Size: 1.0 MB (1003224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212fc94ac887dd5a2399140898860c0a998fe2df050fc6e32930fee44eb331d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea58fb34b6055f277ccc1d770336f1a956999418f8c74dcac36d843e5b416d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ddcab601ff797ff8b88340a09e3597f00209e58763e8cf7ed883c7c7dcb87`  
		Last Modified: Sat, 19 Mar 2022 22:36:28 GMT  
		Size: 113.7 MB (113727937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c310e4514d6b20246d217eb5e9eb415ba672947ac5986dff90d60de6cee91c`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8145813d259caf6cd0bea5d1927b07af9b65099efde705c1b7dc4b12dc186c85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282818f0e70e12d2041d5851adc6e578279aaaed15d0a8744828bf7dc42eefed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:09:07 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:09:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 15:09:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 15:09:55 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 15:09:56 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 15:09:57 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 15:09:58 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 15:09:59 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 15:10:00 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 15:10:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 15:10:02 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 15:10:03 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 15:10:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:06 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 15:10:08 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 15:10:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 15:10:29 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 15:10:29 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 15:10:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 15:10:31 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 15:10:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3433408c5fc7f4ae638ee2b5297e626eccb6ef1eaa854483eaa88fe9452b9`  
		Last Modified: Sat, 19 Mar 2022 15:12:08 GMT  
		Size: 85.8 MB (85763156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cf766653b0804c4ca85b92cc0c0069fac5a3f16d050f228364daa9898cdddc`  
		Last Modified: Sat, 19 Mar 2022 15:11:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef7cbb4cb2bf00d122900c6fc72a76a1c4ce7e507619ce147f81ef8541dd2`  
		Last Modified: Sat, 19 Mar 2022 15:11:57 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708c338db08b4e85061950c8cb417d1fdd8d11ab132c8869662712a9d49a856`  
		Last Modified: Sat, 19 Mar 2022 15:11:55 GMT  
		Size: 929.4 KB (929409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ab77260b346ebc4ffb2b67788f195a531157a6a926db586e202224550f95b5`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a15c093ce6465bc4b31ce2c94333e202d3a124194d56bb99438c8074746c3c`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0df29d03ead5b114014be21794a723b2a019942d32b8d108fe3f1f2de09ff`  
		Last Modified: Sat, 19 Mar 2022 15:12:12 GMT  
		Size: 113.7 MB (113727850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4162cb8595bb82ce1922c26bc251eadd27b261925942c84f067f35057191`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:0c8c69d7af8f945591a5d089408490bf52d5bc01ddafc64b7143d5ec6676a8ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7996e14d3d401d9e6a086fdc28917a40774b46df8ec09f0dd2d332cf566df8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:55:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:56:02 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:56:12 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:57:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:57:03 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:57:07 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 20:57:12 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:57:15 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:57:17 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:57:19 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 20:57:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 20:57:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 20:57:25 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:57:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:36 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:57:37 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 20:57:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 20:58:01 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 20:58:07 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:58:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:58:14 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:58:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54998de650aec3ff8c87077551a8a8dedbac826f959645af516a214758030de1`  
		Last Modified: Sat, 19 Mar 2022 21:00:18 GMT  
		Size: 86.6 MB (86557500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80861eb3c1c18c4914806cea4a42cc6605837eb735445fe587096738b931ba`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e3e83293caa8f19217184082aaf48f054162fd676b0bfe80c811db04b5fa07`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e62718fccbad62107b4fe7fd7a9a97a92e26d79914dbc2cd2ce19c1ae3a3e`  
		Last Modified: Sat, 19 Mar 2022 21:00:01 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ad91e85241ec6b752c76025976f23d679c8eda783616cb3d8830044dcb21a`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaebf6593ed9f193fbd8172caa14b34ddf91ceab1a3dc48c01ad9e695794966`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d1d821c92f5f66422e0625adaed7d15289260431916f065c873a51902db85`  
		Last Modified: Sat, 19 Mar 2022 21:00:10 GMT  
		Size: 113.7 MB (113727951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730acde910ffb0b1920533e60561ebf0826b19c5d57baa84709e782722f8539`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:1dc812cf6152a1dbd7dd664e0764032b903cc57c50cff56b29cd4aca4225acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:b8b90f3f8aa8a5a5a0ec94c45447c20d7e2653088cd2f92fadc0fc1adbdfe9c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15d1ac77f073ff34cd4af6e8870392ef73eb84279d0aeb4e35641c72b1ae3d4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:34:48 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:34:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 22:35:07 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 22:35:07 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 22:35:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:09 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 22:35:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 22:35:18 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 22:35:18 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 22:35:19 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 22:35:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 22:35:19 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 22:35:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918014104c9ad49400ad5b9cc91d4bcbae82a73fa5abc7a409bf899c6c43f707`  
		Last Modified: Sat, 19 Mar 2022 22:36:36 GMT  
		Size: 93.7 MB (93654889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dbdd5fbdd128de63982a3bcd426031fd93f653efb545091ac58b78a211fe`  
		Last Modified: Sat, 19 Mar 2022 22:36:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b04accad0ea54945a94640fe15c4f18217ac339546430605562903bb6e198c`  
		Last Modified: Sat, 19 Mar 2022 22:36:23 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ddf332606cb830b506954d33ba501b217b0cf296e237e53ef52a6a9a64c442`  
		Last Modified: Sat, 19 Mar 2022 22:36:22 GMT  
		Size: 1.0 MB (1003224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212fc94ac887dd5a2399140898860c0a998fe2df050fc6e32930fee44eb331d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea58fb34b6055f277ccc1d770336f1a956999418f8c74dcac36d843e5b416d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ddcab601ff797ff8b88340a09e3597f00209e58763e8cf7ed883c7c7dcb87`  
		Last Modified: Sat, 19 Mar 2022 22:36:28 GMT  
		Size: 113.7 MB (113727937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c310e4514d6b20246d217eb5e9eb415ba672947ac5986dff90d60de6cee91c`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8145813d259caf6cd0bea5d1927b07af9b65099efde705c1b7dc4b12dc186c85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282818f0e70e12d2041d5851adc6e578279aaaed15d0a8744828bf7dc42eefed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:09:07 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:09:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 15:09:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 15:09:55 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 15:09:56 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 15:09:57 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 15:09:58 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 15:09:59 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 15:10:00 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 15:10:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 15:10:02 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 15:10:03 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 15:10:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:06 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 15:10:08 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 15:10:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 15:10:29 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 15:10:29 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 15:10:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 15:10:31 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 15:10:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3433408c5fc7f4ae638ee2b5297e626eccb6ef1eaa854483eaa88fe9452b9`  
		Last Modified: Sat, 19 Mar 2022 15:12:08 GMT  
		Size: 85.8 MB (85763156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cf766653b0804c4ca85b92cc0c0069fac5a3f16d050f228364daa9898cdddc`  
		Last Modified: Sat, 19 Mar 2022 15:11:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef7cbb4cb2bf00d122900c6fc72a76a1c4ce7e507619ce147f81ef8541dd2`  
		Last Modified: Sat, 19 Mar 2022 15:11:57 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708c338db08b4e85061950c8cb417d1fdd8d11ab132c8869662712a9d49a856`  
		Last Modified: Sat, 19 Mar 2022 15:11:55 GMT  
		Size: 929.4 KB (929409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ab77260b346ebc4ffb2b67788f195a531157a6a926db586e202224550f95b5`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a15c093ce6465bc4b31ce2c94333e202d3a124194d56bb99438c8074746c3c`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0df29d03ead5b114014be21794a723b2a019942d32b8d108fe3f1f2de09ff`  
		Last Modified: Sat, 19 Mar 2022 15:12:12 GMT  
		Size: 113.7 MB (113727850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4162cb8595bb82ce1922c26bc251eadd27b261925942c84f067f35057191`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:0c8c69d7af8f945591a5d089408490bf52d5bc01ddafc64b7143d5ec6676a8ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7996e14d3d401d9e6a086fdc28917a40774b46df8ec09f0dd2d332cf566df8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:55:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:56:02 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:56:12 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:57:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:57:03 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:57:07 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 20:57:12 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:57:15 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:57:17 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:57:19 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 20:57:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 20:57:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 20:57:25 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:57:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:36 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:57:37 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 20:57:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 20:58:01 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 20:58:07 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:58:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:58:14 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:58:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54998de650aec3ff8c87077551a8a8dedbac826f959645af516a214758030de1`  
		Last Modified: Sat, 19 Mar 2022 21:00:18 GMT  
		Size: 86.6 MB (86557500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80861eb3c1c18c4914806cea4a42cc6605837eb735445fe587096738b931ba`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e3e83293caa8f19217184082aaf48f054162fd676b0bfe80c811db04b5fa07`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e62718fccbad62107b4fe7fd7a9a97a92e26d79914dbc2cd2ce19c1ae3a3e`  
		Last Modified: Sat, 19 Mar 2022 21:00:01 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ad91e85241ec6b752c76025976f23d679c8eda783616cb3d8830044dcb21a`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaebf6593ed9f193fbd8172caa14b34ddf91ceab1a3dc48c01ad9e695794966`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d1d821c92f5f66422e0625adaed7d15289260431916f065c873a51902db85`  
		Last Modified: Sat, 19 Mar 2022 21:00:10 GMT  
		Size: 113.7 MB (113727951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730acde910ffb0b1920533e60561ebf0826b19c5d57baa84709e782722f8539`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:c80f97b2903305a68e006deab8df768079b3518145427f77275239822e674361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:925fbecf5f86d5cae2c3bf402f137c5850dc48d597c4bd1492fca24eb9da4569
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234296474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac5ff240553f524b9bc9c2257bda4b04b677232a1f7918222e274d049cd247`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 01 Apr 2022 18:19:18 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 18:19:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:20 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 01 Apr 2022 18:19:25 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:27 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:27 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:27 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:27 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec89a5d27c97fd5697654d619e71f11dca487abeed4da399ba484618d8562fb`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31cc31dc0e2edb0d37bc6020745d095ba7ef1738644a2add7b3aff50f0510ba`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ed41f555e5d8e3c5df3e4160decc88729049fa669074f8a6a7e1df1542cf2d`  
		Last Modified: Fri, 01 Apr 2022 18:20:22 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1648688f44a0e2fb120535ef6ee1c01f5c3a0a0fd3d332c9038fcb020e6ef43b`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5b761d9ea81e5200e3675f41f85a95f4298c9caef23e0ea6fbe001d3111b9811
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223398072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f778aeb74eaa7e50743d5efbf03cd3c55224a737a534f12146d3cb1b18d914`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:39:38 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:39:39 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:39:40 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:39:41 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 01 Apr 2022 17:39:42 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 01 Apr 2022 17:39:43 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 17:39:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:39:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 17:39:46 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:39:47 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:39:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 01 Apr 2022 17:39:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:39:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:39:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:39:57 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:39:59 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:39:59 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:00 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4751730c21c09d59f824c9c01dc4cce16a8d741be9072c50f5adc8bd08e7d0`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b6fd8b941c9f1003031fd2444c87dd52b8470aa6b6ffebdea19c32590f13e3`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 6.9 KB (6865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bbd297c66d682be8375738a7ff3b97bb7f535a884ff4dd5d479027ea7dd650`  
		Last Modified: Fri, 01 Apr 2022 17:42:13 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92efa6a889c84d53b52cfbf3f19443fe64f95d8ed08127fca1ed6927ad809eea`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:c9b8aee27d6d0b04f0378da479217fd0bbb1637445fe75851d96c31e220c162c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230900826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3302af3ef82bc77dbe259181bea9c86cf9f99661dca8f2768522f42f555847`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:17:28 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:17:31 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:00:28 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:00:31 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:00:36 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:00:40 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 05 Apr 2022 09:00:44 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 05 Apr 2022 09:00:46 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 05 Apr 2022 09:00:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:00:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 05 Apr 2022 09:00:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 05 Apr 2022 09:01:07 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:01:09 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 05 Apr 2022 09:01:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 05 Apr 2022 09:01:37 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 05 Apr 2022 09:01:47 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 05 Apr 2022 09:01:53 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 09:01:55 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 09:02:01 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 09:02:04 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10028fad124e32bc756473a00b8f22e2df94b0731ef00a5962eaf2a5994b799`  
		Last Modified: Fri, 01 Apr 2022 18:23:50 GMT  
		Size: 546.8 KB (546752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeec67f4290af77d7abe73f3cceccab56855c73bfe06ed9c9b6348e9c7ccbb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b7d020423f7956d896b0e5031586166917b5d4190aa859f283d548e85b9406`  
		Last Modified: Tue, 05 Apr 2022 09:06:01 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f5e32b9d73f8ec97dcd1be27f217c35d7500e4aab5bab75ad7740a4526869`  
		Last Modified: Tue, 05 Apr 2022 09:06:09 GMT  
		Size: 113.3 MB (113347832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d0a5a46c1b23c96cf778bfca16623c71a3f17eda4409f2f95e42342d37daa1`  
		Last Modified: Tue, 05 Apr 2022 09:06:01 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:c80f97b2903305a68e006deab8df768079b3518145427f77275239822e674361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:925fbecf5f86d5cae2c3bf402f137c5850dc48d597c4bd1492fca24eb9da4569
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234296474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac5ff240553f524b9bc9c2257bda4b04b677232a1f7918222e274d049cd247`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 01 Apr 2022 18:19:18 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 18:19:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:20 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 01 Apr 2022 18:19:25 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:27 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:27 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:27 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:27 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec89a5d27c97fd5697654d619e71f11dca487abeed4da399ba484618d8562fb`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31cc31dc0e2edb0d37bc6020745d095ba7ef1738644a2add7b3aff50f0510ba`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ed41f555e5d8e3c5df3e4160decc88729049fa669074f8a6a7e1df1542cf2d`  
		Last Modified: Fri, 01 Apr 2022 18:20:22 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1648688f44a0e2fb120535ef6ee1c01f5c3a0a0fd3d332c9038fcb020e6ef43b`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5b761d9ea81e5200e3675f41f85a95f4298c9caef23e0ea6fbe001d3111b9811
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223398072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f778aeb74eaa7e50743d5efbf03cd3c55224a737a534f12146d3cb1b18d914`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:39:38 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:39:39 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:39:40 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:39:41 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 01 Apr 2022 17:39:42 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 01 Apr 2022 17:39:43 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 17:39:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:39:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 17:39:46 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:39:47 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:39:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 01 Apr 2022 17:39:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:39:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:39:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:39:57 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:39:59 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:39:59 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:00 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4751730c21c09d59f824c9c01dc4cce16a8d741be9072c50f5adc8bd08e7d0`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b6fd8b941c9f1003031fd2444c87dd52b8470aa6b6ffebdea19c32590f13e3`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 6.9 KB (6865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bbd297c66d682be8375738a7ff3b97bb7f535a884ff4dd5d479027ea7dd650`  
		Last Modified: Fri, 01 Apr 2022 17:42:13 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92efa6a889c84d53b52cfbf3f19443fe64f95d8ed08127fca1ed6927ad809eea`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:c9b8aee27d6d0b04f0378da479217fd0bbb1637445fe75851d96c31e220c162c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230900826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3302af3ef82bc77dbe259181bea9c86cf9f99661dca8f2768522f42f555847`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:17:28 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:17:31 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:00:28 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:00:31 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:00:36 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:00:40 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 05 Apr 2022 09:00:44 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 05 Apr 2022 09:00:46 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 05 Apr 2022 09:00:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:00:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 05 Apr 2022 09:00:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 05 Apr 2022 09:01:07 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:01:09 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 05 Apr 2022 09:01:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 05 Apr 2022 09:01:37 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 05 Apr 2022 09:01:47 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 05 Apr 2022 09:01:53 GMT
VOLUME [/opt/bonita]
# Tue, 05 Apr 2022 09:01:55 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 05 Apr 2022 09:02:01 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 09:02:04 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10028fad124e32bc756473a00b8f22e2df94b0731ef00a5962eaf2a5994b799`  
		Last Modified: Fri, 01 Apr 2022 18:23:50 GMT  
		Size: 546.8 KB (546752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeec67f4290af77d7abe73f3cceccab56855c73bfe06ed9c9b6348e9c7ccbb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b7d020423f7956d896b0e5031586166917b5d4190aa859f283d548e85b9406`  
		Last Modified: Tue, 05 Apr 2022 09:06:01 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589f5e32b9d73f8ec97dcd1be27f217c35d7500e4aab5bab75ad7740a4526869`  
		Last Modified: Tue, 05 Apr 2022 09:06:09 GMT  
		Size: 113.3 MB (113347832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d0a5a46c1b23c96cf778bfca16623c71a3f17eda4409f2f95e42342d37daa1`  
		Last Modified: Tue, 05 Apr 2022 09:06:01 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:1aa769ecc00ae2b5c94abf43883615b7c7ecd1f9ce357edf98aeade1d04680c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:df8cf9e551041c9b64a92897b8f09852931bb461310a2bea028079ad1f76ceb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237364091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf789abfc5873ffe54f271066d876604059e84486a3bd32e099ee5be9b65ad5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:19:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:33 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:33 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:19:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:36 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:38 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:38 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:38 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1e620e691728aa8e311d14914ec09747afbb5aaeec58bb9193cba97fc5095c`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebc08e65dc3c4eeacdad4edb70beb111efdbecd2ba5e89264439a6688429d22`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b082f1b87e265e1650946efdffa368afae8fabc94d6052443a1374b67339ad`  
		Last Modified: Fri, 01 Apr 2022 18:20:38 GMT  
		Size: 116.4 MB (116415397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49cefa2fd083cf2bb942e5719e1803efaeb34805e0ce25941398e88c3b2cdd4`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5e8bfa1bea97aea8fd6ee350306915d56359c018acfaf9dcdba64cb07a57fe63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226465705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf86b4639fef9e908a16c016adca244ecf977d8379a40104883adb6ccf6ab9b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:11 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:12 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:13 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 17:40:14 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 17:40:15 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 17:40:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:40:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:40:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:40:22 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 17:40:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:40:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:40:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:40:31 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:40:33 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:40:33 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fcbe56664f56946aa07983e069a083de259a29bfa9ef3858bf4f29f2115946`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4333fdc06cc2fe3bb9e8b58460e52d8f18721e1dd9340fb2efeceb3d6574c62`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8822883e9f9b1dd8295edd1c12f56ae99da080e7c2b60482b62ba9c5ad87390`  
		Last Modified: Fri, 01 Apr 2022 17:42:34 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2eae74ce6c5c1fffd3623b25345c19d17b670976a8ef37a51e930049c58914`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:441d16032bb82790f2bf1bd068c2e14ad0cb1728534112edb792ed82e187e834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233968439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441ae7d5b88efbb9ef80dde708dacedd48f8bd7513ce74f06f5f7b83086b5988`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:17:28 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:17:31 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:17:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:17:43 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:17:45 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:17:47 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:17:49 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:17:52 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:17:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:18:02 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:18:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:18:26 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:18:31 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:18:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:02 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:21 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:23 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:25 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10028fad124e32bc756473a00b8f22e2df94b0731ef00a5962eaf2a5994b799`  
		Last Modified: Fri, 01 Apr 2022 18:23:50 GMT  
		Size: 546.8 KB (546752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bef34d8256bab1909b18380c3a7b42dd9a30fea6371ea571211879d17b46f1`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e079322111e356dd264e0548ccb1632f08ce9c3733978ec1b6a61ae8fee667d`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674c15496e13a6c3071fccd77808f458d2d3e07de9c7ff16a770915ddd896703`  
		Last Modified: Fri, 01 Apr 2022 18:24:00 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b37451ec93d4c6282ae4f1f3c0bb596a7ee8dc13e8c42744d0b5bfc819264a`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:1aa769ecc00ae2b5c94abf43883615b7c7ecd1f9ce357edf98aeade1d04680c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:df8cf9e551041c9b64a92897b8f09852931bb461310a2bea028079ad1f76ceb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237364091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf789abfc5873ffe54f271066d876604059e84486a3bd32e099ee5be9b65ad5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:19:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:33 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:33 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:19:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:36 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:38 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:38 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:38 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1e620e691728aa8e311d14914ec09747afbb5aaeec58bb9193cba97fc5095c`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebc08e65dc3c4eeacdad4edb70beb111efdbecd2ba5e89264439a6688429d22`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b082f1b87e265e1650946efdffa368afae8fabc94d6052443a1374b67339ad`  
		Last Modified: Fri, 01 Apr 2022 18:20:38 GMT  
		Size: 116.4 MB (116415397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49cefa2fd083cf2bb942e5719e1803efaeb34805e0ce25941398e88c3b2cdd4`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5e8bfa1bea97aea8fd6ee350306915d56359c018acfaf9dcdba64cb07a57fe63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226465705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf86b4639fef9e908a16c016adca244ecf977d8379a40104883adb6ccf6ab9b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:11 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:12 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:13 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 17:40:14 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 17:40:15 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 17:40:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:40:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:40:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:40:22 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 17:40:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:40:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:40:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:40:31 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:40:33 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:40:33 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fcbe56664f56946aa07983e069a083de259a29bfa9ef3858bf4f29f2115946`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4333fdc06cc2fe3bb9e8b58460e52d8f18721e1dd9340fb2efeceb3d6574c62`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8822883e9f9b1dd8295edd1c12f56ae99da080e7c2b60482b62ba9c5ad87390`  
		Last Modified: Fri, 01 Apr 2022 17:42:34 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2eae74ce6c5c1fffd3623b25345c19d17b670976a8ef37a51e930049c58914`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:441d16032bb82790f2bf1bd068c2e14ad0cb1728534112edb792ed82e187e834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233968439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441ae7d5b88efbb9ef80dde708dacedd48f8bd7513ce74f06f5f7b83086b5988`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:17:28 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:17:31 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:17:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:17:43 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:17:45 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:17:47 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:17:49 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:17:52 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:17:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:18:02 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:18:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:18:26 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:18:31 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:18:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:02 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:21 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:23 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:25 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10028fad124e32bc756473a00b8f22e2df94b0731ef00a5962eaf2a5994b799`  
		Last Modified: Fri, 01 Apr 2022 18:23:50 GMT  
		Size: 546.8 KB (546752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bef34d8256bab1909b18380c3a7b42dd9a30fea6371ea571211879d17b46f1`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e079322111e356dd264e0548ccb1632f08ce9c3733978ec1b6a61ae8fee667d`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674c15496e13a6c3071fccd77808f458d2d3e07de9c7ff16a770915ddd896703`  
		Last Modified: Fri, 01 Apr 2022 18:24:00 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b37451ec93d4c6282ae4f1f3c0bb596a7ee8dc13e8c42744d0b5bfc819264a`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:1dc812cf6152a1dbd7dd664e0764032b903cc57c50cff56b29cd4aca4225acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:b8b90f3f8aa8a5a5a0ec94c45447c20d7e2653088cd2f92fadc0fc1adbdfe9c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15d1ac77f073ff34cd4af6e8870392ef73eb84279d0aeb4e35641c72b1ae3d4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:34:48 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:34:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 22:35:07 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 22:35:07 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 22:35:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:09 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 22:35:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 22:35:18 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 22:35:18 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 22:35:19 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 22:35:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 22:35:19 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 22:35:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918014104c9ad49400ad5b9cc91d4bcbae82a73fa5abc7a409bf899c6c43f707`  
		Last Modified: Sat, 19 Mar 2022 22:36:36 GMT  
		Size: 93.7 MB (93654889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dbdd5fbdd128de63982a3bcd426031fd93f653efb545091ac58b78a211fe`  
		Last Modified: Sat, 19 Mar 2022 22:36:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b04accad0ea54945a94640fe15c4f18217ac339546430605562903bb6e198c`  
		Last Modified: Sat, 19 Mar 2022 22:36:23 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ddf332606cb830b506954d33ba501b217b0cf296e237e53ef52a6a9a64c442`  
		Last Modified: Sat, 19 Mar 2022 22:36:22 GMT  
		Size: 1.0 MB (1003224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212fc94ac887dd5a2399140898860c0a998fe2df050fc6e32930fee44eb331d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea58fb34b6055f277ccc1d770336f1a956999418f8c74dcac36d843e5b416d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ddcab601ff797ff8b88340a09e3597f00209e58763e8cf7ed883c7c7dcb87`  
		Last Modified: Sat, 19 Mar 2022 22:36:28 GMT  
		Size: 113.7 MB (113727937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c310e4514d6b20246d217eb5e9eb415ba672947ac5986dff90d60de6cee91c`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8145813d259caf6cd0bea5d1927b07af9b65099efde705c1b7dc4b12dc186c85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282818f0e70e12d2041d5851adc6e578279aaaed15d0a8744828bf7dc42eefed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:09:07 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:09:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 15:09:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 15:09:55 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 15:09:56 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 15:09:57 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 15:09:58 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 15:09:59 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 15:10:00 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 15:10:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 15:10:02 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 15:10:03 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 15:10:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:06 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 15:10:08 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 15:10:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 15:10:29 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 15:10:29 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 15:10:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 15:10:31 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 15:10:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3433408c5fc7f4ae638ee2b5297e626eccb6ef1eaa854483eaa88fe9452b9`  
		Last Modified: Sat, 19 Mar 2022 15:12:08 GMT  
		Size: 85.8 MB (85763156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cf766653b0804c4ca85b92cc0c0069fac5a3f16d050f228364daa9898cdddc`  
		Last Modified: Sat, 19 Mar 2022 15:11:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef7cbb4cb2bf00d122900c6fc72a76a1c4ce7e507619ce147f81ef8541dd2`  
		Last Modified: Sat, 19 Mar 2022 15:11:57 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708c338db08b4e85061950c8cb417d1fdd8d11ab132c8869662712a9d49a856`  
		Last Modified: Sat, 19 Mar 2022 15:11:55 GMT  
		Size: 929.4 KB (929409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ab77260b346ebc4ffb2b67788f195a531157a6a926db586e202224550f95b5`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a15c093ce6465bc4b31ce2c94333e202d3a124194d56bb99438c8074746c3c`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0df29d03ead5b114014be21794a723b2a019942d32b8d108fe3f1f2de09ff`  
		Last Modified: Sat, 19 Mar 2022 15:12:12 GMT  
		Size: 113.7 MB (113727850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4162cb8595bb82ce1922c26bc251eadd27b261925942c84f067f35057191`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:0c8c69d7af8f945591a5d089408490bf52d5bc01ddafc64b7143d5ec6676a8ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7996e14d3d401d9e6a086fdc28917a40774b46df8ec09f0dd2d332cf566df8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:55:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:56:02 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:56:12 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:57:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:57:03 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:57:07 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 20:57:12 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:57:15 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:57:17 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:57:19 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 20:57:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 20:57:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 20:57:25 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:57:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:36 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:57:37 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 20:57:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 20:58:01 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 20:58:07 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:58:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:58:14 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:58:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54998de650aec3ff8c87077551a8a8dedbac826f959645af516a214758030de1`  
		Last Modified: Sat, 19 Mar 2022 21:00:18 GMT  
		Size: 86.6 MB (86557500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80861eb3c1c18c4914806cea4a42cc6605837eb735445fe587096738b931ba`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e3e83293caa8f19217184082aaf48f054162fd676b0bfe80c811db04b5fa07`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e62718fccbad62107b4fe7fd7a9a97a92e26d79914dbc2cd2ce19c1ae3a3e`  
		Last Modified: Sat, 19 Mar 2022 21:00:01 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ad91e85241ec6b752c76025976f23d679c8eda783616cb3d8830044dcb21a`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaebf6593ed9f193fbd8172caa14b34ddf91ceab1a3dc48c01ad9e695794966`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d1d821c92f5f66422e0625adaed7d15289260431916f065c873a51902db85`  
		Last Modified: Sat, 19 Mar 2022 21:00:10 GMT  
		Size: 113.7 MB (113727951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730acde910ffb0b1920533e60561ebf0826b19c5d57baa84709e782722f8539`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:1dc812cf6152a1dbd7dd664e0764032b903cc57c50cff56b29cd4aca4225acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:b8b90f3f8aa8a5a5a0ec94c45447c20d7e2653088cd2f92fadc0fc1adbdfe9c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15d1ac77f073ff34cd4af6e8870392ef73eb84279d0aeb4e35641c72b1ae3d4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:34:48 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:34:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 22:35:07 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 22:35:07 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 22:35:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:09 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 22:35:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 22:35:18 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 22:35:18 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 22:35:19 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 22:35:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 22:35:19 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 22:35:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918014104c9ad49400ad5b9cc91d4bcbae82a73fa5abc7a409bf899c6c43f707`  
		Last Modified: Sat, 19 Mar 2022 22:36:36 GMT  
		Size: 93.7 MB (93654889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dbdd5fbdd128de63982a3bcd426031fd93f653efb545091ac58b78a211fe`  
		Last Modified: Sat, 19 Mar 2022 22:36:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b04accad0ea54945a94640fe15c4f18217ac339546430605562903bb6e198c`  
		Last Modified: Sat, 19 Mar 2022 22:36:23 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ddf332606cb830b506954d33ba501b217b0cf296e237e53ef52a6a9a64c442`  
		Last Modified: Sat, 19 Mar 2022 22:36:22 GMT  
		Size: 1.0 MB (1003224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212fc94ac887dd5a2399140898860c0a998fe2df050fc6e32930fee44eb331d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea58fb34b6055f277ccc1d770336f1a956999418f8c74dcac36d843e5b416d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ddcab601ff797ff8b88340a09e3597f00209e58763e8cf7ed883c7c7dcb87`  
		Last Modified: Sat, 19 Mar 2022 22:36:28 GMT  
		Size: 113.7 MB (113727937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c310e4514d6b20246d217eb5e9eb415ba672947ac5986dff90d60de6cee91c`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8145813d259caf6cd0bea5d1927b07af9b65099efde705c1b7dc4b12dc186c85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282818f0e70e12d2041d5851adc6e578279aaaed15d0a8744828bf7dc42eefed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:09:07 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:09:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 15:09:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 15:09:55 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 15:09:56 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 15:09:57 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 15:09:58 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 15:09:59 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 15:10:00 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 15:10:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 15:10:02 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 15:10:03 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 15:10:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:06 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 15:10:08 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 15:10:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 15:10:29 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 15:10:29 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 15:10:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 15:10:31 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 15:10:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3433408c5fc7f4ae638ee2b5297e626eccb6ef1eaa854483eaa88fe9452b9`  
		Last Modified: Sat, 19 Mar 2022 15:12:08 GMT  
		Size: 85.8 MB (85763156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cf766653b0804c4ca85b92cc0c0069fac5a3f16d050f228364daa9898cdddc`  
		Last Modified: Sat, 19 Mar 2022 15:11:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef7cbb4cb2bf00d122900c6fc72a76a1c4ce7e507619ce147f81ef8541dd2`  
		Last Modified: Sat, 19 Mar 2022 15:11:57 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708c338db08b4e85061950c8cb417d1fdd8d11ab132c8869662712a9d49a856`  
		Last Modified: Sat, 19 Mar 2022 15:11:55 GMT  
		Size: 929.4 KB (929409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ab77260b346ebc4ffb2b67788f195a531157a6a926db586e202224550f95b5`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a15c093ce6465bc4b31ce2c94333e202d3a124194d56bb99438c8074746c3c`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0df29d03ead5b114014be21794a723b2a019942d32b8d108fe3f1f2de09ff`  
		Last Modified: Sat, 19 Mar 2022 15:12:12 GMT  
		Size: 113.7 MB (113727850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4162cb8595bb82ce1922c26bc251eadd27b261925942c84f067f35057191`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:0c8c69d7af8f945591a5d089408490bf52d5bc01ddafc64b7143d5ec6676a8ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7996e14d3d401d9e6a086fdc28917a40774b46df8ec09f0dd2d332cf566df8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:55:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:56:02 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:56:12 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:57:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:57:03 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:57:07 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 20:57:12 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:57:15 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:57:17 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:57:19 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 20:57:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 20:57:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 20:57:25 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:57:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:36 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:57:37 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 20:57:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 20:58:01 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 20:58:07 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:58:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:58:14 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:58:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54998de650aec3ff8c87077551a8a8dedbac826f959645af516a214758030de1`  
		Last Modified: Sat, 19 Mar 2022 21:00:18 GMT  
		Size: 86.6 MB (86557500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80861eb3c1c18c4914806cea4a42cc6605837eb735445fe587096738b931ba`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e3e83293caa8f19217184082aaf48f054162fd676b0bfe80c811db04b5fa07`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e62718fccbad62107b4fe7fd7a9a97a92e26d79914dbc2cd2ce19c1ae3a3e`  
		Last Modified: Sat, 19 Mar 2022 21:00:01 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ad91e85241ec6b752c76025976f23d679c8eda783616cb3d8830044dcb21a`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaebf6593ed9f193fbd8172caa14b34ddf91ceab1a3dc48c01ad9e695794966`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d1d821c92f5f66422e0625adaed7d15289260431916f065c873a51902db85`  
		Last Modified: Sat, 19 Mar 2022 21:00:10 GMT  
		Size: 113.7 MB (113727951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730acde910ffb0b1920533e60561ebf0826b19c5d57baa84709e782722f8539`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:9bd37caef5943cf2cdc2a20993002c2d8d794f6f549da01f08ac9fdc56d2ae2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:aa6c404694792455f659ab29b685840a58847a82ee8d6b933510ab9b8d415e85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3791a1d923d653fa2c3fc2640e7509051adf42a471ba281268d753580e1da5f9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:23:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 04:23:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 04:23:38 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 04:23:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 04:23:39 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 04:23:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 04:23:40 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 04:23:40 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 04:23:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 04:23:48 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 04:23:48 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 04:23:48 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 04:23:48 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 04:23:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 04:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 04:23:49 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 04:23:49 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 04:23:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 04:23:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff37705a3721b6f0fa369c96374cf9da30cff49af0d8000271ef496b3a770df`  
		Last Modified: Tue, 05 Apr 2022 04:24:23 GMT  
		Size: 60.7 MB (60744505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f66c34cc10d0cb3a031ef3da4ba3f1bd013bcc964d4956c60fad86f44fe69`  
		Last Modified: Tue, 05 Apr 2022 04:24:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2578f03d3de8ca415ec7f424f8e565acd05fed61f7ae257c04a206815af3329f`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217417d523fc2999c4b2897458c8186aaae7637ca11cffcf678f5a94676243c3`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bafdba13f86b25d0530d42b1945be474d808e2e57c54eb92525278fd97b4066`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7700ffe2df31bc40779a5addc28e3643352992303bc5cd5013f722caeea46b`  
		Last Modified: Tue, 05 Apr 2022 04:24:20 GMT  
		Size: 116.7 MB (116690800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6f64f512c1d336d8e3ad42228cc6f701c2f9ef296cccb6001395170ba33d88`  
		Last Modified: Tue, 05 Apr 2022 04:24:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ec277986357bc1492ec4256aeb59f9509b5206166178468fae72d7b396672ccf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7da5778516cbbaa93e6b5f1f1812601e1ea647ac7f864ea7770f27872c6bf2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:09:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 03:09:35 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 03:09:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 03:09:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 03:09:37 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 03:09:38 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 03:09:39 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 03:09:40 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 03:09:41 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 03:09:42 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 03:09:43 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 03:09:44 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 03:09:45 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 03:09:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 03:09:48 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 03:09:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 03:09:58 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 03:09:58 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 03:09:59 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 03:10:00 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 03:10:01 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 03:10:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 03:10:03 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 03:10:04 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 03:10:05 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 03:10:06 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 03:10:07 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 03:10:08 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 03:10:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 03:10:10 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 03:10:12 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 03:10:12 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 03:10:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 03:10:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66f256ad0fc5640d4ad6542e63ff033094b79f2158b7b837af471110ea8a336`  
		Last Modified: Tue, 05 Apr 2022 03:11:08 GMT  
		Size: 60.1 MB (60067315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f94323a629942950a0ffa4ebd9b9a9a67e2e99450c1b63b7caa029bb6fbab5`  
		Last Modified: Tue, 05 Apr 2022 03:10:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d6976ee94f88624b6444d82e171da5997a9fc114743925400901581ea08c58`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb5aabbb25b6ba30936e48e8d131ebfb29068a96236f7ce6e56f8aea4faafaf`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583ba33b8f8be7b90a8de59a31f336886c4e754bd8846e3019ee792422b0c930`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 3.0 KB (3000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb65a72bf0159fbfb5326ef80a1e211664490a96659378c1d97748689b176279`  
		Last Modified: Tue, 05 Apr 2022 03:11:05 GMT  
		Size: 116.7 MB (116688761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b61e2452bca6bb834b08988d9199d49b4c4ffd3228c57b794b855215c36116`  
		Last Modified: Tue, 05 Apr 2022 03:10:57 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:a8b99264c74f1637a78eb549f8e83bee8f0f2146850d2757e4d483465a901317
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176075045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766bd47323049c15860a8cea6025a09aab1552c1868c15db5ef57c14d7cc9633`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 09:02:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 05 Apr 2022 09:02:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 05 Apr 2022 09:02:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 05 Apr 2022 09:03:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 05 Apr 2022 09:03:03 GMT
ARG BONITA_VERSION
# Tue, 05 Apr 2022 09:03:05 GMT
ARG BRANDING_VERSION
# Tue, 05 Apr 2022 09:03:09 GMT
ARG BONITA_SHA256
# Tue, 05 Apr 2022 09:03:12 GMT
ARG BASE_URL
# Tue, 05 Apr 2022 09:03:16 GMT
ARG BONITA_URL
# Tue, 05 Apr 2022 09:03:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 05 Apr 2022 09:03:27 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 05 Apr 2022 09:03:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 05 Apr 2022 09:03:31 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 05 Apr 2022 09:03:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 05 Apr 2022 09:03:46 GMT
RUN mkdir /opt/files
# Tue, 05 Apr 2022 09:03:49 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 05 Apr 2022 09:04:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 05 Apr 2022 09:04:13 GMT
ENV HTTP_API=false
# Tue, 05 Apr 2022 09:04:16 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 05 Apr 2022 09:04:20 GMT
ENV HTTP_API_PASSWORD=
# Tue, 05 Apr 2022 09:04:24 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 05 Apr 2022 09:04:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 05 Apr 2022 09:04:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 05 Apr 2022 09:04:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 05 Apr 2022 09:04:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 05 Apr 2022 09:04:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 05 Apr 2022 09:04:47 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 05 Apr 2022 09:04:50 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 05 Apr 2022 09:04:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 05 Apr 2022 09:04:59 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 05 Apr 2022 09:05:01 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 05 Apr 2022 09:05:03 GMT
EXPOSE 8080 9000
# Tue, 05 Apr 2022 09:05:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 05 Apr 2022 09:05:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5434586e006643fe98fc4f4804ae9fc2bda4db5b77b98a9fd444e497dfe6b0d0`  
		Last Modified: Tue, 05 Apr 2022 09:06:41 GMT  
		Size: 56.6 MB (56562945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edcf9db5a1b38af5bb9fdf73e674526ec2ea289819852645d9d188fad87bf21`  
		Last Modified: Tue, 05 Apr 2022 09:06:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744c2e63c2fbfc1abb8e0d67e64b0f60853a2071bc30215f0a253be92cb274c6`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4adf978bd9de05949fabf35a650d95b209d0cf397d6a01c098b30cc4072089`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144701e366b871fd0167a7150ebd9e22e946ad67a354ed2ec7cb3871ee76bb2`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e847d35ce919fdc67b9945f9238ecff157ddbabd7d47bcfd9897bfc32b81e3c5`  
		Last Modified: Tue, 05 Apr 2022 09:06:38 GMT  
		Size: 116.7 MB (116690887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341eef26fc26324a7ea91c42a1be66b6b8a7d8230c1df8986f8c6e22e2fa38d4`  
		Last Modified: Tue, 05 Apr 2022 09:06:28 GMT  
		Size: 5.4 KB (5429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
