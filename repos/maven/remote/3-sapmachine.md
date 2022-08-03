## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:7ffc97022a7a9f231f21772a315195d979f1ab9b9f758a2ba9b65fda7156373f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:9fb9f1a6b06303efd0d954cd961c5e2be459b03c6de426b317f938cd6dfa6a62
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274499134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f6b96fc2438e3302e9d38c2ab813edf04de3a562fcbdfdc51b9dcfe08b3e96`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:50:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:51:26 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:51:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 02 Aug 2022 20:51:27 GMT
CMD ["jshell"]
# Wed, 03 Aug 2022 07:38:38 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 07:38:39 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 03 Aug 2022 07:38:39 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Aug 2022 07:38:39 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 03 Aug 2022 07:38:39 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 03 Aug 2022 07:38:47 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 03 Aug 2022 07:38:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Aug 2022 07:38:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Aug 2022 07:38:47 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 03 Aug 2022 07:38:47 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 03 Aug 2022 07:38:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Aug 2022 07:38:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec46b9acc9819591d454afdad02524fdf15208773bd023a9da61286c272baa1c`  
		Last Modified: Tue, 02 Aug 2022 20:52:20 GMT  
		Size: 7.9 MB (7920242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e450e1d764f78da00304a3a4f962c25a214c558e12c2d836a422644944e0d1`  
		Last Modified: Tue, 02 Aug 2022 20:52:59 GMT  
		Size: 197.2 MB (197215911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e17cabc3d9ac3370b5d60d9c219e13901bc626d7b740f31a1b48721f5a0692`  
		Last Modified: Wed, 03 Aug 2022 07:46:21 GMT  
		Size: 32.0 MB (32049684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cca5c68a51e5c96b726ea2c3d3d1fc831259999bcdcdd9077fa1ba789e423b`  
		Last Modified: Wed, 03 Aug 2022 07:46:17 GMT  
		Size: 8.7 MB (8739486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf4311646fa464e415b2131e99efe01806ada72292bf69dd02c22fdfc2ad49b`  
		Last Modified: Wed, 03 Aug 2022 07:46:16 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c7681b964b55b1341daac0deba6a7170cd6228a3bc23c83efcd7303097b53f`  
		Last Modified: Wed, 03 Aug 2022 07:46:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
