## `sonarqube:9-datacenter-search`

```console
$ docker pull sonarqube@sha256:51a35ee70da4a0352a85b0a76123e1b02551209925f106467d7fd61d0fc0baa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:127ad186b51ee7fac31fc68c8a0dbf7c00229df3e5b089a0af254e894dfeda2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.1 MB (507115030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a8fc47850765eceb507715fb250b871a6ffc8f822dc42c19aece93049514d1`
-	Entrypoint: `["\/opt\/sonarqube\/bin\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/bin\/sonar.sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 12 Aug 2022 22:41:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Aug 2022 22:41:43 GMT
ARG SONARQUBE_VERSION=9.6.0.59041
# Fri, 12 Aug 2022 22:43:32 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.6.0.59041.zip
# Fri, 12 Aug 2022 22:44:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.6.0.59041 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Fri, 12 Aug 2022 22:44:26 GMT
# ARGS: SONARQUBE_VERSION=9.6.0.59041 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.6.0.59041.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt ;    cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME} ;     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}" ;     apk del --purge build-dependencies;
# Fri, 12 Aug 2022 22:44:28 GMT
COPY --chown=sonarqube:sonarqubemulti:8997cda09b77db3cd2004e36d485c5b54ddd96e9993642921bc6be78ee8af554 in /opt/sonarqube/bin/ 
# Fri, 12 Aug 2022 22:44:28 GMT
WORKDIR /opt/sonarqube
# Fri, 12 Aug 2022 22:44:29 GMT
EXPOSE 9000
# Fri, 12 Aug 2022 22:44:29 GMT
STOPSIGNAL SIGINT
# Fri, 12 Aug 2022 22:44:29 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 12 Aug 2022 22:44:29 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5590050d63dc1e1f71b01f4b503717dd28359cf466f8e9fcbf00c3fdf03ae7`  
		Last Modified: Fri, 12 Aug 2022 22:51:16 GMT  
		Size: 504.3 MB (504290008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ea1e9fc8b22be169b4d095d61c1abc926e4f84e239a56fd8ec20a14c6eb7b1`  
		Last Modified: Fri, 12 Aug 2022 22:50:49 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
