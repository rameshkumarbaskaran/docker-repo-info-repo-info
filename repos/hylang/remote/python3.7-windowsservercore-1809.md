## `hylang:python3.7-windowsservercore-1809`

```console
$ docker pull hylang@sha256:dfdb44821f82d95d5aa5b1590fed33738daf9770b467fa5c901880eb89852d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `hylang:python3.7-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull hylang@sha256:ab410fbe27341ec89cdde32be1d5e84cc9ee264a1214745faff021743e5f82cd
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2352051758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077b7d54b671f8e1f53f99bceecee5b2c7b80b9a98fed934f6794569f80be9e7`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Jun 2020 18:19:59 GMT
ENV PYTHON_VERSION=3.7.8
# Tue, 30 Jun 2020 18:20:00 GMT
ENV PYTHON_RELEASE=3.7.8
# Tue, 30 Jun 2020 18:21:41 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 30 Jun 2020 18:21:42 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Tue, 30 Jun 2020 18:21:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Tue, 30 Jun 2020 18:21:44 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Tue, 30 Jun 2020 18:22:29 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 30 Jun 2020 18:22:30 GMT
CMD ["python"]
# Tue, 30 Jun 2020 18:40:36 GMT
ENV HY_VERSION=0.18.0
# Tue, 30 Jun 2020 18:41:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 30 Jun 2020 18:41:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f841c6a0c622cd36b5b2688011a224ac3e8e96273758f4a2804f2f3f099f267d`  
		Last Modified: Tue, 09 Jun 2020 23:17:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae35fe0883411acfae02a26e0d6409d7c81cfdc056c6e502b8f385d809a6ccfb`  
		Last Modified: Tue, 30 Jun 2020 18:23:55 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af8d29f298682a241a9ccd5c686349246e067e0a38dec26a430deeef64c3cb4`  
		Last Modified: Tue, 30 Jun 2020 18:23:55 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725e7cb625891898b58155fbfccd43972388276dad7f176f9b755ff02b13ebef`  
		Last Modified: Tue, 30 Jun 2020 18:24:03 GMT  
		Size: 51.5 MB (51533100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d499216498e84acdef3d1e7f8c1982a81d1a371e6630c7ccdcb3c27f5715c3ed`  
		Last Modified: Tue, 30 Jun 2020 18:23:52 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb27af0646fb9267d46af3c75e783ad20da9e718e75ee9d1ad062323fe1b605`  
		Last Modified: Tue, 30 Jun 2020 18:23:52 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e296ffcbf4b8a736d194ee89b578db189f7bdc1d0556c4e00371a0419c3a9fd7`  
		Last Modified: Tue, 30 Jun 2020 18:23:53 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b080528a2a96c0f1d56e5958be82a85aaf7e7c5e1fb6c11678b8ed9426367986`  
		Last Modified: Tue, 30 Jun 2020 18:23:54 GMT  
		Size: 5.5 MB (5453394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511d103c92b01dda2da752707465ed08e1249bceb242d146bce4a6a0069423b9`  
		Last Modified: Tue, 30 Jun 2020 18:23:52 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04df66c04d6d920600a89f74c9db19252f60a703668d0d22207f926e475386df`  
		Last Modified: Tue, 30 Jun 2020 18:43:32 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9a91ecdbe110aaa5624e9252468bb5c5e192c870bab95e8072aac094dc571`  
		Last Modified: Tue, 30 Jun 2020 18:43:33 GMT  
		Size: 1.1 MB (1140807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af39f7214b032b8fb077de1846a3c0de8ecb22407be0a162ea08cbf4638e840c`  
		Last Modified: Tue, 30 Jun 2020 18:43:32 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
