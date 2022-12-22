## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:66c4133d4ebf3adf34c708e582e244056731d7b9845b9470ed32a82a98c4206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:739c855fd38de10d59ab33b8a5f6a4dd020bd92e0c42495b5896eee32b737ac0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.3 MB (520260361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6038cf0c9eeb027ccfa5b790ea011173c443475feea3a2bb8eb96cc7627a1d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:22:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:22:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Dec 2022 10:32:19 GMT
ARG VERBOSE=false
# Fri, 09 Dec 2022 10:32:19 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Dec 2022 02:42:44 GMT
ARG EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530
# Thu, 22 Dec 2022 02:42:44 GMT
ARG NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0
# Thu, 22 Dec 2022 02:42:44 GMT
ARG NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc
# Thu, 22 Dec 2022 02:42:44 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.13 org.opencontainers.image.revision=cl221320221205-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Dec 2022 02:42:44 GMT
ENV LIBERTY_VERSION=22.0.0_13
# Thu, 22 Dec 2022 02:42:45 GMT
ARG LIBERTY_URL
# Thu, 22 Dec 2022 02:42:45 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Dec 2022 02:43:08 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 02:43:08 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Dec 2022 02:43:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.13 BuildLabel=cl221320221205-1900
# Thu, 22 Dec 2022 02:43:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Dec 2022 02:43:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Dec 2022 02:43:10 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Thu, 22 Dec 2022 02:43:10 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Dec 2022 02:43:11 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Dec 2022 02:43:20 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Dec 2022 02:43:20 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 22 Dec 2022 02:43:20 GMT
USER 1001
# Thu, 22 Dec 2022 02:43:20 GMT
EXPOSE 9080 9443
# Thu, 22 Dec 2022 02:43:20 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Dec 2022 02:43:20 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Dec 2022 02:44:21 GMT
ARG VERBOSE=false
# Thu, 22 Dec 2022 02:44:21 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Dec 2022 02:53:16 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Thu, 22 Dec 2022 02:53:17 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Dec 2022 02:53:48 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb0aaff24d2e9d944fe20d8d7b841c223905eed0cad23da4932cdc722436b29`  
		Last Modified: Fri, 09 Dec 2022 04:24:59 GMT  
		Size: 129.3 MB (129322664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef387a10193572f4f42678002c2961e316c78e5d846c1372ad28c5558fe0ef9f`  
		Last Modified: Thu, 22 Dec 2022 03:13:54 GMT  
		Size: 14.3 MB (14284329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81caaecba3c7876e3a774b07bd337fbde8c0c7e25ed0e3abf9194fc9fb24a91c`  
		Last Modified: Thu, 22 Dec 2022 03:13:51 GMT  
		Size: 682.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1808dfd0d9fc6ad2983a7164406b92743e8826fa929183f8777993937fbdf8a`  
		Last Modified: Thu, 22 Dec 2022 03:13:51 GMT  
		Size: 9.8 KB (9760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4443e34462a64ef512bc5d12cb8bae84a9a3c173fab25f386a8e4acde190f5`  
		Last Modified: Thu, 22 Dec 2022 03:13:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ec399156fd718173af5f93c729d10a40d208bf5d2a373e643f1c583b7b0fd7`  
		Last Modified: Thu, 22 Dec 2022 03:13:51 GMT  
		Size: 10.7 KB (10736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb06cb26f06f4553270794183b2b53ddfe1e63b2e0a776882128d9d7180eeba`  
		Last Modified: Thu, 22 Dec 2022 03:13:51 GMT  
		Size: 5.9 MB (5882103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e14b715c8b9fbfd69c1c9d352a1ac18664ab1924fdaa6221ab8db69f985d81a`  
		Last Modified: Thu, 22 Dec 2022 03:14:35 GMT  
		Size: 324.9 MB (324939939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e583f6bdc75b9d9b8294ccf23eceb308ba75a3ecc365a8327a3ccba7f7025546`  
		Last Modified: Thu, 22 Dec 2022 03:14:18 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b2d50c9d13ee74e34c2faff39ff661c1aead4738b683ac287ba92b2e541c07`  
		Last Modified: Thu, 22 Dec 2022 03:14:21 GMT  
		Size: 16.1 MB (16147891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:fd39b512410362f6e2323ae3348b92b9bb6fad6ff4c9b4815bc3afae59ff8738
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.1 MB (521125871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4732f135a0997ca1150ed240bc702bf8da3f119cfa9061e953de17baf624a6ed`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:05:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:05:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Dec 2022 04:38:06 GMT
ARG VERBOSE=false
# Fri, 09 Dec 2022 04:38:07 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Dec 2022 03:34:25 GMT
ARG EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530
# Thu, 22 Dec 2022 03:34:25 GMT
ARG NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0
# Thu, 22 Dec 2022 03:34:26 GMT
ARG NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc
# Thu, 22 Dec 2022 03:34:27 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.13 org.opencontainers.image.revision=cl221320221205-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Dec 2022 03:34:27 GMT
ENV LIBERTY_VERSION=22.0.0_13
# Thu, 22 Dec 2022 03:34:27 GMT
ARG LIBERTY_URL
# Thu, 22 Dec 2022 03:34:28 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Dec 2022 03:35:31 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Dec 2022 03:35:32 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Dec 2022 03:35:32 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.13 BuildLabel=cl221320221205-1900
# Thu, 22 Dec 2022 03:35:33 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Dec 2022 03:35:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Dec 2022 03:35:36 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Thu, 22 Dec 2022 03:35:36 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Dec 2022 03:35:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Dec 2022 03:35:52 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Dec 2022 03:35:53 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 22 Dec 2022 03:35:53 GMT
USER 1001
# Thu, 22 Dec 2022 03:35:53 GMT
EXPOSE 9080 9443
# Thu, 22 Dec 2022 03:35:54 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Dec 2022 03:35:54 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Dec 2022 03:38:16 GMT
ARG VERBOSE=false
# Thu, 22 Dec 2022 03:38:16 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Dec 2022 03:53:57 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Thu, 22 Dec 2022 03:54:04 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Dec 2022 03:54:59 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103bba608e4bcf78845fbe100e090c5cbdd4d12ecd86a1d8aaab5fb5d5778837`  
		Last Modified: Fri, 09 Dec 2022 03:11:06 GMT  
		Size: 129.0 MB (128996365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3616c22e47b0c7700aee6275425f77e6347d17a8d33d0f8ecfd0a4d1a99d1c`  
		Last Modified: Thu, 22 Dec 2022 04:32:49 GMT  
		Size: 14.3 MB (14284818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67321ce54b761efea213e093ea01cdf9ef053086d1f0eb0dad3f3f3609f50293`  
		Last Modified: Thu, 22 Dec 2022 04:32:45 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86a6f496b9c1c67ab30a7204afc65a614aa716c558a69eb78ec2f02c0cd3413`  
		Last Modified: Thu, 22 Dec 2022 04:32:45 GMT  
		Size: 9.8 KB (9758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d6621dd2b3b71cde2ef1ab56e1782e4cd98caacfe235d2c1ddf7b2183cd14d`  
		Last Modified: Thu, 22 Dec 2022 04:32:45 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a244197a1b0e3652814b6a23e123de1b3482467d131071a92267fc16ed83db6`  
		Last Modified: Thu, 22 Dec 2022 04:32:45 GMT  
		Size: 10.8 KB (10757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a3a9acd98fd78a284467f378f01c9ed0671a37c32407f0e49245232fd0fda7`  
		Last Modified: Thu, 22 Dec 2022 04:32:47 GMT  
		Size: 5.5 MB (5498029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abde0f59cd84358148b363143e0b462f9eeb1ff8f1d4a9e02ea16e7ed1af6cd`  
		Last Modified: Thu, 22 Dec 2022 04:33:47 GMT  
		Size: 324.9 MB (324940228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f68d250ed97469107e2fbc73e9db94ba758f483ecc86fa6df7e549b1985a68`  
		Last Modified: Thu, 22 Dec 2022 04:33:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb6fccfab8bc159e5e07158388f89e681d9c474661fafecbd7d2c9de7a91bf1`  
		Last Modified: Thu, 22 Dec 2022 04:33:22 GMT  
		Size: 13.9 MB (13865796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:1973e4a00a4c8175e32165e79efcc3803ac11515d269700b60eca13ab8ac96f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.6 MB (515595614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d015ab03474bcea4aef853c7f9023f5466eff6671b77347d4aa70e16b5bbcc9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:17:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:17:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Dec 2022 05:30:43 GMT
ARG VERBOSE=false
# Fri, 09 Dec 2022 05:30:44 GMT
ARG OPENJ9_SCC=true
# Wed, 21 Dec 2022 23:44:55 GMT
ARG EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530
# Wed, 21 Dec 2022 23:44:56 GMT
ARG NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0
# Wed, 21 Dec 2022 23:44:57 GMT
ARG NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc
# Wed, 21 Dec 2022 23:44:58 GMT
LABEL org.opencontainers.image.authors=Leo Christy Jesuraj, Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.13 org.opencontainers.image.revision=cl221320221205-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 21 Dec 2022 23:44:58 GMT
ENV LIBERTY_VERSION=22.0.0_13
# Wed, 21 Dec 2022 23:44:59 GMT
ARG LIBERTY_URL
# Wed, 21 Dec 2022 23:44:59 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 21 Dec 2022 23:45:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 23:45:29 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 23:45:29 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.13 BuildLabel=cl221320221205-1900
# Wed, 21 Dec 2022 23:45:30 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 21 Dec 2022 23:45:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 21 Dec 2022 23:45:37 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Wed, 21 Dec 2022 23:45:38 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 21 Dec 2022 23:45:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 21 Dec 2022 23:45:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=5062904442242bf7935fadec638812cdbce614a7d22d5dc267b7b47767a81530 NON_IBM_SHA=a0a7b4082bb39a2435f7ddc4d383746bf09d05834b545dd3dfa4405f6e4e9ff0 NOTICES_SHA=7376962045d167dddb46459382b15a4a6811feb29e032420f7f95383dba2a3dc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 21 Dec 2022 23:45:57 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 21 Dec 2022 23:45:58 GMT
USER 1001
# Wed, 21 Dec 2022 23:45:59 GMT
EXPOSE 9080 9443
# Wed, 21 Dec 2022 23:45:59 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 21 Dec 2022 23:46:00 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 21 Dec 2022 23:48:14 GMT
ARG VERBOSE=false
# Wed, 21 Dec 2022 23:48:15 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 21 Dec 2022 23:57:11 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 21 Dec 2022 23:57:28 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 21 Dec 2022 23:58:09 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fdd86aa56415e723ad1c625e8e84de704bd93370cb5380694e05e888e84210`  
		Last Modified: Fri, 09 Dec 2022 03:20:31 GMT  
		Size: 126.5 MB (126472625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8834e8ca6a9b6589941264f63a19a884e8ad4c90f131a264adb36994843fd8`  
		Last Modified: Thu, 22 Dec 2022 00:22:34 GMT  
		Size: 14.3 MB (14284436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93708e07b42388d6f82f69a6e9bffa58b60174bf622a4fb19dcdcf3501301a5f`  
		Last Modified: Thu, 22 Dec 2022 00:22:32 GMT  
		Size: 687.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344b48e15da2f0c5baacbf720b117e629c8492002f6886d4545d760bb59913c2`  
		Last Modified: Thu, 22 Dec 2022 00:22:32 GMT  
		Size: 9.8 KB (9761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce06a6049a997bb33eba06f279d1a9a75891d3c6c751665b94569eec72bcf6ba`  
		Last Modified: Thu, 22 Dec 2022 00:22:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4158ebaa99166036ed591791a10512d3668defe6e83069e1d1e133868d2c7a`  
		Last Modified: Thu, 22 Dec 2022 00:22:32 GMT  
		Size: 10.7 KB (10749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab69aac834c72cdd1367c5b0869522d76f8222d10b0617d3ec12f5d73ff6195`  
		Last Modified: Thu, 22 Dec 2022 00:22:32 GMT  
		Size: 6.1 MB (6097184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8212bb74ebe88d7d31a8274f695993728a6c0cc3ea750d3cd0b943112885618f`  
		Last Modified: Thu, 22 Dec 2022 00:23:10 GMT  
		Size: 324.9 MB (324939185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00268b50364107c534d52f464d866d3b3a1c56fede8c6d1c5daffc2f68c2890b`  
		Last Modified: Thu, 22 Dec 2022 00:22:55 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda38e03d0f4d8402d5d1230b5737a882df1aa3270cd89d798e5144f2f7ae16a`  
		Last Modified: Thu, 22 Dec 2022 00:22:58 GMT  
		Size: 15.7 MB (15741124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
