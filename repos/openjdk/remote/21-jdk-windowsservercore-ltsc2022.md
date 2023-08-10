## `openjdk:21-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e49ce6c5a4ea820210a25947331d33c7f20993c3ca1cfc280e77b4892e7d22ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `openjdk:21-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull openjdk@sha256:10c0f69bec7873fad6db2158f4a73b410c5773c5ffd17242399b58c4cadf0701
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1996391165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d3806747e62867f3684591d49c94db91aef55e5456e00ba1ec9960501210e7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 02:36:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 10 Aug 2023 02:43:01 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 10 Aug 2023 02:43:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 10 Aug 2023 02:43:22 GMT
ENV JAVA_VERSION=21-ea+34
# Thu, 10 Aug 2023 02:43:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/34/GPL/openjdk-21-ea+34_windows-x64_bin.zip
# Thu, 10 Aug 2023 02:43:24 GMT
ENV JAVA_SHA256=535816b01c3da46efed9897c95e2198dc1d3aa4b1d3e6b06da8dbdbc2cfbd4c2
# Thu, 10 Aug 2023 02:44:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 10 Aug 2023 02:44:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a18930eb7350c60f06351657db53550ff8c064f9f63673a2955eb64b696ffbd`  
		Last Modified: Thu, 10 Aug 2023 02:48:56 GMT  
		Size: 452.7 KB (452708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724681ec83ac29f19beeb1cb4fe664ac3de56a42d7f381314110fedb4f063463`  
		Last Modified: Thu, 10 Aug 2023 02:50:54 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ffe6018f3cff93f4bc90eacb1002f4cb347245b09e012b4071e3911805d7f0`  
		Last Modified: Thu, 10 Aug 2023 02:50:55 GMT  
		Size: 262.9 KB (262873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58980653d3b1c650eaecc1ef4cf98e6291f6aac3418aa5e2946d979259d46bc`  
		Last Modified: Thu, 10 Aug 2023 02:50:52 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77907fa4e20e26a5b02e3b02be5f8877744db905d006b6de341e774294f23f6`  
		Last Modified: Thu, 10 Aug 2023 02:50:52 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a3da077ffcf4e5ea784d923d95f1aac7320fb582fa485c9c00e2de346fe9b5`  
		Last Modified: Thu, 10 Aug 2023 02:50:52 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bf49c9b040789537e8236fe3aa4f06d336d496b87dfa73ed81e7bbcb084203`  
		Last Modified: Thu, 10 Aug 2023 02:51:13 GMT  
		Size: 198.3 MB (198303271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35660a99319963b3748dcbf8c54f8338004a91309db0a59fc8667a0f573a428b`  
		Last Modified: Thu, 10 Aug 2023 02:50:52 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
