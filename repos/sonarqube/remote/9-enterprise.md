## `sonarqube:9-enterprise`

```console
$ docker pull sonarqube@sha256:aba731a0b5d9705fec4cf036f71749d0e87c25387e4f730946bee314d0baa6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sonarqube:9-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:2e53a618bde6abc43fc581af637aaecd5c923e2d4bb7bae4e2fe955efa55c6e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.7 MB (484651054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41da366347d90db3fa69aa6d5c4b8aa9a0ba346dc1124e719cc1b25d02de0810`
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
# Fri, 12 Aug 2022 22:42:52 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.6.0.59041.zip
# Fri, 12 Aug 2022 22:42:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.6.0.59041 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 12 Aug 2022 22:43:27 GMT
# ARGS: SONARQUBE_VERSION=9.6.0.59041 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.6.0.59041.zip
RUN set -eux;     addgroup -S -g 1000 sonarqube;     adduser -S -D -u 1000 -G sonarqube sonarqube;     apk add --no-cache --virtual build-dependencies gnupg unzip curl;     apk add --no-cache bash su-exec ttf-dejavu openjdk11-jre;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     chown -R sonarqube:sonarqube ${SONARQUBE_HOME};     chmod -R 777 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apk del --purge build-dependencies; 	cd "${SONARQUBE_HOME}/elasticsearch/bin" ; 	sed -i -e 's/\r$//' elasticsearch elasticsearch-env elasticsearch-env-from-file ;
# Fri, 12 Aug 2022 22:43:29 GMT
COPY --chown=sonarqube:sonarqubemulti:66701f646ad2f21287c063721ad66eabe0c3f39a3371b70504abf154fe36a694 in /opt/sonarqube/bin/ 
# Fri, 12 Aug 2022 22:43:29 GMT
WORKDIR /opt/sonarqube
# Fri, 12 Aug 2022 22:43:29 GMT
EXPOSE 9000
# Fri, 12 Aug 2022 22:43:29 GMT
STOPSIGNAL SIGINT
# Fri, 12 Aug 2022 22:43:29 GMT
ENTRYPOINT ["/opt/sonarqube/bin/run.sh"]
# Fri, 12 Aug 2022 22:43:29 GMT
CMD ["/opt/sonarqube/bin/sonar.sh"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfbfff6b1668493b0b19e94c0ca2ec0634f1c2b828f4eb3c3e55b8d78bf894a`  
		Last Modified: Fri, 12 Aug 2022 22:49:51 GMT  
		Size: 481.8 MB (481826428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1678f0cb7eab16ca35fc7394eb9ca5eb92a6df8aef2bf3ca145c547cb2a2ffa9`  
		Last Modified: Fri, 12 Aug 2022 22:49:24 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
