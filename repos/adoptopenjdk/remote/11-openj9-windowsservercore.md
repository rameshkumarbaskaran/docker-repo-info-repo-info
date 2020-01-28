## `adoptopenjdk:11-openj9-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:0c1775fe54c198bb4f95754281abc078a076bc43007978e40d10669aa6a11087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `adoptopenjdk:11-openj9-windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull adoptopenjdk@sha256:75b3a8947b5cfc451825b1a4834bde1c5a6a061132b52baab9d2ba4e67aad698
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6114258059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79bcf09cf849df874f3dec89b370255792f3ef79420a340b40bd229aec13948`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2020 00:53:32 GMT
ENV JAVA_VERSION=jdk-11.0.6+10_openj9-0.18.1
# Tue, 28 Jan 2020 00:56:57 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Tue, 28 Jan 2020 00:56:59 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Tue, 28 Jan 2020 00:57:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895fa985c7424ab63c9f3c73dcfe9a8c43f2d08df8eb80b38e5a567efe1a34e2`  
		Last Modified: Tue, 28 Jan 2020 01:29:42 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7eb90e36ca901f9d1773c46ead7b1ce23fc87cf874adcfcd3c41c74d49cc1b4`  
		Last Modified: Tue, 28 Jan 2020 01:30:33 GMT  
		Size: 389.7 MB (389653960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c16422a578766e85081450f9b873e06744174d33dfd86d192555f8a8c4ed17`  
		Last Modified: Tue, 28 Jan 2020 01:29:42 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625d780d6f81f4b53cfc104f686828f0a670403eef67de2575c259431d226242`  
		Last Modified: Tue, 28 Jan 2020 01:29:42 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-openj9-windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull adoptopenjdk@sha256:71068602a046cb4a72dcb254899391d6867274e59855461248c131b76225efdf
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2601793769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdc32fb055a764c868839fc78f3e55c404ee0b33c932209bc4ecd5bfbd70d58`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2020 00:57:22 GMT
ENV JAVA_VERSION=jdk-11.0.6+10_openj9-0.18.1
# Tue, 28 Jan 2020 01:00:15 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Tue, 28 Jan 2020 01:00:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Tue, 28 Jan 2020 01:00:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f287131ae3de30144bb1c32167483f475d88baa5a43ef38669d5bc23c415eee`  
		Last Modified: Tue, 28 Jan 2020 01:31:04 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba0dfb56ebfc9c9a353d8429d1329d6db23951e5eefa090e290990437f9de5a`  
		Last Modified: Tue, 28 Jan 2020 01:32:03 GMT  
		Size: 384.4 MB (384377799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff71878329ed1516e1f8193aa14b0ae61c6ecb9ed5099a665b092de174497484`  
		Last Modified: Tue, 28 Jan 2020 01:31:04 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3279fce38aa1097d01495efb98819f47f87b32b5751133585982ba48e737333`  
		Last Modified: Tue, 28 Jan 2020 01:31:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-openj9-windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull adoptopenjdk@sha256:dedc849438d5b673c864d4cbb6bc570fab7f25a6a73842cf67f2303a37255b71
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5800571547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499cb3cefa94eb6a1b94522053d81a4ec1b4984c7231b5f6f04dba627c179732`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Jan 2020 00:53:32 GMT
ENV JAVA_VERSION=jdk-11.0.6+10_openj9-0.18.1
# Tue, 28 Jan 2020 01:02:23 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jre_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jre_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (d3d6f7c320b4d2c1bc270cf85ef901395c74ef66562455ca51b48eb2cbff5380) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd3d6f7c320b4d2c1bc270cf85ef901395c74ef66562455ca51b48eb2cbff5380') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Tue, 28 Jan 2020 01:02:26 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895fa985c7424ab63c9f3c73dcfe9a8c43f2d08df8eb80b38e5a567efe1a34e2`  
		Last Modified: Tue, 28 Jan 2020 01:29:42 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389ed538740b0db256859ae575803c60f7c60e2e5ac3c01283b0e0f8d1a81135`  
		Last Modified: Tue, 28 Jan 2020 01:32:47 GMT  
		Size: 76.0 MB (75968676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24283e262f28b4c7a2d50db5433ef613c215def6bc342f931b4a3fc6278f2e98`  
		Last Modified: Tue, 28 Jan 2020 01:32:34 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
