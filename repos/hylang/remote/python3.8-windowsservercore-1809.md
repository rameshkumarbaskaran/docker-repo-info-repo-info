## `hylang:python3.8-windowsservercore-1809`

```console
$ docker pull hylang@sha256:535b0ad3954b0c1f9a6e5cbf781d26e022e8679db3403e5b8a31c63f066b1b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `hylang:python3.8-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull hylang@sha256:a772da6f35d2262f98f2d79c5caf195b6a593f4ae91a0757d20f1eb0f10a57f7
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2353087478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c207979a7b91b235da2a481e7cb1ffe6c0b92184d739e614a05f025aa39498a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Tue, 09 Jun 2020 22:33:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 23:49:48 GMT
ENV PYTHON_VERSION=3.8.3
# Tue, 09 Jun 2020 23:49:49 GMT
ENV PYTHON_RELEASE=3.8.3
# Tue, 09 Jun 2020 23:51:44 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 09 Jun 2020 23:51:45 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Tue, 09 Jun 2020 23:51:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Tue, 09 Jun 2020 23:51:47 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Tue, 09 Jun 2020 23:53:15 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2020 23:53:16 GMT
CMD ["python"]
# Wed, 10 Jun 2020 00:24:39 GMT
ENV HY_VERSION=0.18.0
# Wed, 10 Jun 2020 00:25:18 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 10 Jun 2020 00:25:19 GMT
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
	-	`sha256:6f9004cf1af66427119816150a155709e40b7df48839b5fbe61fabed47d333a4`  
		Last Modified: Wed, 10 Jun 2020 00:05:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b868a48a478a439f3ef4e33ad624d3fd9346a8d00903b58033c1fe7c58999b8`  
		Last Modified: Wed, 10 Jun 2020 00:05:31 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1162d7ffe229edc0cd753260b28a44d1b01a3aee76f6e5043ca4a23ec97dbcd4`  
		Last Modified: Wed, 10 Jun 2020 00:06:28 GMT  
		Size: 52.6 MB (52551169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cc6d6116488f2bd9d664eedf7455cb73ff02037e8c97e509e6b20ac8e5395a`  
		Last Modified: Wed, 10 Jun 2020 00:05:29 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad14fd666be521d0e033be7d1610e87fb58e308fdb359987e283a8d274df827f`  
		Last Modified: Wed, 10 Jun 2020 00:05:28 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf63762ebad895ea5039ecf2678864f426b6fea25641eaed266145d67aa2b452`  
		Last Modified: Wed, 10 Jun 2020 00:05:28 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1838b59d1e2def32b01e54edb700b16221ee96e075bc9059644c0f5d66bb5485`  
		Last Modified: Wed, 10 Jun 2020 00:05:30 GMT  
		Size: 5.5 MB (5480455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df8c1a107c22801ec4cedab25846a40d38e5052e8d05da1018d504df9fbc40f`  
		Last Modified: Wed, 10 Jun 2020 00:05:28 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08003aa2664df5b547ee6347068332a33865758b6bd579f664272e3eacccb013`  
		Last Modified: Wed, 10 Jun 2020 00:30:21 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e947b9ac66a4b6ee623b4208c025d87a19935e3d0ae4f9843a6be6afeb5acd75`  
		Last Modified: Wed, 10 Jun 2020 00:30:21 GMT  
		Size: 1.1 MB (1131262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093606eddfa262ffaafa42036f6256f129438ab9828e1f188de89e7d7a4ea685`  
		Last Modified: Wed, 10 Jun 2020 00:30:19 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
