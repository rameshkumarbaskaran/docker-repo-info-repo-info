## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:cada68dcf9da0d3c9834a302fe09b7c40e594674eee89b81457efa9e0183424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7f529f9b883e7508d4d1a47443425886646969b67110faca226ecd6e3d7db0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303285075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f0876e68b678eab976554606ae27aabd58cc4db13da7af5ec730f198d334d1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:09:48 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:09:58 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:09:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:09:58 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:10:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:10:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:10:02 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:10:03 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b853465de20699222566708b0cb06b4069871dad8bcce008ddcbbf0c1bbac40f`  
		Last Modified: Tue, 31 Oct 2023 03:12:54 GMT  
		Size: 144.9 MB (144873899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a62bc2ad4395e9ebe6c929c8e5e13d173c66164b7a20ee8484ab8d7e147ad`  
		Last Modified: Tue, 31 Oct 2023 03:12:44 GMT  
		Size: 6.5 MB (6522266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdc8bfe48d470191a4f525a0d0a2b2d2df8cf58b607493f4fe27287d41a7e8a`  
		Last Modified: Tue, 31 Oct 2023 03:12:42 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f61cdc434df46bf9943e942b815c6121c056d9a469e1d1ff9b88d8c8ac6b080`  
		Last Modified: Tue, 31 Oct 2023 03:12:49 GMT  
		Size: 112.6 MB (112571528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e852f99034810f3853e7fbd42ccb0207c3cfc7ea9a1cbc9458f169446970d2ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300468610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682e56eb5ed513792f1a3c4c10172712d2e63f8c1737aa35adea5df8ed058dbe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 03:55:13 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 03:55:33 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Tue, 31 Oct 2023 03:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 31 Oct 2023 03:55:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 31 Oct 2023 03:55:33 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 31 Oct 2023 03:55:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Tue, 31 Oct 2023 03:55:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 03:55:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 31 Oct 2023 03:55:37 GMT
VOLUME [/data /logs]
# Tue, 31 Oct 2023 03:55:37 GMT
EXPOSE 7473 7474 7687
# Tue, 31 Oct 2023 03:55:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 31 Oct 2023 03:55:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fed2ff3e93e200ff72bc61afff6be5f7308927c09ac68cf254714c7fabd2492`  
		Last Modified: Tue, 31 Oct 2023 03:58:12 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2deb54bf49d8218d04bbfbd9825b15f7b0149c7ee4c607a2e40a99c1832842`  
		Last Modified: Tue, 31 Oct 2023 03:58:04 GMT  
		Size: 6.5 MB (6516591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f4cf921619b8aac5f90d22a4751c47aee713ce6ccc841fd7091823360a9953`  
		Last Modified: Tue, 31 Oct 2023 03:58:03 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787c30cb8efdf63af7a59c1dc194fc2f186fe59528309cacb4525b7ca4b18ea5`  
		Last Modified: Tue, 31 Oct 2023 03:58:08 GMT  
		Size: 112.6 MB (112571529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
