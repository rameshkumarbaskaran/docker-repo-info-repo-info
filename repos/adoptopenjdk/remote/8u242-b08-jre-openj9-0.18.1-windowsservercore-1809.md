## `adoptopenjdk:8u242-b08-jre-openj9-0.18.1-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:09b0a7668b7adc0692d68acfad635626b8604f79538f3f0c9f244031833ed842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `adoptopenjdk:8u242-b08-jre-openj9-0.18.1-windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull adoptopenjdk@sha256:2ccce9518cc60d4c2e7a1eaa080483d045546e401bd7d367be2e9adfe20910fa
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2322942728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11727b36f8b9b1199649b034d7e666efa5ae2023952aee35572cb0d9aa5c7fdb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 11:14:31 GMT
ENV JAVA_VERSION=jdk8u242-b08_openj9-0.18.1
# Thu, 20 Feb 2020 11:20:49 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08_openj9-0.18.1/OpenJDK8U-jre_x64_windows_openj9_8u242b08_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08_openj9-0.18.1/OpenJDK8U-jre_x64_windows_openj9_8u242b08_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (a8aa18b79dc2fddc9563951f975cfbf6490c8ccfc92cbda924ac7b9ed9454bf5) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a8aa18b79dc2fddc9563951f975cfbf6490c8ccfc92cbda924ac7b9ed9454bf5') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Thu, 20 Feb 2020 11:20:52 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838a1df172e35934800cc4589e26e8535c55d5d3e2d7f4df74fbc936af8d9088`  
		Last Modified: Thu, 20 Feb 2020 12:04:42 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d873d35a6f5dc7e0f15c201442df5a82a6a22fbfdbb7459e448b1b637f2ce5`  
		Last Modified: Thu, 20 Feb 2020 12:06:41 GMT  
		Size: 92.4 MB (92435237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468518f0c7fa121252edd34e6007020b5a56074392154dc4ec0984542b293011`  
		Last Modified: Thu, 20 Feb 2020 12:06:27 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
