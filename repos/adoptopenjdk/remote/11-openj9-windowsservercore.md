## `adoptopenjdk:11-openj9-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:3129e23712f835d1910b2a2adbbc06e78d3fb9e671074bc44c5ca87e00568e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `adoptopenjdk:11-openj9-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull adoptopenjdk@sha256:969bd840ff5ba687d0ff5949700c7be563fa9c04dcb924f4d71a33c8e978cb9b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2688967481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3174855c54a7cb1226558c31cc22a846f52f235fcc7425687a07356c06d34150`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Jul 2020 00:24:17 GMT
ENV JAVA_VERSION=jdk-11.0.8+10_openj9-0.21.0
# Sat, 18 Jul 2020 00:26:58 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10_openj9-0.21.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.8_10_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10_openj9-0.21.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.8_10_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (7250326e5fad877da447bc1e37dfbfcaca18b10f1acc82ffc557a9421dc068bf) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7250326e5fad877da447bc1e37dfbfcaca18b10f1acc82ffc557a9421dc068bf') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 18 Jul 2020 00:27:00 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Sat, 18 Jul 2020 00:27:01 GMT
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
	-	`sha256:4daee471b24230a5cd78984baebc91527ce3072d7bf9eee3b7513cf18b801912`  
		Last Modified: Sat, 18 Jul 2020 01:18:25 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a708d1d9fe4f255d8b68a76b6a5440b8ca8dbdd45f50b821a6bdfd0ab38ba7`  
		Last Modified: Sat, 18 Jul 2020 01:18:55 GMT  
		Size: 378.8 MB (378770703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32bc72aa4a8faa2e69227819ab26f187be209962563bceae3748e46a78c7450`  
		Last Modified: Sat, 18 Jul 2020 01:18:25 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255a1b5671916413be740c0851bee9de835a715c408c1d3c335db8cf91f5a695`  
		Last Modified: Sat, 18 Jul 2020 01:18:25 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
