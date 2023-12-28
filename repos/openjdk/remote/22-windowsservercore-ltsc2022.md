## `openjdk:22-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:2dd12c87b22813a40d1fc6000ca30f362fcf04b6719976086021cce71589e04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `openjdk:22-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull openjdk@sha256:c71219ecb8929437572dbbfa8b11ef33da336b7a994fdec7e7a665e0bbad9db1
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087834212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8ba2c958e8186aa5855dd2059c6799a4c5f68617d7832b37a1917f586f79ec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Wed, 27 Dec 2023 21:53:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Dec 2023 21:54:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:54:24 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 27 Dec 2023 21:54:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:54:31 GMT
ENV JAVA_VERSION=22-ea+29
# Wed, 27 Dec 2023 21:54:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/29/GPL/openjdk-22-ea+29_windows-x64_bin.zip
# Wed, 27 Dec 2023 21:54:32 GMT
ENV JAVA_SHA256=78ac775c98c21936b976b697605990f73d1b7011e37cc7e2478488a74b2cd247
# Wed, 27 Dec 2023 21:55:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:55:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80ade58e2c5fbafaa925a419ca6ce4b8f8cd0a9a96e57f7455d615f0dc76215`  
		Last Modified: Wed, 27 Dec 2023 21:55:07 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e28802ba179dfa146caf64698e6c9b933ae4ad531c655ecb6b100d124072518`  
		Last Modified: Wed, 27 Dec 2023 21:55:07 GMT  
		Size: 515.9 KB (515925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92c10f9b8524da54d2ac52d4ce679135798c2e857be96c19e536276e259a802`  
		Last Modified: Wed, 27 Dec 2023 21:55:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c0e9f85d53663b6bbb6fe4c4dda8f1b527c64ce73a6096d9d5bef2cd39c2c5`  
		Last Modified: Wed, 27 Dec 2023 21:55:07 GMT  
		Size: 333.3 KB (333306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82223523acc44a78e539e6ad9b73f6a3be75fef3d521aa98c60aaba363ed46c5`  
		Last Modified: Wed, 27 Dec 2023 21:55:06 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1613150671b588068ddb255daa6f6f74a8e5f471f352637ca7dbfd796f4f73`  
		Last Modified: Wed, 27 Dec 2023 21:55:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b9861928b62f80af0506b71b12aa78d76c2420e55ac4d64999cbfba37c9ad4`  
		Last Modified: Wed, 27 Dec 2023 21:55:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f36f79adeea9e2f543c321661856a73064369ab96a7ea51794274c40095b8b`  
		Last Modified: Wed, 27 Dec 2023 21:55:16 GMT  
		Size: 197.7 MB (197703628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb43d44649ce1a66d072b27b0c33e87cb152dc2be1d836aa5ca4cf9b7f183ee`  
		Last Modified: Wed, 27 Dec 2023 21:55:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
