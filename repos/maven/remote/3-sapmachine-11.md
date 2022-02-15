## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:593db9dfeabdc546950f124b8a723a2ce4f5cd48a881b81c87568c8e6b740e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-sapmachine-11` - linux; amd64

```console
$ docker pull maven@sha256:4b3e01017f2eaae250896e82a6825c1613fca9f672e7672e8d9be3da07eb1a79
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275560145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f964081c8657c7f45f0eed29dd6e9529cc6d2172727fce001093f20b7dd61c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 07:04:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Feb 2022 19:35:53 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.14.1     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Feb 2022 19:35:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 09 Feb 2022 19:35:54 GMT
CMD ["jshell"]
# Mon, 14 Feb 2022 20:26:15 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Mon, 14 Feb 2022 20:26:16 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 14 Feb 2022 20:26:16 GMT
ARG USER_HOME_DIR=/root
# Mon, 14 Feb 2022 20:26:16 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 14 Feb 2022 20:26:16 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 14 Feb 2022 20:26:24 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 14 Feb 2022 20:26:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 14 Feb 2022 20:26:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 14 Feb 2022 20:26:25 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 14 Feb 2022 20:26:25 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 14 Feb 2022 20:26:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 14 Feb 2022 20:26:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62164c5b3eea6ba9e40ab7adbcb5b8d492e8c8c0c763bd36f36cf58c59f3ee7b`  
		Last Modified: Wed, 02 Feb 2022 07:05:57 GMT  
		Size: 8.3 MB (8318363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3706635550bf903deb21bdfb36201d406116b0443e679da64b8a5786b18b3b0a`  
		Last Modified: Wed, 09 Feb 2022 19:36:29 GMT  
		Size: 197.7 MB (197710459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548605bb534fd5274eef6676d15faf2b96911b76a52f4bdd03f6dd0be92efb10`  
		Last Modified: Mon, 14 Feb 2022 20:34:31 GMT  
		Size: 31.9 MB (31856172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be303655ee48218520c2c85f8593241c7ae84b54411f589cff84e176dec6936b`  
		Last Modified: Mon, 14 Feb 2022 20:34:27 GMT  
		Size: 9.1 MB (9109837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb50c74d61e124d1a986150b2bf47639b71275c0ae35265184a3fc86f9774ca`  
		Last Modified: Mon, 14 Feb 2022 20:34:26 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7fcf2b3c32fe93d2170ce3e553a457cf9d86d60ac64974dfde4531da22eda0`  
		Last Modified: Mon, 14 Feb 2022 20:34:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
