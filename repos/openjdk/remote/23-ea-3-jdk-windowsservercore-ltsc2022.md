## `openjdk:23-ea-3-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:aa1d11ebc10a8b30b6a2193bf5e3eae1318cfdd230847fcf53f0a1c884531926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `openjdk:23-ea-3-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull openjdk@sha256:0407832f766d1bea0593d8563fd33b51ca9f8c959f35fd04c362abf3bf7a4ce4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087878923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152067342b403db9023406b2e266e9893cce5bfe6c9bfbb5b6e515c2957f4a7a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Wed, 27 Dec 2023 21:53:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Dec 2023 21:54:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:54:25 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 27 Dec 2023 21:54:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:54:33 GMT
ENV JAVA_VERSION=23-ea+3
# Wed, 27 Dec 2023 21:54:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_windows-x64_bin.zip
# Wed, 27 Dec 2023 21:54:34 GMT
ENV JAVA_SHA256=540333ea6c1ebfa807c83b9b95584a6bf796924d9e2dd3731975515cb9875fb1
# Wed, 27 Dec 2023 21:55:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 27 Dec 2023 21:55:06 GMT
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
	-	`sha256:baa0bcf82c557cf4e7416f90e5cd0db943cf7cbf6c2b52e118d4da050d610830`  
		Last Modified: Wed, 27 Dec 2023 21:55:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e358dcfbbe3aa7e9a36a95394eac20a2fb57ef7c6cf84ae8c41defd3493722ba`  
		Last Modified: Wed, 27 Dec 2023 21:55:11 GMT  
		Size: 499.6 KB (499577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50659cee906383c14e2eef616c5002a929b7b5a0acfccd3aa35d09888654d2b5`  
		Last Modified: Wed, 27 Dec 2023 21:55:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df951756adf5c2609f84be5d8ff92979d0669e6324095a7625cfb0ec28e6163`  
		Last Modified: Wed, 27 Dec 2023 21:55:11 GMT  
		Size: 316.3 KB (316308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6def1548c46591c8369512dfc2de4bdf8ce33a2f6b58ebe00d864136e42012`  
		Last Modified: Wed, 27 Dec 2023 21:55:09 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbe6443a442e613a315b2c2e3ec813968917a1f04af23bbcd3d8ae7bffaac5d`  
		Last Modified: Wed, 27 Dec 2023 21:55:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8952a4cadf6fe5ee0bad4fd06b1b23dcf24a905e0fc79d3b1f4de4bdc583be87`  
		Last Modified: Wed, 27 Dec 2023 21:55:09 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ecc00c439a0f76a369e0b9f22b3b01b74bcf725ceffc4528cefbc2bae0e13`  
		Last Modified: Wed, 27 Dec 2023 21:55:20 GMT  
		Size: 197.8 MB (197781652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71f0aea78a3ca6fde072bb69e413f56f3bac7ce1e6bd750f43275c0e2a9f8f3`  
		Last Modified: Wed, 27 Dec 2023 21:55:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
