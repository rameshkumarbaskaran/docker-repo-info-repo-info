## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:8f591ca56c38d6976c6469da1654cc4e8957d900995bc10c52d5394dcf067fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-sapmachine-11` - linux; amd64

```console
$ docker pull maven@sha256:aef980963b536538fc09895d29d996d8c4cbbd04aac8b1304051ead1a1f0fb2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275831368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1fb07e9aeb954142869a479954374fdf15fecba1ff08bd4718a9955f5398ec`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 13:19:55 GMT
ARG RELEASE
# Thu, 26 Jan 2023 13:19:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 13:19:55 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Jan 2023 13:19:57 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Thu, 26 Jan 2023 13:19:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 20:18:39 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:19:14 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.18     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:19:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 31 Jan 2023 20:19:15 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 23:18:44 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 23:18:44 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 23:18:44 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 23:18:45 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 23:18:45 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 23:18:52 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 23:18:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 23:18:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 23:18:52 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 23:18:52 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 23:18:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 23:18:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1278cf339380e0a07c6e1307b321875623c71291c41a78a24bdf707b892a3da7`  
		Last Modified: Tue, 31 Jan 2023 20:20:46 GMT  
		Size: 7.9 MB (7913339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b7798c9526b8ab76087b41031e57a440ba8e804a87abbc3d9e4b4a74f341d`  
		Last Modified: Tue, 31 Jan 2023 20:20:59 GMT  
		Size: 198.9 MB (198930604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d53e213dc06ca562568810dd616e9f8e0b7bd76b3b2ea9a0af497afbd0c7c8b`  
		Last Modified: Tue, 31 Jan 2023 23:23:59 GMT  
		Size: 32.1 MB (32057179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37015723aba6ab21bb2e4ab72424f578fae6fa72c11b352cbccfa652658206cc`  
		Last Modified: Tue, 31 Jan 2023 23:23:54 GMT  
		Size: 8.4 MB (8351153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23c5e4160a2eb5fbd9d5e39d014eba03ddcfc6a08dbe5e9cfba933566ebab18`  
		Last Modified: Tue, 31 Jan 2023 23:23:53 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355c36c431ef475ff870b172908de3b26ac1ac80ce1f453a8d46521f59dc1c04`  
		Last Modified: Tue, 31 Jan 2023 23:23:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
