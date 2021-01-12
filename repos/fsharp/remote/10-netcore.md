## `fsharp:10-netcore`

```console
$ docker pull fsharp@sha256:d398df2e8254e1c06510575f709c8806efe84c901966a07da3f8067bf14f37e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:10-netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:7cd41c58565cb6d87ce7bb91eab8596f349394466051cfe11a0135924ebf9a95
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332934984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8499459433a8592d9d53700fc3662a0ebf55d88425bf52ccc3d7039732b9508b`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 04:13:10 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 12 Jan 2021 04:13:10 GMT
ENV MONO_THREADS_PER_CPU=50
# Tue, 12 Jan 2021 04:25:55 GMT
RUN MONO_VERSION=6.10.0.104 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Tue, 12 Jan 2021 04:25:55 GMT
WORKDIR /root
# Tue, 12 Jan 2021 04:25:56 GMT
CMD ["fsharpi"]
# Tue, 12 Jan 2021 04:42:43 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Tue, 12 Jan 2021 04:42:43 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.8-api/
# Tue, 12 Jan 2021 04:42:44 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Tue, 12 Jan 2021 04:42:58 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 04:43:24 GMT
RUN DOTNET_SDK_VERSION=3.1.403 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=0a0319ee8e9042bf04b6e83211c2d6e44e40e604bff0a133ba0d246d08bff76ebd88918ab5e10e6f7f0d2b504ddeb65c0108c6539bc4fbc4f09e4af3937e88ea &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Tue, 12 Jan 2021 04:43:27 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Tue, 12 Jan 2021 04:43:28 GMT
WORKDIR /root
# Tue, 12 Jan 2021 04:43:28 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012538d7964c4f88903101ebc0a455c252239e9889988a52beb6cfb9d4e973c4`  
		Last Modified: Tue, 12 Jan 2021 04:44:33 GMT  
		Size: 160.5 MB (160499308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99e5018deff23d811c8318e09baecbeccf5bd111e1d1ae76e42fcaea6a9c4aa`  
		Last Modified: Tue, 12 Jan 2021 04:45:26 GMT  
		Size: 17.2 MB (17205438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ce3e2cb5e8cc1e8a9cc14503c97592d1c93f02163890c1c7e519bbfe9d744b`  
		Last Modified: Tue, 12 Jan 2021 04:45:48 GMT  
		Size: 123.8 MB (123846316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6972925cf483716b09c417b56e741caa36a21b1ad08d83edf980a3fc4b44f5b`  
		Last Modified: Tue, 12 Jan 2021 04:45:23 GMT  
		Size: 4.3 MB (4275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
