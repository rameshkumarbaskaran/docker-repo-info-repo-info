## `adoptopenjdk:11-jdk-hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:d94b1500d2f132360b61c70385bcf371475ab1812b46b7cf8e8a8e108e54487f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `adoptopenjdk:11-jdk-hotspot-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull adoptopenjdk@sha256:16618a35855d932b0a19034dd99e5827c509727894784305a8407613fb4dc580
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2679786680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a9a1f36eb8a4086a19f14ed7d0e66f6f901ea130cead4f2eb4cffc290964a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 17 Jul 2020 22:55:17 GMT
ENV JAVA_VERSION=jdk-11.0.8+10
# Fri, 17 Jul 2020 22:57:48 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.8_10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.8_10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (148b487e0dde39ec5c0f32aa2397c17968b6cf6818822cea2b2394dfd0157396) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '148b487e0dde39ec5c0f32aa2397c17968b6cf6818822cea2b2394dfd0157396') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 17 Jul 2020 22:57:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7b66bdcf6a1deae29e3dc95b56af1ccb3e91839b7945590251ac670c897a80`  
		Last Modified: Sat, 18 Jul 2020 01:14:47 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7ae27b4c93c1d5f4e9af35c9523103d92ce043509f7c192ce7d7a4763832b3`  
		Last Modified: Sat, 18 Jul 2020 01:15:19 GMT  
		Size: 369.6 MB (369590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9effddcd1608bab7cd9fd3dd3de4abf41bc49441ed23ebe28c1f822c5ea9ab45`  
		Last Modified: Sat, 18 Jul 2020 01:14:48 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
