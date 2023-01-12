## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:fea0758ad1b2686d690701f7375189f17a276cc74fcd95964ae9328fda884ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:e37af6b7bb9437511759af6c8a095f6d720ed65c42d3b13fadf8245c7c56de74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274933806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d455d16447fc4e4bde4f9335695b30959c7442b08b13d4ec5f9bdc6ea9493a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 06:08:30 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Jan 2023 02:28:58 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.5     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Jan 2023 02:28:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 12 Jan 2023 02:28:59 GMT
CMD ["jshell"]
# Thu, 12 Jan 2023 02:47:44 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Jan 2023 02:47:44 GMT
ARG MAVEN_VERSION=3.8.7
# Thu, 12 Jan 2023 02:47:44 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Jan 2023 02:47:44 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Thu, 12 Jan 2023 02:47:44 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Thu, 12 Jan 2023 02:47:50 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 12 Jan 2023 02:47:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Jan 2023 02:47:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Jan 2023 02:47:51 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 12 Jan 2023 02:47:51 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 12 Jan 2023 02:47:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Jan 2023 02:47:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9829f76f3bad367d27d5bf3e91e6bc0f738874c547c1b6c35ea445acb9f11`  
		Last Modified: Fri, 09 Dec 2022 06:10:29 GMT  
		Size: 7.9 MB (7912181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc23e95071d6152338b7fcf5049f4865dfb8db677b3a9f106375a1089786020d`  
		Last Modified: Thu, 12 Jan 2023 02:30:25 GMT  
		Size: 198.0 MB (198038329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eeeaffd00d2ac2b5d283b11ae6a63035a101b12dbce0cc487386983a87f161`  
		Last Modified: Thu, 12 Jan 2023 02:49:56 GMT  
		Size: 32.1 MB (32054043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638717135c644847fa0535f6720f71e6fe3e540ce2855f9988b833d09bd34835`  
		Last Modified: Thu, 12 Jan 2023 02:49:52 GMT  
		Size: 8.4 MB (8351156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4113d4863324b6ca7f421b23156ae4d4ae2669827f38d83d6dcea778ea2f9c5`  
		Last Modified: Thu, 12 Jan 2023 02:49:51 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d0a1dfac759a0292cd409d8efc4ede3211e79498e537cdcc289031d17524ad`  
		Last Modified: Thu, 12 Jan 2023 02:49:51 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
