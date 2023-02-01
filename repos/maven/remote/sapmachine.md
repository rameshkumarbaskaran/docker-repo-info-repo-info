## `maven:sapmachine`

```console
$ docker pull maven@sha256:a683fdde3499d6a074c11ed03c00909b5eae1c4c44b9f651d085ff2aac35b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:bed43f589234ce25a9bebb69923a282be4f0d30414638084ea6f5f6b6a0573ec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274981322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d108ca1a20efb793083ec5e08710f15e25e42a8119168f74d8c0317b66f8ca`
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
# Tue, 31 Jan 2023 20:19:55 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 20:19:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 31 Jan 2023 20:19:56 GMT
CMD ["jshell"]
# Tue, 31 Jan 2023 23:19:07 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 23:19:07 GMT
ARG MAVEN_VERSION=3.8.7
# Tue, 31 Jan 2023 23:19:07 GMT
ARG USER_HOME_DIR=/root
# Tue, 31 Jan 2023 23:19:07 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Tue, 31 Jan 2023 23:19:07 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Tue, 31 Jan 2023 23:19:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 31 Jan 2023 23:19:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 31 Jan 2023 23:19:10 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 31 Jan 2023 23:19:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 31 Jan 2023 23:19:10 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 31 Jan 2023 23:19:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 31 Jan 2023 23:19:10 GMT
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
	-	`sha256:14de22f37a02eacdf06717158c302cf571bb87bc9f4d1520a5c1648ad162b87e`  
		Last Modified: Tue, 31 Jan 2023 20:21:23 GMT  
		Size: 198.1 MB (198080629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0e2bfdf039e289a87b43a6f9a1e4f5372cc56ab3a0888b0660e15c3b121d6c`  
		Last Modified: Tue, 31 Jan 2023 23:24:15 GMT  
		Size: 32.1 MB (32057125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c97089590f1449ae98cd57c032cd199b53d86c9776da41e44b49249e50397dd`  
		Last Modified: Tue, 31 Jan 2023 23:24:10 GMT  
		Size: 8.4 MB (8351135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130fb19d4c969c5c2f1323ec757cc021bd32e9dccbc2bfc3a81be3717b54a17`  
		Last Modified: Tue, 31 Jan 2023 23:24:09 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbc97a925ddeb26a84464c38ba1f4825e891ab3aec43df53b8c88b688bf47ed`  
		Last Modified: Tue, 31 Jan 2023 23:24:10 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
