## `sonarqube:community`

```console
$ docker pull sonarqube@sha256:9ca40ae23bb2228a6c4cc8c20de41fcd72a8ed7358331b4bd5910cd20dcee995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:community` - linux; amd64

```console
$ docker pull sonarqube@sha256:bd53b7146a1462351e98c7bd85b07ac4bf0e026df3015eab823648fca9549d6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367421034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e543676fb9a244d1d5659fac2f078efa6f8f1a351759f5d52f3f2ed401738fd2`
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
# Fri, 12 Aug 2022 22:41:44 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.6.0.59041.zip
# Fri, 12 Aug 2022 22:41:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.6.0.59041 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 12 Aug 2022 22:42:05 GMT
# ARGS: SONARQUBE_VERSION=9.6.0.59041 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.6.0.59041.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies;
# Fri, 12 Aug 2022 22:42:07 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 12 Aug 2022 22:42:07 GMT
WORKDIR /opt/sonarqube
# Fri, 12 Aug 2022 22:42:07 GMT
EXPOSE 9000
# Fri, 12 Aug 2022 22:42:07 GMT
STOPSIGNAL SIGINT
# Fri, 12 Aug 2022 22:42:07 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 12 Aug 2022 22:42:07 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1220b1fb64e6bb1f38bda3e7458a9c698ac930da3036ba1eb7ab8eacef5c6283`  
		Last Modified: Fri, 12 Aug 2022 22:48:29 GMT  
		Size: 364.6 MB (364596409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a3b7127edef73f1bbca18585a34ae886032627aa69dfc638a99511aaf2cede`  
		Last Modified: Fri, 12 Aug 2022 22:48:05 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
