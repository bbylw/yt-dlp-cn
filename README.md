> 本文档汉化自 [yt-dlp/yt-dlp](https://github.com/yt-dlp/yt-dlp)

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
<div align="center">

[![YT-DLP](https://raw.githubusercontent.com/yt-dlp/yt-dlp/master/.github/banner.svg)](#readme)

[![Release version](https://img.shields.io/github/v/release/yt-dlp/yt-dlp?color=brightgreen&label=Download&style=for-the-badge)](#installation "安装")
[![PyPI](https://img.shields.io/badge/-PyPI-blue.svg?logo=pypi&labelColor=555555&style=for-the-badge)](https://pypi.org/project/yt-dlp "PyPI")
[![Donate](https://img.shields.io/badge/_-Donate-red.svg?logo=githubsponsors&labelColor=555555&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/blob/master/Maintainers.md#maintainers "捐赠")
[![Discord](https://img.shields.io/discord/807245652072857610?color=blue&labelColor=555555&label=&logo=discord&style=for-the-badge)](https://discord.gg/H5MNcFW63r "Discord")
[![Supported Sites](https://img.shields.io/badge/-Supported_Sites-brightgreen.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md "支持的网站")
[![License: Unlicense](https://img.shields.io/badge/-Unlicense-blue.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/blob/master/LICENSE "许可证")
[![CI Status](https://img.shields.io/github/actions/workflow/status/yt-dlp/yt-dlp/core.yml?branch=master&label=Tests&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/actions "CI 状态")
[![Commits](https://img.shields.io/github/commit-activity/m/yt-dlp/yt-dlp?label=commits&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/commits "提交历史")
[![Last Commit](https://img.shields.io/github/last-commit/yt-dlp/yt-dlp/master?label=&style=for-the-badge&display_timestamp=committer)](https://github.com/yt-dlp/yt-dlp/pulse/monthly "最后活动")

</div>
<!-- MANPAGE: END EXCLUDED SECTION -->

yt-dlp 是一个功能丰富的命令行音频/视频下载器，支持[数千个网站](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md)。该项目是 [youtube-dl](https://github.com/ytdl-org/youtube-dl) 的分支，基于现已不活跃的 [youtube-dlc](https://github.com/blackjack4494/yt-dlc)。

<!-- MANPAGE: MOVE "USAGE AND OPTIONS" SECTION HERE -->

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
* [安装](#安装)
    * [详细说明](https://github.com/yt-dlp/yt-dlp/wiki/Installation)
    * [发布文件](#发布文件)
    * [更新](#更新)
    * [依赖](#依赖项)
    * [编译](#编译)
* [使用和选项](#用法和选项)
    * [常规选项](#常规选项)
    * [网络选项](#网络选项)
    * [地理限制](#地理限制)
    * [视频选择](#视频选择)
    * [下载选项](#下载选项)
    * [文件系统选项](#文件系统选项)
    * [缩略图选项](#缩略图选项)
    * [互联网快捷方式选项](#互联网快捷方式选项)
    * [详细信息和模拟选项](#详细程度和模拟选项)
    * [变通方法](#变通方法)
    * [视频格式选项](#视频格式选项)
    * [字幕选项](#字幕选项)
    * [身份验证选项](#认证选项)
    * [后处理选项](#后处理选项)
    * [SponsorBlock 选项](#sponsorblock-选项)
    * [提取器选项](#提取器选项)
    * [预设别名](#预设别名)
* [配置](#配置)
    * [配置文件编码](#配置文件编码)
    * [使用 netrc 进行身份验证](#使用-netrc-进行认证)
    * [关于环境变量的说明](#关于环境变量的说明)
* [输出模板](#输出模板)
    * [输出模板示例](#输出模板示例)
* [格式选择](#格式选择)
    * [过滤格式](#过滤格式)
    * [排序格式](#排序格式)
    * [格式选择示例](#格式选择示例)
* [修改元数据](#修改元数据)
    * [修改元数据示例](#修改元数据示例)
* [提取器参数](#提取器参数)
* [插件](#插件)
    * [安装插件](#安装插件)
    * [开发插件](#开发插件)
* [嵌入 YT-DLP](#嵌入-yt-dlp)
    * [嵌入示例](#嵌入示例)
* [与 YOUTUBE-DL 的差异](#与-youtube-dl-的变化)
    * [新功能](#新功能)
    * [默认行为的差异](#默认行为的差异)
    * [已弃用的选项](#已弃用的选项)
* [贡献](https://github.com/yt-dlp/yt-dlp/blob/master/CONTRIBUTING.md#contributing-to-yt-dlp)
    * [提交问题](https://github.com/yt-dlp/yt-dlp/blob/master/CONTRIBUTING.md#opening-an-issue)
    * [开发者说明](https://github.com/yt-dlp/yt-dlp/blob/master/CONTRIBUTING.md#developer-instructions)
* [WIKI](https://github.com/yt-dlp/yt-dlp/wiki)
    * [常见问题](https://github.com/yt-dlp/yt-dlp/wiki/FAQ)
<!-- MANPAGE: END EXCLUDED SECTION -->


# 安装

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
[![Windows](https://img.shields.io/badge/-Windows_x64-blue.svg?style=for-the-badge&logo=windows)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe)
[![Unix](https://img.shields.io/badge/-Linux/BSD-red.svg?style=for-the-badge&logo=linux)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp)
[![MacOS](https://img.shields.io/badge/-MacOS-lightblue.svg?style=for-the-badge&logo=apple)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos)
[![PyPI](https://img.shields.io/badge/-PyPI-blue.svg?logo=pypi&labelColor=555555&style=for-the-badge)](https://pypi.org/project/yt-dlp)
[![Source Tarball](https://img.shields.io/badge/-Source_tar-green.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)
[![Other variants](https://img.shields.io/badge/-Other-grey.svg?style=for-the-badge)](#release-files)
[![All versions](https://img.shields.io/badge/-All_Versions-lightgrey.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/releases)
<!-- MANPAGE: END EXCLUDED SECTION -->

您可以使用[二进制文件](#release-files)、[pip](https://pypi.org/project/yt-dlp)或第三方包管理器来安装 yt-dlp。有关详细说明，请参阅[wiki](https://github.com/yt-dlp/yt-dlp/wiki/Installation)


<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
## 发布文件

#### 推荐

| 文件                                                                                   | 描述                                                                                                                       |
| :------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| [yt-dlp](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp)             | 平台无关的 [zipimport](https://docs.python.org/3/library/zipimport.html) 二进制文件。需要 Python（推荐用于 **Linux/BSD**） |
| [yt-dlp.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe)     | Windows (Win8+) 独立 x64 二进制文件（推荐用于 **Windows**）                                                                |
| [yt-dlp_macos](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos) | 通用 MacOS (10.15+) 独立可执行文件（推荐用于 **MacOS**）                                                                   |

#### 替代方案

| 文件                                                                                                                   | 描述                                                          |
| :--------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------ |
| [yt-dlp_linux](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux)                                 | Linux (glibc 2.17+) 独立 x86_64 二进制文件                    |
| [yt-dlp_linux.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux.zip)                         | 未打包的 Linux (glibc 2.17+) x86_64 可执行文件（无自动更新）  |
| [yt-dlp_linux_aarch64](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux_aarch64)                 | Linux (glibc 2.17+) 独立 aarch64 二进制文件                   |
| [yt-dlp_linux_aarch64.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux_aarch64.zip)         | 未打包的 Linux (glibc 2.17+) aarch64 可执行文件（无自动更新） |
| [yt-dlp_linux_armv7l.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux_armv7l.zip)           | 未打包的 Linux (glibc 2.31+) armv7l 可执行文件（无自动更新）  |
| [yt-dlp_musllinux](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_musllinux)                         | Linux (musl 1.2+) 独立 x86_64 二进制文件                      |
| [yt-dlp_musllinux.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_musllinux.zip)                 | 未打包的 Linux (musl 1.2+) x86_64 可执行文件（无自动更新）    |
| [yt-dlp_musllinux_aarch64](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_musllinux_aarch64)         | Linux (musl 1.2+) 独立 aarch64 二进制文件                     |
| [yt-dlp_musllinux_aarch64.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_musllinux_aarch64.zip) | 未打包的 Linux (musl 1.2+) aarch64 可执行文件（无自动更新）   |
| [yt-dlp_x86.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_x86.exe)                             | Windows (Win8+) 独立 x86 (32 位) 二进制文件                   |
| [yt-dlp_win_x86.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_win_x86.zip)                     | 未打包的 Windows (Win8+) x86 (32 位) 可执行文件（无自动更新） |
| [yt-dlp_arm64.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_arm64.exe)                         | Windows (Win10+) 独立 ARM64 二进制文件                        |
| [yt-dlp_win_arm64.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_win_arm64.zip)                 | 未打包的 Windows (Win10+) ARM64 可执行文件（无自动更新）      |
| [yt-dlp_win.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_win.zip)                             | 未打包的 Windows (Win8+) x64 可执行文件（无自动更新）         |
| [yt-dlp_macos.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos.zip)                         | 未打包的 MacOS (10.15+) 可执行文件（无自动更新）              |

#### 其他

| 文件                                                                                           | 描述                         |
| :--------------------------------------------------------------------------------------------- | :--------------------------- |
| [yt-dlp.tar.gz](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)       | 源代码压缩包                 |
| [SHA2-512SUMS](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-512SUMS)         | GNU 风格的 SHA512 校验和     |
| [SHA2-512SUMS.sig](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-512SUMS.sig) | SHA512 校验和的 GPG 签名文件 |
| [SHA2-256SUMS](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-256SUMS)         | GNU 风格的 SHA256 校验和     |
| [SHA2-256SUMS.sig](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-256SUMS.sig) | SHA256 校验和的 GPG 签名文件 |

可用于验证 GPG 签名的公钥可在[此处获取](https://github.com/yt-dlp/yt-dlp/blob/master/public.key)
使用示例：
```
curl -L https://github.com/yt-dlp/yt-dlp/raw/master/public.key | gpg --import
gpg --verify SHA2-256SUMS.sig SHA2-256SUMS
gpg --verify SHA2-512SUMS.sig SHA2-512SUMS
```

#### 许可证

虽然 yt-dlp 采用 [Unlicense](https://github.com/yt-dlp/yt-dlp/blob/master/LICENSE) 许可，但许多发布文件包含来自其他项目的代码，这些项目使用不同的许可证。

最值得注意的是，PyInstaller 打包的可执行文件包含 GPLv3+ 许可的代码，因此组合作品采用 [GPLv3+](https://www.gnu.org/licenses/gpl-3.0.html) 许可。

zipimport Unix 可执行文件 (`yt-dlp`) 包含来自 [`meriyah`](https://github.com/meriyah/meriyah) 的 [ISC](https://github.com/meriyah/meriyah/blob/main/LICENSE.md) 许可代码和来自 [`astring`](https://github.com/davidbonnet/astring) 的 [MIT](https://github.com/davidbonnet/astring/blob/main/LICENSE) 许可代码。

详情请参阅 [THIRD_PARTY_LICENSES.txt](https://github.com/yt-dlp/yt-dlp/blob/master/THIRD_PARTY_LICENSES.txt)。

git 仓库、源代码压缩包 (`yt-dlp.tar.gz`)、PyPI 源代码分发和 PyPI 构建分发 (wheel) 仅包含采用 [Unlicense](https://github.com/yt-dlp/yt-dlp/blob/master/LICENSE) 许可的代码。

<!-- MANPAGE: END EXCLUDED SECTION -->

**注意**：手册页、shell 补全（自动完成）文件等可在[源代码压缩包](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)中找到


## 更新
如果您使用的是[发布二进制文件](#release-files)，可以使用 `yt-dlp -U` 进行更新

如果您[使用 pip 安装](https://github.com/yt-dlp/yt-dlp/wiki/Installation#with-pip)，只需重新运行用于安装程序的相同命令

对于其他第三方包管理器，请参阅[wiki](https://github.com/yt-dlp/yt-dlp/wiki/Installation#third-party-package-managers)或参考其文档

<a id="update-channels"></a>

目前二进制文件有三个发布渠道：`stable`（稳定版）、`nightly`（每日构建版）和 `master`（主分支版）。

* `stable` 是默认渠道，其许多更改已经过 `nightly` 和 `master` 渠道用户的测试。
* `nightly` 渠道计划在每天 UTC 午夜左右构建发布，作为项目新补丁和更改的快照。这是 yt-dlp **普通用户的推荐渠道**。`nightly` 发布版本可从 [yt-dlp/yt-dlp-nightly-builds](https://github.com/yt-dlp/yt-dlp-nightly-builds/releases) 获取，或作为 `yt-dlp` PyPI 包的开发版本（可以使用 pip 的 `--pre` 标志安装）。
* `master` 渠道提供在每次推送到主分支后构建的发布版本，这些版本将包含最新的修复和添加，但也可能更容易出现回归问题。它们可从 [yt-dlp/yt-dlp-master-builds](https://github.com/yt-dlp/yt-dlp-master-builds/releases) 获取。

使用 `--update`/`-U` 时，发布二进制文件只会更新到其当前渠道。
`--update-to CHANNEL` 可用于在有新版本可用时切换到不同的渠道。`--update-to [CHANNEL@]TAG` 也可用于升级或降级到渠道中的特定标签。

您也可以使用 `--update-to <repository>` (`<owner>/<repository>`) 更新到完全不同仓库的渠道。但是，请注意您要更新到的仓库，因为不会对来自不同仓库的二进制文件进行验证。

使用示例：

* `yt-dlp --update-to master` 切换到 `master` 渠道并更新到其最新发布版本
* `yt-dlp --update-to stable@2023.07.06` 升级/降级到 `stable` 渠道标签 `2023.07.06` 的发布版本
* `yt-dlp --update-to 2023.10.07` 升级/降级到当前渠道的标签 `2023.10.07`（如果存在）
* `yt-dlp --update-to example/yt-dlp@2023.09.24` 升级/降级到 `example/yt-dlp` 仓库的发布版本，标签 `2023.09.24`

**重要提示**：任何遇到 `stable` 发布版本问题的用户在提交错误报告之前应安装或更新到 `nightly` 发布版本：
```
# 从稳定版可执行文件/二进制文件更新到 nightly 版本：
yt-dlp --update-to nightly

# 使用 pip 安装 nightly 版本：
python -m pip install -U --pre "yt-dlp[default]"
```

当运行超过 90 天的 yt-dlp 版本时，您将看到一条警告消息，建议更新到最新版本。
您可以通过在命令或配置文件中添加 `--no-update` 来抑制此警告。

## 依赖
支持 Python 3.10+ (CPython) 和 3.11+ (PyPy) 版本。其他版本和实现可能无法正常工作。

<!-- Python 3.5+ uses VC++14 and it is already embedded in the binary created
<!x-- https://www.microsoft.com/en-us/download/details.aspx?id=26999 --x>
On Windows, [Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://download.microsoft.com/download/1/6/5/165255E7-1014-4D0A-B094-B6A430A6BFFC/vcredist_x86.exe) is also necessary to run yt-dlp. You probably already have this, but if the executable throws an error due to missing `MSVCR100.dll` you need to install it manually.
-->

虽然所有其他依赖都是可选的，但强烈推荐 `ffmpeg`、`ffprobe`、`yt-dlp-ejs` 和支持的 JavaScript 运行时/引擎

### 强烈推荐

* [**ffmpeg** 和 **ffprobe**](https://www.ffmpeg.org) - 用于[合并单独的视频和音频文件](#format-selection)以及各种[后处理](#post-processing-options)任务所必需。许可证[取决于构建版本](https://www.ffmpeg.org/legal.html)

    ffmpeg 中存在一些错误，在与 yt-dlp 一起使用时会导致各种问题。由于 ffmpeg 是如此重要的依赖项，我们在 [yt-dlp/FFmpeg-Builds](https://github.com/yt-dlp/FFmpeg-Builds) 提供了[自定义构建版本](https://github.com/yt-dlp/FFmpeg-Builds#ffmpeg-static-auto-builds)，其中包含针对这些问题的补丁。有关这些构建版本解决的具体问题的详细信息，请参阅[自述文件](https://github.com/yt-dlp/FFmpeg-Builds#patches-applied)

    **重要提示**：您需要的是 ffmpeg *二进制文件*，**不是**[同名的 Python 包](https://pypi.org/project/ffmpeg)

* [**yt-dlp-ejs**](https://github.com/yt-dlp/ejs) - 完整的 YouTube 支持所必需。采用 [Unlicense](https://github.com/yt-dlp/ejs/blob/main/LICENSE) 许可，捆绑了 [MIT](https://github.com/davidbonnet/astring/blob/main/LICENSE) 和 [ISC](https://github.com/meriyah/meriyah/blob/main/LICENSE.md) 组件。

    运行 yt-dlp-ejs 还需要 JavaScript 运行时/引擎，如 [**deno**](https://deno.land)（推荐）、[**node.js**](https://nodejs.org)、[**bun**](https://bun.sh) 或 [**QuickJS**](https://bellard.org/quickjs/)。请参阅[wiki](https://github.com/yt-dlp/yt-dlp/wiki/EJS)。

### 网络
* [**certifi**](https://github.com/certifi/python-certifi)\* - 提供 Mozilla 根证书包。采用 [MPLv2](https://github.com/certifi/python-certifi/blob/master/LICENSE) 许可
* [**brotli**](https://github.com/google/brotli)\* 或 [**brotlicffi**](https://github.com/python-hyper/brotlicffi) - [Brotli](https://en.wikipedia.org/wiki/Brotli) 内容编码支持。两者均采用 MIT 许可 <sup>[1](https://github.com/google/brotli/blob/master/LICENSE) [2](https://github.com/python-hyper/brotlicffi/blob/master/LICENSE) </sup>
* [**websockets**](https://github.com/aaugustin/websockets)\* - 用于通过 websocket 下载。采用 [BSD-3-Clause](https://github.com/aaugustin/websockets/blob/main/LICENSE) 许可
* [**requests**](https://github.com/psf/requests)\* - HTTP 库。用于 HTTPS 代理和持久连接支持。采用 [Apache-2.0](https://github.com/psf/requests/blob/main/LICENSE) 许可

#### 模拟

以下提供对模拟浏览器请求的支持。这对于一些采用 TLS 指纹识别的网站可能是必需的。

* [**curl_cffi**](https://github.com/lexiforest/curl_cffi)（推荐）- [curl-impersonate](https://github.com/lexiforest/curl-impersonate) 的 Python 绑定。提供 Chrome、Edge 和 Safari 的模拟目标。采用 [MIT](https://github.com/lexiforest/curl_cffi/blob/main/LICENSE) 许可
  * 可以通过 `curl-cffi` 额外功能安装，例如 `pip install "yt-dlp[default,curl-cffi]"`
  * 目前包含在大多数构建版本中，*除了* `yt-dlp`（Unix zipimport 二进制文件）和 `yt-dlp_x86`（Windows 32 位）


### 元数据

* [**mutagen**](https://github.com/quodlibet/mutagen)\* - 用于在某些格式中 `--embed-thumbnail`。采用 [GPLv2+](https://github.com/quodlibet/mutagen/blob/master/COPYING) 许可
* [**AtomicParsley**](https://github.com/wez/atomicparsley) - 用于在 `mutagen`/`ffmpeg` 无法处理时在 `mp4`/`m4a` 文件中 `--embed-thumbnail`。采用 [GPLv2+](https://github.com/wez/atomicparsley/blob/master/COPYING) 许可
* [**xattr**](https://github.com/xattr/xattr)、[**pyxattr**](https://github.com/iustin/pyxattr) 或 [**setfattr**](http://savannah.nongnu.org/projects/attr) - 用于在 **Mac** 和 **BSD** 上写入 xattr 元数据（`--xattrs`）。分别采用 [MIT](https://github.com/xattr/xattr/blob/master/LICENSE.txt)、[LGPL2.1](https://github.com/iustin/pyxattr/blob/master/COPYING) 和 [GPLv2+](http://git.savannah.nongnu.org/cgit/attr.git/tree/doc/COPYING) 许可

### 其他

* [**pycryptodomex**](https://github.com/Legrandin/pycryptodome)\* - 用于解密 AES-128 HLS 流和各种其他数据。采用 [BSD-2-Clause](https://github.com/Legrandin/pycryptodome/blob/master/LICENSE.rst) 许可
* [**phantomjs**](https://github.com/ariya/phantomjs) - 在一些需要运行 JavaScript 的提取器中使用。不再用于 YouTube。将在不久的将来弃用。采用 [BSD-3-Clause](https://github.com/ariya/phantomjs/blob/master/LICENSE.BSD) 许可
* [**secretstorage**](https://github.com/mitya57/secretstorage)\* - 用于 `--cookies-from-browser` 在 **Linux** 上解密 **Chromium** 基于浏览器的 cookie 时访问 **Gnome** 密钥环。采用 [BSD-3-Clause](https://github.com/mitya57/secretstorage/blob/master/LICENSE) 许可
* 您想与 `--downloader` 一起使用的任何外部下载器

### 已弃用

* [**rtmpdump**](http://rtmpdump.mplayerhq.hu) - 用于下载 `rtmp` 流。可以使用 `--downloader ffmpeg` 代替 ffmpeg。采用 [GPLv2+](http://rtmpdump.mplayerhq.hu) 许可
* [**mplayer**](http://mplayerhq.hu/design7/info.html) 或 [**mpv**](https://mpv.io) - 用于下载 `rstp`/`mms` 流。可以使用 `--downloader ffmpeg` 代替 ffmpeg。采用 [GPLv2+](https://github.com/mpv-player/mpv/blob/master/Copyright) 许可

要使用或重新分发依赖项，您必须同意其各自的许可条款。

独立发布二进制文件是使用 Python 解释器和标有 **\*** 的包构建的。

如果您没有尝试的任务所需的必要依赖项，yt-dlp 会警告您。所有当前可用的依赖项在 `--verbose` 输出的顶部可见


## 编译

### 独立 PyInstaller 构建
要构建独立可执行文件，您必须拥有 Python 和 `pyinstaller`（如果需要，还包括 yt-dlp 的任何[可选依赖项](#dependencies)）。可执行文件将为与使用的 Python 相同的 CPU 架构构建。

您可以运行以下命令：

```
python devscripts/install_deps.py --include-group pyinstaller
python devscripts/make_lazy_extractors.py
python -m bundle.pyinstaller
```

在某些系统上，您可能需要使用 `py` 或 `python3` 代替 `python`。

`python -m bundle.pyinstaller` 接受可以传递给 `pyinstaller` 的任何参数，例如 `--onefile/-F` 或 `--onedir/-D`，这在[此处有进一步说明](https://pyinstaller.org/en/stable/usage.html#what-to-generate)。

**注意**：4.4 以下的 Pyinstaller 版本[不支持](https://github.com/pyinstaller/pyinstaller#requirements-and-tested-platforms)从 Windows 商店安装的 Python，除非使用虚拟环境。

**重要提示**：直接运行 `pyinstaller` **而不是**使用 `python -m bundle.pyinstaller` **不是**官方支持的。这可能无法正常工作。

### 平台无关二进制文件 (UNIX)
您需要构建工具 `python` (3.10+)、`zip`、`make` (GNU)、`pandoc`\* 和 `pytest`\*。

安装这些后，只需运行 `make`。

您也可以运行 `make yt-dlp` 来仅编译二进制文件而不更新任何附加文件。（标记有 **\*** 的构建工具不需要用于此操作）

### 相关脚本

* **`devscripts/install_deps.py`** - 为 yt-dlp 安装依赖项。
* **`devscripts/update-version.py`** - 根据当前日期更新版本号。
* **`devscripts/set-variant.py`** - 设置可执行文件的构建变体。
* **`devscripts/make_changelog.py`** - 使用简短的提交消息创建 markdown 更新日志并更新 `CONTRIBUTORS` 文件。
* **`devscripts/make_lazy_extractors.py`** - 创建延迟提取器。在构建二进制文件（任何变体）之前运行此操作将提高其启动性能。将环境变量 `YTDLP_NO_LAZY_EXTRACTORS` 设置为非空值以强制禁用延迟提取器加载。

注意：有关更多信息，请参阅它们的 `--help`。

### 分支项目
如果您在 GitHub 上分支该项目，您可以运行分支的[构建工作流](https://github.com/yt-dlp/yt-dlp/blob/master/.github/workflows/build.yml)以自动构建所选版本作为工件。或者，您可以运行[发布工作流](https://github.com/yt-dlp/yt-dlp/blob/master/.github/workflows/release.yml)或启用[nightly 工作流](https://github.com/yt-dlp/yt-dlp/blob/master/.github/workflows/release-nightly.yml)来创建完整的（预）发布版本。

# 使用和选项

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
    yt-dlp [OPTIONS] [--] URL [URL...]

提示：使用 `CTRL`+`F`（或 `Command`+`F`）按关键字搜索
<!-- MANPAGE: END EXCLUDED SECTION -->

<!-- Auto generated -->
## 常规选项：
    -h, --help                      打印此帮助文本并退出
    --version                       打印程序版本并退出
    -U, --update                    将此程序更新到最新版本
    --no-update                     不检查更新（默认）
    --update-to [CHANNEL]@[TAG]     升级/降级到特定版本。
                                    CHANNEL 也可以是仓库。如果省略，
                                    CHANNEL 和 TAG 分别默认为 "stable"
                                    和 "latest"；有关详细信息，请参阅
                                    "UPDATE"。支持的渠道：stable、
                                    nightly、master
    -i, --ignore-errors             忽略下载和后处理错误。
                                    即使后处理失败，下载也将被视为成功
    --no-abort-on-error             下载错误时继续下一个视频；
                                    例如，跳过播放列表中不可用的视频（默认）
    --abort-on-error                如果发生错误，中止进一步下载视频
                                    （别名：--no-ignore-errors）
    --list-extractors               列出所有支持的提取器并退出
    --extractor-descriptions        输出所有支持的提取器的描述并退出
    --use-extractors NAMES          要使用的提取器名称，用逗号分隔。
                                    您也可以使用正则表达式、"all"、"default"
                                    和 "end"（结束 URL 匹配）；例如 --ies
                                    "holodex.*,end,youtube"。在名称前加 "-"
                                    以排除它，例如 --ies
                                    default,-generic。使用 --list-extractors
                                    获取提取器名称列表。（别名：--ies）
    --default-search PREFIX         对不合格的 URL 使用此前缀。例如，
                                    "gvsearch2:python" 从 google videos
                                    下载两个搜索词为 "python" 的视频。
                                    使用值 "auto" 让 yt-dlp 猜测
                                    （"auto_warning" 在猜测时发出警告）。
                                    "error" 只是抛出错误。默认值
                                    "fixup_error" 修复损坏的 URL，但如果
                                    无法修复则发出错误而不是搜索
    --ignore-config                 不再加载任何配置文件，
                                    除了那些提供给 --config-locations 的文件。
                                    为了向后兼容，如果在系统配置文件中
                                    找到此选项，则不会加载用户配置。
                                    （别名：--no-config）
    --no-config-locations           不加载任何自定义配置文件（默认）。
                                    在配置文件中给出时，忽略当前文件中
                                    定义的所有以前的 --config-locations
    --config-locations PATH         主配置文件的位置；
                                    可以是配置文件的路径或其包含目录
                                    （"-" 表示 stdin）。可以多次使用
                                    并在其他配置文件中使用
    --plugin-dirs DIR               搜索插件的附加目录路径。
                                    此选项可以多次使用以添加多个目录。
                                    使用 "default" 搜索默认插件目录（默认）
    --no-plugin-dirs                清除要搜索的插件目录，
                                    包括默认目录和以前的 --plugin-dirs
                                    提供的目录
    --js-runtimes RUNTIME[:PATH]    要启用的其他 JavaScript 运行时，
                                    以及运行时的可选位置
                                    （二进制文件的路径或其包含目录）。
                                    此选项可以多次使用以启用多个运行时。
                                    支持的运行时（按优先级从高到低）：
                                    deno、node、quickjs、bun。默认情况下
                                    只启用 "deno"。将使用已启用且可用的
                                    最高优先级运行时。要在 "deno" 可用时
                                    使用较低优先级的运行时，需要在启用
                                    其他运行时之前传递 --no-js-runtimes
    --no-js-runtimes                清除要启用的 JavaScript 运行时，
                                    包括默认运行时和以前的 --js-runtimes
                                    提供的运行时
    --remote-components COMPONENT   允许 yt-dlp 在需要时获取的远程组件。
                                    如果您使用的是官方可执行文件或已安装
                                    所需版本的 yt-dlp-ejs 包，则目前
                                    不需要此选项。您可以多次使用此选项
                                    以允许多个组件。支持的值：
                                    ejs:npm（来自 npm 的外部 JavaScript 组件）、
                                    ejs:github（来自 yt-dlp-ejs GitHub 的
                                    外部 JavaScript 组件）。默认情况下，
                                    不允许任何远程组件
    --no-remote-components          禁止获取所有远程组件，
                                    包括以前由 --remote-components 或默认值
                                    允许的任何组件。
    --flat-playlist                 不提取播放列表的 URL 结果条目；
                                    某些条目元数据可能缺失，下载可能会被跳过
    --no-flat-playlist              完全提取播放列表的视频（默认）
    --live-from-start               从开始下载直播流。
                                    目前是实验性的，仅支持 YouTube、
                                    Twitch 和 TVer
    --no-live-from-start            从当前时间下载直播流（默认）
    --wait-for-video MIN[-MAX]      等待计划的流变得可用。
                                    传递重试之间等待的最少秒数（或范围）
    --no-wait-for-video             不等待计划的流（默认）
    --mark-watched                  标记视频为已观看（即使使用 --simulate）
    --no-mark-watched               不标记视频为已观看（默认）
    --color [STREAM:]POLICY         是否在输出中发出颜色代码，
                                    可选择以 STREAM（stdout 或 stderr）
                                    为前缀以应用设置。可以是 "always"、
                                    "auto"（默认）、"never" 或
                                    "no_color"（使用非颜色终端序列）。
                                    使用 "auto-tty" 或 "no_color-tty"
                                    仅根据终端支持决定。可以多次使用
    --compat-options OPTS           可以通过恢复 yt-dlp 中的一些更改
                                    来帮助保持与 youtube-dl 或 youtube-dlc
                                    配置兼容性的选项。有关详细信息，
                                    请参阅"默认行为的差异"
    --alias ALIASES OPTIONS         为选项字符串创建别名。除非别名
                                    以破折号 "-" 开头，否则会加上 "--" 前缀。
                                    参数根据 Python 字符串格式化迷你语言
                                    进行解析。例如 --alias get-audio,-X "-S
                                    aext:{0},abr -x --audio-format {0}" 创建
                                    选项 "--get-audio" 和 "-X"，它们接受
                                    参数 (ARG0) 并扩展为 "-S
                                    aext:ARG0,abr -x --audio-format ARG0"。
                                    所有定义的别名都在 --help 输出中列出。
                                    别名选项可以触发更多别名；因此要小心
                                    避免定义递归选项。作为安全措施，
                                    每个别名最多可以触发 100 次。
                                    此选项可以多次使用
    -t, --preset-alias PRESET       应用预定义的选项集。例如，
                                    --preset-alias mp3。可用的预设有：
                                    mp3、aac、mp4、mkv、sleep。
                                    有关更多信息，请参阅末尾的
                                    "预设别名"部分。此选项可以多次使用

## 网络选项：
    --proxy URL                     使用指定的 HTTP/HTTPS/SOCKS 代理。要
                                    启用 SOCKS 代理，请指定适当的方案，
                                    例如 socks5://user:pass@127.0.0.1:1080/。
                                    传递空字符串 (--proxy "") 进行
                                    直接连接
    --socket-timeout SECONDS        放弃前等待的时间，以秒为单位
    --source-address IP             要绑定的客户端 IP 地址
    --impersonate CLIENT[:OS]       要模拟请求的客户端。例如，
                                    chrome、chrome-110、chrome:windows-10。
                                    传递 --impersonate="" 以模拟任何客户端。
                                    请注意，强制对所有请求进行模拟可能会对
                                    下载速度和稳定性产生不利影响
    --list-impersonate-targets      列出可用的模拟客户端。
    -4, --force-ipv4                通过 IPv4 建立所有连接
    -6, --force-ipv6                通过 IPv6 建立所有连接
    --enable-file-urls              启用 file:// URL。出于安全原因，
                                    默认情况下禁用此功能。

## 地理限制：
    --geo-verification-proxy URL    使用此代理来验证某些地理限制网站的
                                    IP 地址。由 --proxy 指定的默认代理
                                   （如果选项不存在，则为无）用于
                                    实际下载
    --xff VALUE                     如何伪造 X-Forwarded-For HTTP 标头以
                                    尝试绕过地理限制。可以是以下之一：
                                    "default"（仅在已知有用时）、
                                    "never"、CIDR 表示法中的 IP 块，
                                    或两个字母的 ISO 3166-2 国家代码

## 视频选择：
    -I, --playlist-items ITEM_SPEC  要下载的项目的逗号分隔的 playlist_index。
                                    您可以使用 "[START]:[STOP][:STEP]" 指定范围。
                                    为了向后兼容，也支持 START-STOP。
                                    使用负索引从右侧计数，使用负 STEP
                                    以相反顺序下载。例如，在大小为 15 的
                                    播放列表上使用 "-I 1:3,7,-5::2" 将下载
                                    索引为 1,2,3,7,11,13,15 的项目
    --min-filesize SIZE             如果文件大小小于 SIZE，则中止下载，
                                    例如 50k 或 44.6M
    --max-filesize SIZE             如果文件大小大于 SIZE，则中止下载，
                                    例如 50k 或 44.6M
    --date DATE                     仅下载在此日期上传的视频。
                                    日期可以是 "YYYYMMDD" 或格式
                                    [now|today|yesterday][-N[day|week|month|year]]。
                                    例如，"--date today-2weeks" 仅下载
                                    两周前同一天上传的视频
    --datebefore DATE               仅下载在此日期或之前上传的视频。
                                    接受的日期格式与 --date 相同
    --dateafter DATE                仅下载在此日期或之后上传的视频。
                                    接受的日期格式与 --date 相同
    --match-filters FILTER          通用视频过滤器。可以使用"过滤格式"中
                                    定义的运算符将任何"输出模板"字段与
                                    数字或字符串进行比较。您也可以简单地
                                    指定一个字段以在字段存在时进行匹配，
                                    使用 "!field" 检查字段是否不存在，
                                    使用 "&" 检查多个条件。如果需要，
                                    使用 "\" 转义 "&" 或引号。如果多次使用，
                                    则如果至少满足一个条件，则过滤器匹配。
                                    例如，--match-filters
                                    !is_live --match-filters "like_count>?100 &
                                    description~='(?i)\bcats \& dogs\b'" 仅匹配
                                    非直播视频或点赞数超过 100（或点赞
                                    字段不可用）且描述包含短语"cats &
                                    dogs"（不区分大小写）的视频。
                                    使用 "--match-filters -" 交互式询问
                                    是否下载每个视频
    --no-match-filters              不使用任何 --match-filters（默认）
    --break-match-filters FILTER    与 "--match-filters" 相同，但在拒绝
                                    视频时停止下载过程
    --no-break-match-filters        不使用任何 --break-match-filters（默认）
    --no-playlist                   如果 URL 指向视频和播放列表，则仅
                                    下载视频
    --yes-playlist                  如果 URL 指向视频和播放列表，则
                                    下载播放列表
    --age-limit YEARS               仅下载适合指定年龄的视频
    --download-archive FILE         仅下载未在存档文件中列出的视频。
                                    在其中记录所有下载的视频的 ID
    --no-download-archive           不使用存档文件（默认）
    --max-downloads NUMBER          下载 NUMBER 个文件后中止
    --break-on-existing             遇到 --download-archive 选项提供的
                                    存档中的文件时停止下载过程
    --no-break-on-existing          遇到存档中的文件时不停止下载过程
                                    （默认）
    --break-per-input               更改 --max-downloads、--break-on-existing、
                                    --break-match-filters 和 autonumber 以
                                    按输入 URL 重置
    --no-break-per-input            --break-on-existing 和类似选项
                                    终止整个下载队列
    --skip-playlist-after-errors N  允许的失败次数，之后跳过播放列表的其余部分

## 下载选项：
    -N, --concurrent-fragments N    应该并发下载的 dash/hlsnative 视频
                                    片段数（默认为 1）
    -r, --limit-rate RATE           最大下载速率（字节/秒），
                                    例如 50K 或 4.2M
    --throttled-rate RATE           最小下载速率（字节/秒），
                                    低于此速率时假定存在限速并重新提取
                                    视频数据，例如 100K
    -R, --retries RETRIES           重试次数（默认为 10）或
                                    "infinite"（无限）
    --file-access-retries RETRIES   文件访问错误时的重试次数
                                    （默认为 3）或 "infinite"（无限）
    --fragment-retries RETRIES      片段的重试次数（默认为 10）或
                                    "infinite"（无限）（DASH、hlsnative 和 ISM）
    --retry-sleep [TYPE:]EXPR       重试之间的休眠时间（秒），
                                    （可选）以重试类型为前缀
                                    （http（默认）、fragment、file_access、
                                    extractor）以应用休眠。EXPR 可以是数字、
                                    linear=START[:END[:STEP=1]] 或
                                    exp=START[:END[:BASE=2]]。此选项可以
                                    多次使用以设置不同重试类型的休眠时间，
                                    例如 --retry-sleep
                                    linear=1::2 --retry-sleep fragment:exp=1:20
    --skip-unavailable-fragments    跳过 DASH、hlsnative 和 ISM 下载的
                                    不可用片段（默认）
                                    （别名：--no-abort-on-unavailable-fragments）
    --abort-on-unavailable-fragments
                                    如果片段不可用则中止下载
                                    （别名：--no-skip-unavailable-fragments）
    --keep-fragments                下载完成后在磁盘上保留下载的片段
    --no-keep-fragments             下载完成后删除下载的片段（默认）
    --buffer-size SIZE              下载缓冲区的大小，例如 1024 或 16K
                                    （默认为 1024）
    --resize-buffer                 缓冲区大小从 --buffer-size 的初始值
                                    自动调整（默认）
    --no-resize-buffer              不自动调整缓冲区大小
    --http-chunk-size SIZE          基于块的 HTTP 下载的块大小，
                                    例如 10485760 或 10M（默认禁用）。
                                    可能有助于绕过 Web 服务器施加的带宽限制
                                    （实验性）
    --playlist-random               以随机顺序下载播放列表视频
    --lazy-playlist                 在接收播放列表条目时进行处理。
                                    这会禁用 n_entries、
                                    --playlist-random 和 --playlist-reverse
    --no-lazy-playlist              仅在解析整个播放列表后处理
                                    播放列表中的视频（默认）
    --hls-use-mpegts                对 HLS 视频使用 mpegts 容器；
                                    允许某些播放器在下载时播放视频，
                                    并在下载中断时减少文件损坏的机会。
                                    对于直播流，默认启用此功能
    --no-hls-use-mpegts             对 HLS 视频不使用 mpegts 容器。
                                    不下载直播流时这是默认设置
    --download-sections REGEX       仅下载与正则表达式匹配的章节。
                                    "*" 前缀表示时间范围而不是章节。
                                    负时间戳从末尾计算。
                                    "*from-url" 可用于在从 URL 提取的
                                    "start_time" 和 "end_time" 之间下载。
                                    需要 ffmpeg。此选项可以多次使用
                                    以下载多个章节，例如 --download-sections
                                    "*10:15-inf" --download-sections "intro"
    --downloader [PROTO:]NAME       要使用的外部下载器的名称或路径
                                    （可选）以协议
                                    （http、ftp、m3u8、dash、rstp、rtmp、mms）
                                    为前缀以用于该协议。目前支持 native、
                                    aria2c、axel、curl、ffmpeg、httpie、wget。
                                    您可以多次使用此选项为不同协议
                                    设置不同的下载器。例如 --downloader aria2c
                                    --downloader "dash,m3u8:native" 将使用
                                    aria2c 进行 http/ftp 下载，使用
                                    原生下载器进行 dash/m3u8 下载
                                    （别名：--external-downloader）
    --downloader-args NAME:ARGS     将这些参数传递给外部下载器。
                                    指定下载器名称和参数，用冒号 ":" 分隔。
                                    对于 ffmpeg，可以使用与
                                    --postprocessor-args 相同的语法
                                    将参数传递到不同位置。您可以多次使用
                                    此选项为不同的下载器提供不同的参数
                                    （别名：--external-downloader-args）

## 文件系统选项：
    -a, --batch-file FILE           包含要下载的 URL 的文件（"-" 表示
                                    stdin），每行一个 URL。以 "#"、";" 或 "]"
                                    开头的行被视为注释并被忽略
    --no-batch-file                 不从批处理文件读取 URL（默认）
    -P, --paths [TYPES:]PATH        文件应下载到的路径。
                                    指定文件类型和路径，用冒号 ":" 分隔。
                                    支持与 --output 相同的所有 TYPES。
                                    此外，您还可以提供 "home"（默认）
                                    和 "temp" 路径。所有中间文件首先
                                    下载到 temp 路径，然后在下载完成后
                                    将最终文件移动到 home 路径。
                                    如果 --output 是绝对路径，则忽略此选项
    -o, --output [TYPES:]TEMPLATE   输出文件名模板；有关详细信息，请参阅
                                    "输出模板"
    --output-na-placeholder TEXT    --output 中不可用字段的占位符
                                    （默认："NA"）
    --restrict-filenames            将文件名限制为仅 ASCII 字符，
                                    并避免文件名中的 "&" 和空格
    --no-restrict-filenames         允许文件名中使用 Unicode 字符、"&" 和
                                    空格（默认）
    --windows-filenames             强制文件名与 Windows 兼容
    --no-windows-filenames          仅最小程度地清理文件名
    --trim-filenames LENGTH         将文件名长度（不包括扩展名）限制为
                                    指定的字符数
    -w, --no-overwrites             不覆盖任何文件
    --force-overwrites              覆盖所有视频和元数据文件。
                                    此选项包括 --no-continue
    --no-force-overwrites           不覆盖视频，但覆盖相关文件（默认）
    -c, --continue                  恢复部分下载的文件/片段（默认）
    --no-continue                   不恢复部分下载的片段。
                                    如果文件未分段，则重新开始下载整个文件
    --part                          使用 .part 文件而不是直接写入
                                    输出文件（默认）
    --no-part                       不使用 .part 文件 - 直接写入
                                    输出文件
    --mtime                         使用 Last-modified 标头设置文件
                                    修改时间
    --no-mtime                      不使用 Last-modified 标头设置
                                    文件修改时间（默认）
    --write-description             将视频描述写入 .description 文件
    --no-write-description          不写入视频描述（默认）
    --write-info-json               将视频元数据写入 .info.json 文件
                                    （这可能包含个人信息）
    --no-write-info-json            不写入视频元数据（默认）
    --write-playlist-metafiles      在使用 --write-info-json、
                                    --write-description 等时，除了视频元数据外，
                                    还写入播放列表元数据（默认）
    --no-write-playlist-metafiles   在使用 --write-info-json、
                                    --write-description 等时不写入
                                    播放列表元数据
    --clean-info-json               从 infojson 中删除一些内部元数据，
                                    例如文件名（默认）
    --no-clean-info-json            将所有字段写入 infojson
    --write-comments                获取视频评论以放入 infojson。
                                    即使不使用此选项，如果提取已知很快，
                                    也会获取评论（别名：--get-comments）
    --no-write-comments             不获取视频评论，除非提取已知很快
                                    （别名：--no-get-comments）
    --load-info-json FILE           包含视频信息的 JSON 文件
                                    （使用 "--write-info-json" 选项创建）
    --cookies FILE                  Netscape 格式的文件，用于从中读取
                                    cookie 并在其中转储 cookie jar
    --no-cookies                    不从/向文件读取/转储 cookie（默认）
    --cookies-from-browser BROWSER[+KEYRING][:PROFILE][::CONTAINER]
                                    要从中加载 cookie 的浏览器名称。
                                    目前支持的浏览器有：
                                    brave、chrome、chromium、edge、firefox、
                                    opera、safari、vivaldi、whale。可选地，
                                    可以使用各自的分隔符提供用于在 Linux 上
                                    解密 Chromium cookie 的 KEYRING、
                                    要从中加载 cookie 的 PROFILE 的名称/路径，
                                    以及 CONTAINER 名称（如果是 Firefox）
                                    （"none" 表示无容器）。默认情况下，
                                    使用最近访问的配置文件的所有容器。
                                    目前支持的密钥环有：basictext、
                                    gnomekeyring、kwallet、kwallet5、kwallet6
    --no-cookies-from-browser       不从浏览器加载 cookie（默认）
    --cache-dir DIR                 yt-dlp 可以永久存储某些下载信息
                                    （例如客户端 ID 和签名）的文件系统位置。
                                    默认为 ${XDG_CACHE_HOME}/yt-dlp
    --no-cache-dir                  禁用文件系统缓存
    --rm-cache-dir                  删除所有文件系统缓存文件

## 缩略图选项：
    --write-thumbnail               将缩略图图像写入磁盘
    --no-write-thumbnail            不将缩略图图像写入磁盘（默认）
    --write-all-thumbnails          将所有缩略图图像格式写入磁盘
    --list-thumbnails               列出每个视频的可用缩略图。
                                    除非使用 --no-simulate，否则模拟

## 互联网快捷方式选项：
    --write-link                    写入互联网快捷方式文件，取决于
                                    当前平台（.url、.webloc 或
                                    .desktop）。URL 可能被操作系统缓存
    --write-url-link                写入 .url Windows 互联网快捷方式。
                                    操作系统根据文件路径缓存 URL
    --write-webloc-link             写入 .webloc macOS 互联网快捷方式
    --write-desktop-link            写入 .desktop Linux 互联网快捷方式

## 详细信息和模拟选项：
    -q, --quiet                     激活静默模式。如果与 --verbose 一起使用，
                                    则将日志打印到 stderr
    --no-quiet                      停用静默模式。（默认）
    --no-warnings                   忽略警告
    -s, --simulate                  不下载视频，也不向磁盘写入任何内容
    --no-simulate                   即使使用打印/列出选项也下载视频
    --ignore-no-formats-error       忽略"无视频格式"错误。对于
                                    提取元数据很有用，即使视频实际上
                                    无法下载（实验性）
    --no-ignore-no-formats-error    当找不到可下载的视频格式时
                                    抛出错误（默认）
    --skip-download                 不下载视频，但写入所有相关文件
                                    （别名：--no-download）
    -O, --print [WHEN:]TEMPLATE     要打印到屏幕的字段名或输出模板，
                                    可选择以打印时间（用 ":" 分隔）为前缀。
                                    "WHEN" 的支持值与 --use-postprocessor
                                    相同（默认：video）。意味着 --quiet。
                                    意味着 --simulate，除非使用
                                    --no-simulate 或 WHEN 的后续阶段。
                                    此选项可以多次使用
    --print-to-file [WHEN:]TEMPLATE FILE
                                    将给定模板附加到文件。WHEN 和 TEMPLATE
                                    的值与 --print 相同。FILE 使用与
                                    输出模板相同的语法。此选项可以多次使用
    -j, --dump-json                 静默，但为每个视频打印 JSON 信息。
                                    除非使用 --no-simulate，否则模拟。
                                    有关可用键的说明，请参阅"输出模板"
    -J, --dump-single-json          静默，但为每个传递的 URL 或 infojson
                                    打印 JSON 信息。除非使用 --no-simulate，
                                    否则模拟。如果 URL 指向播放列表，
                                    则整个播放列表信息在一行中转储
    --force-write-archive           强制写入下载存档条目，只要不发生错误，
                                    即使使用 -s 或其他模拟选项
                                    （别名：--force-download-archive）
    --newline                       将进度条作为新行输出
    --no-progress                   不打印进度条
    --progress                      显示进度条，即使在静默模式下
    --console-title                 在控制台标题栏中显示进度
    --progress-template [TYPES:]TEMPLATE
                                    进度输出的模板，可选择以以下之一为前缀：
                                    "download:"（默认）、"download-title:"
                                    （控制台标题）、"postprocess:" 或
                                    "postprocess-title:"。视频字段可在
                                    "info" 键下访问，进度属性可在
                                    "progress" 键下访问。例如
                                    --console-title --progress-template
                                    "download-title:%(info.id)s-%(progress.eta)s"
    --progress-delta SECONDS        进度输出之间的时间（默认：0）
    -v, --verbose                   打印各种调试信息
    --dump-pages                    打印使用 base64 编码的下载页面以
                                    调试问题（非常详细）
    --write-pages                   将下载的中间页面写入当前目录中的
                                    文件以调试问题
    --print-traffic                 显示发送和读取的 HTTP 流量

## 变通方法：
    --encoding ENCODING             强制指定的编码（实验性）
    --legacy-server-connect         明确允许与不支持 RFC 5746 安全
                                    重新协商的服务器建立 HTTPS 连接
    --no-check-certificates         禁止 HTTPS 证书验证
    --prefer-insecure               使用未加密的连接来检索视频信息
                                    （目前仅支持 YouTube）
    --add-headers FIELD:VALUE       指定自定义 HTTP 标头及其值，
                                    用冒号 ":" 分隔。您可以多次使用此选项
    --bidi-workaround               解决缺乏双向文本支持的终端问题。
                                    需要 PATH 中的 bidiv 或 fribidi 可执行文件
    --sleep-requests SECONDS        数据提取期间请求之间的休眠秒数
    --sleep-interval SECONDS        每次下载前的休眠秒数。
                                    与 --max-sleep-interval 一起使用时
                                    这是最小休眠时间（别名：--min-sleep-interval）
    --max-sleep-interval SECONDS    最大休眠秒数。只能与
                                    --min-sleep-interval 一起使用
    --sleep-subtitles SECONDS       每次字幕下载前的休眠秒数

## 视频格式选项：
    -f, --format FORMAT             视频格式代码，有关详细信息，请参阅
                                    "格式选择"
    -S, --format-sort SORTORDER     按给定字段对格式进行排序，有关
                                    详细信息，请参阅"排序格式"
    --format-sort-reset             忽略以前用户指定的排序顺序并
                                    重置为默认值
    --format-sort-force             强制用户指定的排序顺序优先于
                                    所有字段，有关详细信息，请参阅"排序格式"
                                    （别名：--S-force）
    --no-format-sort-force          某些字段优先于用户指定的排序顺序（默认）
    --video-multistreams            允许将多个视频流合并到单个文件中
    --no-video-multistreams         每个输出文件仅下载一个视频流（默认）
    --audio-multistreams            允许将多个音频流合并到单个文件中
    --no-audio-multistreams         每个输出文件仅下载一个音频流（默认）
    --prefer-free-formats           优先选择具有免费容器的视频格式，
                                    而不是相同质量的非免费容器。
                                    与 "-S ext" 一起使用以严格优先选择
                                    免费容器，而不考虑质量
    --no-prefer-free-formats        不对免费容器给予任何特殊偏好（默认）
    --check-formats                 确保仅从实际可下载的格式中选择格式
    --check-all-formats             检查所有格式是否实际可下载
    --no-check-formats              不检查格式是否实际可下载
    -F, --list-formats              列出每个视频的可用格式。
                                    除非使用 --no-simulate，否则模拟
    --merge-output-format FORMAT    合并格式时可能使用的容器，用 "/" 分隔，
                                    例如 "mp4/mkv"。如果不需要合并，则忽略。
                                    （目前支持：avi、flv、mkv、mov、mp4、webm）

## 字幕选项：
    --write-subs                    写入字幕文件
    --no-write-subs                 不写入字幕文件（默认）
    --write-auto-subs               写入自动生成的字幕文件
                                    （别名：--write-automatic-subs）
    --no-write-auto-subs            不写入自动生成的字幕
                                    （默认）（别名：--no-write-automatic-subs）
    --list-subs                     列出每个视频的可用字幕。
                                    除非使用 --no-simulate，否则模拟
    --sub-format FORMAT             字幕格式；接受用 "/" 分隔的格式偏好，
                                    例如 "srt" 或 "ass/srt/best"
    --sub-langs LANGS               要下载的字幕语言（可以是正则表达式）
                                    或 "all"，用逗号分隔，例如
                                    --sub-langs "en.*,ja"（其中 "en.*" 是
                                    匹配 "en" 后跟 0 个或多个任意字符的
                                    正则表达式模式）。您可以在语言代码前
                                    加 "-" 以将其从请求的语言中排除，
                                    例如 --sub-langs all,-live_chat。
                                    使用 --list-subs 获取可用语言标签列表

## 身份验证选项：
    -u, --username USERNAME         使用此帐户 ID 登录
    -p, --password PASSWORD         帐户密码。如果省略此选项，yt-dlp 将
                                    交互式询问
    -2, --twofactor TWOFACTOR       双因素身份验证代码
    -n, --netrc                     使用 .netrc 身份验证数据
    --netrc-location PATH           .netrc 身份验证数据的位置；
                                    可以是路径或其包含目录。
                                    默认为 ~/.netrc
    --netrc-cmd NETRC_CMD           要执行的命令以获取提取器的凭据。
    --video-password PASSWORD       视频特定密码
    --ap-mso MSO                    Adobe Pass 多系统运营商（电视
                                    提供商）标识符，使用 --ap-list-mso
                                    获取可用 MSO 列表
    --ap-username USERNAME          多系统运营商帐户登录
    --ap-password PASSWORD          多系统运营商帐户密码。
                                    如果省略此选项，yt-dlp 将交互式询问
    --ap-list-mso                   列出所有支持的多系统运营商
    --client-certificate CERTFILE   PEM 格式的客户端证书文件路径。
                                    可能包括私钥
    --client-certificate-key KEYFILE
                                    客户端证书的私钥文件路径
    --client-certificate-password PASSWORD
                                    客户端证书私钥的密码（如果已加密）。
                                    如果未提供且密钥已加密，yt-dlp 将
                                    交互式询问

## 后处理选项：
    -x, --extract-audio             将视频文件转换为仅音频文件
                                    （需要 ffmpeg 和 ffprobe）
    --audio-format FORMAT           使用 -x 时将音频转换为的格式。
                                    （目前支持：best（默认）、aac、alac、
                                    flac、m4a、mp3、opus、vorbis、wav）。
                                    您可以使用与 --remux-video 类似的语法
                                    指定多个规则
    --audio-quality QUALITY         指定使用 -x 转换音频时要使用的
                                    ffmpeg 音频质量。插入 0（最佳）到 10（最差）
                                    之间的值以进行 VBR 或特定比特率，如 128K
                                    （默认为 5）
    --remux-video FORMAT            如有必要，将视频重新封装到另一个容器中
                                    （目前支持：avi、flv、gif、mkv、mov、mp4、
                                    webm、aac、aiff、alac、flac、m4a、mka、mp3、
                                    ogg、opus、vorbis、wav）。如果目标容器
                                    不支持视频/音频编解码器，重新封装将失败。
                                    您可以指定多个规则；例如
                                    "aac>m4a/mov>mp4/mkv" 将把 aac 重新封装为 m4a，
                                    mov 重新封装为 mp4，其他所有内容重新封装为 mkv
    --recode-video FORMAT           如有必要，将视频重新编码为另一种格式。
                                    语法和支持的格式与 --remux-video 相同
    --postprocessor-args NAME:ARGS  将这些参数传递给后处理器。
                                    指定后处理器/可执行文件名称和参数，
                                    用冒号 ":" 分隔，以将参数传递给指定的
                                    后处理器/可执行文件。支持的后处理器有：
                                    Merger、ModifyChapters、SplitChapters、
                                    ExtractAudio、VideoRemuxer、VideoConvertor、
                                    Metadata、EmbedSubtitle、EmbedThumbnail、
                                    SubtitlesConvertor、ThumbnailsConvertor、
                                    FixupStretched、FixupM4a、FixupM3u8、
                                    FixupTimestamp 和 FixupDuration。支持的
                                    可执行文件有：AtomicParsley、FFmpeg 和 FFprobe。
                                    您还可以指定 "PP+EXE:ARGS" 以仅在由
                                    指定的后处理器使用时将参数传递给
                                    指定的可执行文件。此外，对于 ffmpeg/ffprobe，
                                    可以在前缀后附加 "_i"/"_o"，可选择后跟
                                    一个数字，以便在指定的输入/输出文件之前
                                    传递参数，例如 --ppa
                                    "Merger+ffmpeg_i1:-v quiet"。您可以多次使用
                                    此选项为不同的后处理器提供不同的参数。
                                    （别名：--ppa）
    -k, --keep-video                后处理后将中间视频文件保留在磁盘上
    --no-keep-video                 后处理后删除中间视频文件（默认）
    --post-overwrites               覆盖后处理的文件（默认）
    --no-post-overwrites            不覆盖后处理的文件
    --embed-subs                    将字幕嵌入视频中（仅适用于 mp4、
                                    webm 和 mkv 视频）
    --no-embed-subs                 不嵌入字幕（默认）
    --embed-thumbnail               将缩略图嵌入视频作为封面艺术
    --no-embed-thumbnail            不嵌入缩略图（默认）
    --embed-metadata                将元数据嵌入视频文件。
                                    如果存在，还会嵌入章节/infojson，
                                    除非使用 --no-embed-chapters/--no-embed-info-json
                                    （别名：--add-metadata）
    --no-embed-metadata             不将元数据添加到文件（默认）
                                    （别名：--no-add-metadata）
    --embed-chapters                将章节标记添加到视频文件
                                    （别名：--add-chapters）
    --no-embed-chapters             不添加章节标记（默认）
                                    （别名：--no-add-chapters）
    --embed-info-json               将 infojson 作为附件嵌入
                                    mkv/mka 视频文件
    --no-embed-info-json            不将 infojson 作为附件嵌入
                                    视频文件
    --parse-metadata [WHEN:]FROM:TO
                                    从其他字段解析其他元数据，如标题/艺术家；
                                    有关详细信息，请参阅"修改元数据"。
                                    "WHEN" 的支持值与 --use-postprocessor 相同
                                    （默认：pre_process）
    --replace-in-metadata [WHEN:]FIELDS REGEX REPLACE
                                    使用给定的正则表达式替换元数据字段中的
                                    文本。此选项可以多次使用。
                                    "WHEN" 的支持值与 --use-postprocessor 相同
                                    （默认：pre_process）
    --xattrs                        将元数据写入视频文件的 xattrs
                                    （使用 Dublin Core 和 XDG 标准）
    --concat-playlist POLICY        连接播放列表中的视频。可以是以下之一：
                                    "never"、"always" 或 "multi_video"
                                    （默认；仅当视频形成单个节目时）。
                                    所有视频文件必须具有相同的编解码器和
                                    流数才能连接。"pl_video:" 前缀可以与
                                    "--paths" 和 "--output" 一起使用以设置
                                    连接文件的输出文件名。有关详细信息，
                                    请参阅"输出模板"
    --fixup POLICY                  自动更正文件的已知故障。
                                    可以是以下之一：never（不执行任何操作）、
                                    warn（仅发出警告）、detect_or_warn（默认；
                                    如果可以，修复文件，否则发出警告）、
                                    force（即使文件已存在也尝试修复）
    --ffmpeg-location PATH          ffmpeg 二进制文件的位置；
                                    可以是二进制文件的路径或其包含目录
    --exec [WHEN:]CMD               执行命令，可选择以执行时间（用 ":" 分隔）
                                    为前缀。"WHEN" 的支持值与
                                    --use-postprocessor 相同（默认：after_move）。
                                    可以使用与输出模板相同的语法将任何字段
                                    作为参数传递给命令。如果未传递任何字段，
                                    则将 %(filepath,_filename|)q 附加到
                                    命令末尾。此选项可以多次使用
    --no-exec                       删除任何以前定义的 --exec
    --convert-subs FORMAT           将字幕转换为另一种格式
                                    （目前支持：ass、lrc、srt、vtt）。
                                    使用 "--convert-subs none" 禁用转换
                                    （默认）（别名：--convert-subtitles）
    --convert-thumbnails FORMAT     将缩略图转换为另一种格式
                                    （目前支持：jpg、png、webp）。
                                    您可以使用与 "--remux-video" 类似的语法
                                    指定多个规则。使用 "--convert-thumbnails none"
                                    禁用转换（默认）
    --split-chapters                根据内部章节将视频拆分为多个文件。
                                    "chapter:" 前缀可以与 "--paths" 和 "--output"
                                    一起使用以设置拆分文件的输出文件名。
                                    有关详细信息，请参阅"输出模板"
    --no-split-chapters             不根据章节拆分视频（默认）
    --remove-chapters REGEX         删除标题与给定正则表达式匹配的章节。
                                    语法与 --download-sections 相同。
                                    此选项可以多次使用
    --no-remove-chapters            不从文件中删除任何章节（默认）
    --force-keyframes-at-cuts       在下载/拆分/删除章节时在切口处强制关键帧。
                                    由于需要重新编码，这很慢，但结果视频
                                    在切口周围可能具有更少的伪影
    --no-force-keyframes-at-cuts    在切割/拆分时不强制章节周围的关键帧
                                    （默认）
    --use-postprocessor NAME[:ARGS]
                                    要启用的插件后处理器的（区分大小写）名称，
                                    以及（可选）要传递给它的参数，用冒号 ":" 分隔。
                                    ARGS 是用分号 ";" 分隔的 NAME=VALUE 列表。
                                    "when" 参数确定何时调用后处理器。
                                    可以是以下之一："pre_process"（视频提取后）、
                                    "after_filter"（视频通过过滤器后）、
                                    "video"（--format 之后；--print/--output 之前）、
                                    "before_dl"（每次视频下载之前）、
                                    "post_process"（每次视频下载后；默认）、
                                    "after_move"（将视频文件移动到其最终位置后）、
                                    "after_video"（下载和处理视频的所有格式后）
                                    或 "playlist"（播放列表结束时）。
                                    此选项可以多次使用以添加不同的后处理器

## SponsorBlock 选项：
使用 [SponsorBlock API](https://sponsor.ajay.app) 为下载的 YouTube 视频
    创建章节条目或删除各种片段（赞助商、介绍等）

    --sponsorblock-mark CATS        要为其创建章节的 SponsorBlock 类别，
                                    用逗号分隔。可用类别有 sponsor、intro、outro、
                                    selfpromo、preview、filler、interaction、
                                    music_offtopic、hook、poi_highlight、
                                    chapter、all 和 default (=all)。您可以在
                                    类别前加 "-" 以将其排除。
                                    有关类别的说明，请参阅 [1]。
                                    例如 --sponsorblock-mark all,-preview
                                    [1] https://wiki.sponsor.ajay.app/w/Segment_Categories
    --sponsorblock-remove CATS      要从视频文件中删除的 SponsorBlock 类别，
                                    用逗号分隔。如果一个类别同时存在于标记和删除中，
                                    remove 优先。语法和可用类别与
                                    --sponsorblock-mark 相同，只是 "default"
                                    指的是 "all,-filler"，并且 poi_highlight、
                                    chapter 不可用
    --sponsorblock-chapter-title TEMPLATE
                                    由 --sponsorblock-mark 创建的 SponsorBlock
                                    章节标题的输出模板。唯一可用的字段是
                                    start_time、end_time、category、
                                    categories、name、category_names。默认为
                                    "[SponsorBlock]: %(category_names)l"
    --no-sponsorblock               禁用 --sponsorblock-mark 和
                                    --sponsorblock-remove
    --sponsorblock-api URL          SponsorBlock API 位置，默认为
                                    https://sponsor.ajay.app

## 提取器选项：
    --extractor-retries RETRIES     已知提取器错误的重试次数
                                    （默认为 3）或 "infinite"（无限）
    --allow-dynamic-mpd             处理动态 DASH 清单（默认）
                                    （别名：--no-ignore-dynamic-mpd）
    --ignore-dynamic-mpd            不处理动态 DASH 清单
                                    （别名：--no-allow-dynamic-mpd）
    --hls-split-discontinuity       在不连续处（如广告中断）将 HLS 播放列表
                                    拆分为不同格式
    --no-hls-split-discontinuity    在不连续处（如广告中断）不将 HLS 播放列表
                                    拆分为不同格式（默认）
    --extractor-args IE_KEY:ARGS    将 ARGS 参数传递给 IE_KEY 提取器。
                                    有关详细信息，请参阅"提取器参数"。
                                    您可以多次使用此选项为不同的提取器提供参数

## 预设别名：
为方便和易用而预定义的别名。请注意，未来版本的 yt-dlp 可能会
    添加或调整预设，但现有的预设名称不会被更改或删除

    -t mp3                          -f 'ba[acodec^=mp3]/ba/b' -x --audio-format
                                    mp3

    -t aac                          -f
                                    'ba[acodec^=aac]/ba[acodec^=mp4a.40.]/ba/b'
                                    -x --audio-format aac

    -t mp4                          --merge-output-format mp4 --remux-video mp4
                                    -S vcodec:h264,lang,quality,res,fps,hdr:12,a
                                    codec:aac

    -t mkv                          --merge-output-format mkv --remux-video mkv

    -t sleep                        --sleep-subtitles 5 --sleep-requests 0.75
                                    --sleep-interval 10 --max-sleep-interval 20

# 配置

您可以通过在配置文件中放置任何支持的命令行选项来配置 yt-dlp。配置从以下位置加载：

1. **主配置**：
    * 给定给 `--config-locations` 的文件
1. **便携式配置**：（推荐用于便携式安装）
    * 如果使用二进制文件，则二进制文件所在目录中的 `yt-dlp.conf`
    * 如果从源代码运行，则 `yt_dlp` 父目录中的 `yt-dlp.conf`
1. **主目录配置**：
    * 给定给 `-P` 的主路径中的 `yt-dlp.conf`
    * 如果未给定 `-P`，则搜索当前目录
1. **用户配置**：
    * `${XDG_CONFIG_HOME}/yt-dlp.conf`
    * `${XDG_CONFIG_HOME}/yt-dlp/config`（推荐用于 Linux/macOS）
    * `${XDG_CONFIG_HOME}/yt-dlp/config.txt`
    * `${APPDATA}/yt-dlp.conf`
    * `${APPDATA}/yt-dlp/config`（推荐用于 Windows）
    * `${APPDATA}/yt-dlp/config.txt`
    * `~/yt-dlp.conf`
    * `~/yt-dlp.conf.txt`
    * `~/.yt-dlp/config`
    * `~/.yt-dlp/config.txt`

    另请参阅：[关于环境变量的说明](#notes-about-environment-variables)
1. **系统配置**：
    * `/etc/yt-dlp.conf`
    * `/etc/yt-dlp/config`
    * `/etc/yt-dlp/config.txt`

例如，使用以下配置文件，yt-dlp 将始终提取音频、复制 mtime、使用代理并将所有视频保存在您主目录的 `YouTube` 目录下：
```
# 以 # 开头的行是注释

# 始终提取音频
-x

# 复制 mtime
--mtime

# 使用此代理
--proxy 127.0.0.1:3128

# 将所有视频保存在您主目录的 YouTube 目录下
-o ~/YouTube/%(title)s.%(ext)s
```

**注意**：配置文件中的选项只是常规命令行调用中使用的相同选项（即开关）；因此在 `-` 或 `--` 后**必须没有空格**，例如 `-o` 或 `--proxy`，而不是 `- o` 或 `-- proxy`。必要时还必须引用它们，就像在 UNIX shell 中一样。

如果您想为特定的 yt-dlp 运行禁用所有配置文件，可以使用 `--ignore-config`。如果在任何配置文件中找到 `--ignore-config`，则不会加载进一步的配置。例如，在便携式配置文件中包含该选项会阻止加载主目录、用户和系统配置。此外，（为了向后兼容）如果在系统配置文件中找到 `--ignore-config`，则不会加载用户配置。

### 配置文件编码

配置文件根据 UTF BOM（如果存在）进行解码，否则根据系统区域设置的编码进行解码。

如果您希望以不同方式解码文件，请在文件开头添加 `# coding: ENCODING`（例如 `# coding: shift-jis`）。在此之前不得有任何字符，甚至空格或 BOM。

### 使用 netrc 进行身份验证

您可能还需要为支持身份验证的提取器（通过使用 `--username` 和 `--password` 提供登录名和密码）配置自动凭据存储，以便不在每次 yt-dlp 执行时将凭据作为命令行参数传递，并防止在 shell 命令历史记录中跟踪纯文本密码。您可以基于每个提取器使用 [`.netrc` 文件](https://stackoverflow.com/tags/.netrc/info) 来实现这一点。为此，您需要在 `--netrc-location` 中创建 `.netrc` 文件并将权限限制为仅您可读/写：
```
touch ${HOME}/.netrc
chmod a-rwx,u+rw ${HOME}/.netrc
```
之后，您可以按照以下格式为提取器添加凭据，其中 *extractor* 是提取器的小写名称：
```
machine <extractor> login <username> password <password>
```
例如
```
machine youtube login myaccount@gmail.com password my_youtube_password
machine twitch login my_twitch_account_name password my_twitch_password
```
要激活使用 `.netrc` 文件的身份验证，您应该将 `--netrc` 传递给 yt-dlp 或将其放置在[配置文件](#configuration)中。

.netrc 文件的默认位置是 `~`（见下文）。

作为使用 `.netrc` 文件的替代方案（其缺点是将密码保存在纯文本文件中），您可以配置自定义 shell 命令来为提取器提供凭据。这是通过提供 `--netrc-cmd` 参数来完成的，它应该以 netrc 格式输出凭据并在成功时返回 `0`，其他值将被视为错误。命令中的 `{}` 将被提取器的名称替换，以便可以选择正确提取器的凭据。

例如，要使用存储为 `.authinfo.gpg` 的加密 `.netrc` 文件
```
yt-dlp --netrc-cmd 'gpg --decrypt ~/.authinfo.gpg' 'https://www.youtube.com/watch?v=BaW_jenozKc'
```


### 关于环境变量的说明
* 环境变量通常在 UNIX 上指定为 `${VARIABLE}`/`$VARIABLE`，在 Windows 上指定为 `%VARIABLE%`；但在本文档中始终显示为 `${VARIABLE}`
* yt-dlp 还允许在 Windows 上对类似路径的选项使用 UNIX 风格的变量；例如 `--output`、`--config-locations`
* 如果未设置，`${XDG_CONFIG_HOME}` 默认为 `~/.config`，`${XDG_CACHE_HOME}` 默认为 `~/.cache`
* 在 Windows 上，`~` 指向 `${HOME}`（如果存在）；否则指向 `${USERPROFILE}` 或 `${HOMEDRIVE}${HOMEPATH}`
* 在 Windows 上，`${USERPROFILE}` 通常指向 `C:\Users\<user name>`，`${APPDATA}` 指向 `${USERPROFILE}\AppData\Roaming`

# 输出模板

`-o` 选项用于指示输出文件名的模板，而 `-P` 选项用于指定每种类型的文件应保存到的路径。

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
**简而言之：**[带我到示例](#output-template-examples)。
<!-- MANPAGE: END EXCLUDED SECTION -->

`-o` 的最简单用法是在下载单个文件时不设置任何模板参数，例如 `yt-dlp -o funny_video.flv "https://some/video"`（像这样硬编码文件扩展名_不_推荐，并且可能会破坏某些后处理）。

但是，它也可能包含在下载每个视频时将被替换的特殊序列。特殊序列可以根据 [Python 字符串格式化操作](https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting)进行格式化，例如 `%(NAME)s` 或 `%(NAME)05d`。为了澄清，这是一个百分号后跟括号中的名称，后跟格式化操作。

字段名称本身（括号内的部分）也可以有一些特殊的格式化：

1. **对象遍历**：元数据中可用的字典和列表可以使用点 `.` 分隔符进行遍历；例如 `%(tags.0)s`、`%(subtitles.en.-1.ext)s`。您可以使用冒号 `:` 进行 Python 切片；例如 `%(id.3:7)s`、`%(id.6:2:-1)s`、`%(formats.:.format_id)s`。可以使用大括号 `{}` 来构建仅包含特定键的字典；例如 `%(formats.:.{format_id,height})#j`。空字段名称 `%()s` 指的是整个信息字典；例如 `%(.{id,title})s`。请注意，使用此方法变得可用的所有字段并未在下面列出。使用 `-j` 查看此类字段

1. **算术运算**：可以使用 `+`、`-` 和 `*` 对数字字段进行简单的算术运算。例如 `%(playlist_index+10)03d`、`%(n_entries+1-playlist_index)d`

1. **日期/时间格式化**：日期/时间字段可以根据 [strftime 格式化](https://docs.python.org/3/library/datetime.html#strftime-and-strptime-format-codes)进行格式化，方法是使用 `>` 将其与字段名称分隔。例如 `%(duration>%H-%M-%S)s`、`%(upload_date>%Y-%m-%d)s`、`%(epoch-3600>%H-%M-%S)s`

1. **替代项**：可以用 `,` 分隔指定替代字段。例如 `%(release_date>%Y,upload_date>%Y|Unknown)s`

1. **替换**：可以根据 [`str.format` 迷你语言](https://docs.python.org/3/library/string.html#format-specification-mini-language) 使用 `&` 分隔符指定替换值。如果字段*不*为空，则将使用此替换值而不是实际字段内容。这是在考虑替代字段之后完成的；因此，如果*任何*替代字段*不*为空，则使用替换。例如 `%(chapters&has chapters|no chapters)s`、`%(title&TITLE={:>20}|NO TITLE)s`

1. **默认值**：可以使用 `|` 分隔符为字段为空时指定字面默认值。这将覆盖 `--output-na-placeholder`。例如 `%(uploader|Unknown)s`

1. **更多转换**：除了正常的格式类型 `diouxXeEfFgGcrs` 之外，yt-dlp 还支持转换为 `B` = **B**ytes（字节）、`j` = **j**son（标志 `#` 用于漂亮打印，`+` 用于 Unicode）、`h` = HTML 转义、`l` = 逗号分隔的**l**ist（列表）（标志 `#` 用于 `\n` 换行分隔）、`q` = 为终端引用的字符串 **q**uoted（标志 `#` 将列表拆分为不同的参数）、`D` = 添加**D**ecimal（十进制）后缀（例如 10M）（标志 `#` 使用 1024 作为因子）、`S` = **S**anitize（清理）为文件名（标志 `#` 用于受限）

1. **Unicode 规范化**：格式类型 `U` 可用于 NFC [Unicode 规范化](https://docs.python.org/3/library/unicodedata.html#unicodedata.normalize)。备用形式标志（`#`）将规范化更改为 NFD，转换标志 `+` 可用于 NFKC/NFKD 兼容性等效规范化。例如 `%(title)+.100U` 是 NFKC

综上所述，字段的一般语法是：
```
%(name[.keys][addition][>strf][,alternate][&replacement][|default])[flags][width][.precision][length]type
```

此外，您可以通过指定文件类型后跟用冒号 `:` 分隔的模板，为各种元数据文件设置与一般输出模板不同的输出模板。支持的文件类型有 `subtitle`、`thumbnail`、`description`、`annotation`（已弃用）、`infojson`、`link`、`pl_thumbnail`、`pl_description`、`pl_infojson`、`chapter`、`pl_video`。例如 `-o "%(title)s.%(ext)s" -o "thumbnail:%(title)s\%(title)s.%(ext)s"` 将把缩略图放在与视频同名的文件夹中。如果任何模板为空，则不会写入该类型的文件。例如 `--write-thumbnail -o "thumbnail:"` 将仅为播放列表写入缩略图，而不为视频写入。

<a id="outtmpl-postprocess-note"></a>

**注意**：由于后处理（即合并等），实际输出文件名可能会有所不同。使用 `--print after_move:filepath` 获取所有后处理完成后的名称。

可用字段包括：

 - `id` (string)：视频标识符
 - `title` (string)：视频标题
 - `fulltitle` (string)：忽略直播时间戳和通用标题的视频标题
 - `ext` (string)：视频文件名扩展名
 - `alt_title` (string)：视频的次要标题
 - `description` (string)：视频的描述
 - `display_id` (string)：视频的替代标识符
 - `uploader` (string)：视频上传者的全名
 - `uploader_id` (string)：视频上传者的昵称或 ID
 - `uploader_url` (string)：视频上传者个人资料的 URL
 - `license` (string)：视频许可的许可证名称
 - `creators` (list)：视频的创作者
 - `creator` (string)：视频的创作者；逗号分隔
 - `timestamp` (numeric)：视频变得可用的时刻的 UNIX 时间戳
 - `upload_date` (string)：视频上传日期（UTC，YYYYMMDD）
 - `release_timestamp` (numeric)：视频发布时刻的 UNIX 时间戳
 - `release_date` (string)：视频在 UTC 发布的日期（YYYYMMDD）
 - `release_year` (numeric)：视频或专辑发布的年份（YYYY）
 - `modified_timestamp` (numeric)：视频最后修改时刻的 UNIX 时间戳
 - `modified_date` (string)：视频在 UTC 最后修改的日期（YYYYMMDD）
 - `channel` (string)：视频上传到的频道的全名
 - `channel_id` (string)：频道的 ID
 - `channel_url` (string)：频道的 URL
 - `channel_follower_count` (numeric)：频道的关注者数量
 - `channel_is_verified` (boolean)：频道是否在平台上已验证
 - `location` (string)：拍摄视频的物理位置
 - `duration` (numeric)：视频的长度（秒）
 - `duration_string` (string)：视频的长度（HH:mm:ss）
 - `view_count` (numeric)：有多少用户在平台上观看了该视频
 - `concurrent_view_count` (numeric)：当前有多少用户在平台上观看该视频
 - `like_count` (numeric)：视频的正面评价数量
 - `dislike_count` (numeric)：视频的负面评价数量
 - `repost_count` (numeric)：视频的转发数量
 - `average_rating` (numeric)：用户给出的平均评价，使用的比例取决于网页
 - `comment_count` (numeric)：视频上的评论数量（对于某些提取器，评论仅在最后下载，因此无法使用此字段）
 - `save_count` (numeric)：视频被保存或书签的次数
 - `age_limit` (numeric)：视频的年龄限制（年）
 - `live_status` (string)：以下之一："not_live"、"is_live"、"is_upcoming"、"was_live"、"post_live"（曾是直播，但 VOD 尚未处理）
 - `is_live` (boolean)：此视频是直播流还是固定长度的视频
 - `was_live` (boolean)：此视频最初是否是直播流
 - `playable_in_embed` (string)：此视频是否允许在其他网站的嵌入式播放器中播放
 - `availability` (string)：视频是"private"、"premium_only"、"subscriber_only"、"needs_auth"、"unlisted"还是"public"
 - `media_type` (string)：网站分类的媒体类型，例如 "episode"、"clip"、"trailer"
 - `start_time` (numeric)：播放应开始的秒数，如 URL 中指定的
 - `end_time` (numeric)：播放应结束的秒数，如 URL 中指定的
 - `extractor` (string)：提取器的名称
 - `extractor_key` (string)：提取器的键名
 - `epoch` (numeric)：信息提取完成时的 Unix 纪元
 - `autonumber` (numeric)：每次下载都会增加的数字，从 `--autonumber-start` 开始，用前导零填充到 5 位数字
 - `video_autonumber` (numeric)：每个视频都会增加的数字
 - `n_entries` (numeric)：播放列表中提取的项目总数
 - `playlist_id` (string)：包含视频的播放列表的标识符
 - `playlist_title` (string)：包含视频的播放列表的名称
 - `playlist` (string)：如果可用则为 `playlist_title`，否则为 `playlist_id`
 - `playlist_count` (numeric)：播放列表中的项目总数。如果未提取整个播放列表，则可能未知
 - `playlist_index` (numeric)：视频在播放列表中的索引，根据最终索引用前导零填充
 - `playlist_autonumber` (numeric)：视频在播放列表下载队列中的位置，根据播放列表的总长度用前导零填充
 - `playlist_uploader` (string)：播放列表上传者的全名
 - `playlist_uploader_id` (string)：播放列表上传者的昵称或 ID
 - `playlist_channel` (string)：上传播放列表的频道的显示名称
 - `playlist_channel_id` (string)：上传播放列表的频道的标识符
 - `playlist_webpage_url` (string)：播放列表网页的 URL
 - `webpage_url` (string)：视频网页的 URL，如果提供给 yt-dlp，应该产生相同的结果
 - `webpage_url_basename` (string)：网页 URL 的基本名称
 - `webpage_url_domain` (string)：网页 URL 的域
 - `original_url` (string)：用户提供的 URL（或播放列表条目的 `webpage_url`）
 - `categories` (list)：视频所属的类别列表
 - `tags` (list)：分配给视频的标签列表
 - `cast` (list)：演员列表

[过滤格式](#filtering-formats)中的所有字段也可以使用

适用于属于某个逻辑章节或部分的视频：

 - `chapter` (string)：视频所属章节的名称或标题
 - `chapter_number` (numeric)：视频所属章节的编号
 - `chapter_id` (string)：视频所属章节的 ID

适用于某个系列或节目剧集的视频：

 - `series` (string)：视频剧集所属系列或节目的标题
 - `series_id` (string)：视频剧集所属系列或节目的 ID
 - `season` (string)：视频剧集所属季的标题
 - `season_number` (numeric)：视频剧集所属季的编号
 - `season_id` (string)：视频剧集所属季的 ID
 - `episode` (string)：视频剧集的标题
 - `episode_number` (numeric)：季内视频剧集的编号
 - `episode_id` (string)：视频剧集的 ID

适用于音乐专辑中的曲目或部分媒体：

 - `track` (string)：曲目标题
 - `track_number` (numeric)：专辑或光盘内曲目的编号
 - `track_id` (string)：曲目的 ID
 - `artists` (list)：曲目的艺术家
 - `artist` (string)：曲目的艺术家；逗号分隔
 - `genres` (list)：曲目的流派
 - `genre` (string)：曲目的流派；逗号分隔
 - `composers` (list)：作品的作曲者
 - `composer` (string)：作品的作曲者；逗号分隔
 - `album` (string)：曲目所属专辑的标题
 - `album_type` (string)：专辑的类型
 - `album_artists` (list)：专辑上出现的所有艺术家
 - `album_artist` (string)：专辑上出现的所有艺术家；逗号分隔
 - `disc_number` (numeric)：曲目所属光盘或其他物理介质的编号

仅在使用 `--download-sections` 以及对具有内部章节的视频使用 `--split-chapters` 时的 `chapter:` 前缀时可用：

 - `section_title` (string)：章节的标题
 - `section_number` (numeric)：文件内章节的编号
 - `section_start` (numeric)：章节的开始时间（秒）
 - `section_end` (numeric)：章节的结束时间（秒）

仅在 `--print` 中使用时可用：

 - `urls` (string)：所有请求格式的 URL，每行一个
 - `filename` (string)：视频文件的名称。请注意，[实际文件名可能会有所不同](#outtmpl-postprocess-note)
 - `formats_table` (table)：`--list-formats` 打印的视频格式表
 - `thumbnails_table` (table)：`--list-thumbnails` 打印的缩略图格式表
 - `subtitles_table` (table)：`--list-subs` 打印的字幕格式表
 - `automatic_captions_table` (table)：`--list-subs` 打印的自动字幕格式表

 仅在视频下载后可用 (`post_process`/`after_move`)：

 - `filepath`：下载的视频文件的实际路径

仅在 `--sponsorblock-chapter-title` 中可用：

 - `start_time` (numeric)：章节的开始时间（秒）
 - `end_time` (numeric)：章节的结束时间（秒）
 - `categories` (list)：章节所属的 [SponsorBlock 类别](https://wiki.sponsor.ajay.app/w/Types#Category)
 - `category` (string)：章节所属的最小 SponsorBlock 类别
 - `category_names` (list)：类别的友好名称
 - `name` (string)：最小类别的友好名称
 - `type` (string)：章节的 [SponsorBlock 操作类型](https://wiki.sponsor.ajay.app/w/Types#Action_Type)

上述每个序列在输出模板中引用时，将被与序列名称对应的实际值替换。例如，对于 `-o %(title)s-%(id)s.%(ext)s` 和标题为 `yt-dlp test video` 且 ID 为 `BaW_jenozKc` 的 mp4 视频，这将导致在当前目录中创建一个 `yt-dlp test video-BaW_jenozKc.mp4` 文件。

**注意**：某些序列不能保证存在，因为它们取决于特定提取器获得的元数据。此类序列将用 `--output-na-placeholder` 提供的占位符值替换（默认为 `NA`）。

**提示**：查看 `-j` 输出以确定特定 URL 可用的字段

对于数字序列，您可以使用[数字相关格式化](https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting)；例如 `%(view_count)05d` 将导致一个字符串，其中观看计数用零填充到最多 5 个字符，如 `00042`。

输出模板还可以包含任意分层路径，例如 `-o "%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s"`，这将导致在与此路径模板对应的目录中下载每个视频。任何缺失的目录将自动为您创建。

要在输出模板中使用百分比字面量，请使用 `%%`。要输出到 stdout，请使用 `-o -`。

当前的默认模板是 `%(title)s [%(id)s].%(ext)s`。

在某些情况下，您不希望特殊字符（如中文、空格或 &），例如当将下载的文件名传输到 Windows 系统或通过 8 位不安全通道传输文件名时。在这些情况下，添加 `--restrict-filenames` 标志以获得较短的标题。

#### 输出模板示例

```bash
$ yt-dlp --print filename -o "test video.%(ext)s" BaW_jenozKc
test video.webm    # 具有正确扩展名的字面名称

$ yt-dlp --print filename -o "%(title)s.%(ext)s" BaW_jenozKc
youtube-dl test video ''_ä↭𝕐.webm    # 各种奇怪的字符

$ yt-dlp --print filename -o "%(title)s.%(ext)s" BaW_jenozKc --restrict-filenames
youtube-dl_test_video_.webm    # 受限的文件名

# 将 YouTube 播放列表视频下载到按播放列表中视频顺序索引的单独目录中
$ yt-dlp -o "%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s" "https://www.youtube.com/playlist?list=PLwiyx1dc3P2JR9N8gQaQN_BCvlSlap7re"

# 将 YouTube 播放列表视频下载到根据其上传年份的单独目录中
$ yt-dlp -o "%(upload_date>%Y)s/%(title)s.%(ext)s" "https://www.youtube.com/playlist?list=PLwiyx1dc3P2JR9N8gQaQN_BCvlSlap7re"

# 使用 " - " 分隔符为播放列表索引添加前缀，但仅当可用时
$ yt-dlp -o "%(playlist_index&{} - |)s%(title)s.%(ext)s" BaW_jenozKc "https://www.youtube.com/user/TheLinuxFoundation/playlists"

# 下载 YouTube 频道/用户的所有播放列表，将每个播放列表保存在单独目录中：
$ yt-dlp -o "%(uploader)s/%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s" "https://www.youtube.com/user/TheLinuxFoundation/playlists"

# 下载 Udemy 课程，将每个章节保存在您主目录的 MyVideos 目录下的单独目录中
$ yt-dlp -u user -p password -P "~/MyVideos" -o "%(playlist)s/%(chapter_number)s - %(chapter)s/%(title)s.%(ext)s" "https://www.udemy.com/java-tutorial"

# 下载整个系列季，将每个系列和每个季保存在 C:/MyVideos 下的单独目录中
$ yt-dlp -P "C:/MyVideos" -o "%(series)s/%(season_number)s - %(season)s/%(episode_number)s - %(episode)s.%(ext)s" "https://videomore.ru/kino_v_detalayah/5_sezon/367617"

# 将视频下载为 "C:\MyVideos\uploader\title.ext"，字幕下载为 "C:\MyVideos\subs\uploader\title.ext"
# 并将所有临时文件放在 "C:\MyVideos\tmp" 中
$ yt-dlp -P "C:/MyVideos" -P "temp:tmp" -P "subtitle:subs" -o "%(uploader)s/%(title)s.%(ext)s" BaW_jenozKc --write-subs

# 将视频下载为 "C:\MyVideos\uploader\title.ext"，字幕下载为 "C:\MyVideos\uploader\subs\title.ext"
$ yt-dlp -P "C:/MyVideos" -o "%(uploader)s/%(title)s.%(ext)s" -o "subtitle:%(uploader)s/subs/%(title)s.%(ext)s" BaW_jenozKc --write-subs

# 将正在下载的视频流式传输到 stdout
$ yt-dlp -o - BaW_jenozKc
```

# 格式选择

默认情况下，如果您**不**传递任何选项，yt-dlp 会尝试下载最佳可用质量。
这通常相当于使用 `-f bestvideo*+bestaudio/best`。但是，如果启用了多个音频流（`--audio-multistreams`），默认格式会更改为 `-f bestvideo+bestaudio/best`。同样，如果 ffmpeg 不可用，或者您使用 yt-dlp 流式传输到 `stdout`（`-o -`），默认将变为 `-f best/bestvideo+bestaudio`。

**弃用警告**：最新版本的 yt-dlp 可以使用 ffmpeg 同时将多种格式流式传输到 stdout。因此，在未来的版本中，此功能的默认设置将设置为 `-f bv*+ba/b`，类似于正常下载。如果您想保留 `-f b/bv+ba` 设置，建议在配置选项中明确指定它。

格式选择的一般语法是 `-f FORMAT`（或 `--format FORMAT`），其中 `FORMAT` 是一个*选择器表达式*，即描述您想要下载的格式或格式的表达式。

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
**简而言之：**[带我到示例](#format-selection-examples)。
<!-- MANPAGE: END EXCLUDED SECTION -->

最简单的情况是请求特定格式；例如，使用 `-f 22`，您可以下载格式代码等于 22 的格式。您可以使用 `--list-formats` 或 `-F` 获取特定视频的可用格式代码列表。请注意，这些格式代码是特定于提取器的。

您还可以使用文件扩展名（目前支持 `3gp`、`aac`、`flv`、`m4a`、`mp3`、`mp4`、`ogg`、`wav`、`webm`）下载作为单个文件提供的特定文件扩展名的最佳质量格式，例如 `-f webm` 将下载作为单个文件提供的具有 `webm` 扩展名的最佳质量格式。

您可以使用 `-f -` 为*每个视频*交互式提供格式选择器

您还可以使用特殊名称来选择特定的边缘情况格式：

 - `all`：分别选择**所有格式**
 - `mergeall`：选择并**合并所有格式**（必须与 `--audio-multistreams`、`--video-multistreams` 或两者一起使用）
 - `b*`、`best*`：选择**包含视频或音频或两者**的最佳质量格式（即 `vcodec!=none or acodec!=none`）
 - `b`、`best`：选择**包含视频和音频两者**的最佳质量格式。相当于 `best*[vcodec!=none][acodec!=none]`
 - `bv`、`bestvideo`：选择最佳质量**仅视频**格式。相当于 `best*[acodec=none]`
 - `bv*`、`bestvideo*`：选择**包含视频**的最佳质量格式。它也可能包含音频。相当于 `best*[vcodec!=none]`
 - `ba`、`bestaudio`：选择最佳质量**仅音频**格式。相当于 `best*[vcodec=none]`
 - `ba*`、`bestaudio*`：选择**包含音频**的最佳质量格式。它也可能包含视频。相当于 `best*[acodec!=none]`（[不要使用！](https://github.com/yt-dlp/yt-dlp/issues/979#issuecomment-919629354)）
 - `w*`、`worst*`：选择包含视频或音频的最差质量格式
 - `w`、`worst`：选择包含视频和音频两者的最差质量格式。相当于 `worst*[vcodec!=none][acodec!=none]`
 - `wv`、`worstvideo`：选择最差质量的仅视频格式。相当于 `worst*[acodec=none]`
 - `wv*`、`worstvideo*`：选择包含视频的最差质量格式。它也可能包含音频。相当于 `worst*[vcodec!=none]`
 - `wa`、`worstaudio`：选择最差质量的仅音频格式。相当于 `worst*[vcodec=none]`
 - `wa*`、`worstaudio*`：选择包含音频的最差质量格式。它也可能包含视频。相当于 `worst*[acodec!=none]`

例如，要下载最差质量的仅视频格式，您可以使用 `-f worstvideo`。但是，建议不要使用 `worst` 和相关选项。当您的格式选择器是 `worst` 时，会选择在所有方面都最差的格式。大多数情况下，您实际想要的是文件大小最小的视频。因此，通常最好使用 `-S +size` 或更严格地，使用 `-S +size,+br,+res,+fps` 而不是 `-f worst`。有关更多详细信息，请参阅[排序格式](#sorting-formats)。

您可以使用 `best<type>.<n>` 选择某种类型的第 n 个最佳格式。例如，`best.2` 将选择第二个最佳组合格式。同样，`bv*.3` 将选择第三个包含视频流的最佳格式。

如果您想下载多个视频，而它们没有相同的可用格式，您可以使用斜杠指定偏好顺序。请注意，左侧的格式是首选的；例如 `-f 22/17/18` 将下载格式 22（如果可用），否则将下载格式 17（如果可用），否则将下载格式 18（如果可用），否则将抱怨没有适合下载的格式。

如果您想下载同一视频的多种格式，请使用逗号作为分隔符，例如 `-f 22,17,18` 将下载所有这三种格式（当然，如果它们可用）。或者一个更复杂的示例，结合优先级功能：`-f 136/137/mp4/bestvideo,140/m4a/bestaudio`。

您可以使用 `-f <format1>+<format2>+...` 将多种格式的视频和音频合并到单个文件中（需要安装 ffmpeg）；例如 `-f bestvideo+bestaudio` 将下载最佳仅视频格式、最佳仅音频格式，并使用 ffmpeg 将它们合并在一起。

**弃用警告**：由于*下面*描述的行为复杂且反直觉，这将被删除，并且多流将在未来默认启用。将添加一个新运算符来将格式限制为单个音频/视频

除非使用 `--video-multistreams`，否则除第一个之外的所有包含视频流的格式都将被忽略。同样，除非使用 `--audio-multistreams`，否则除第一个之外的所有包含音频流的格式都将被忽略。例如 `-f bestvideo+best+bestaudio --video-multistreams --audio-multistreams` 将下载并合并所有 3 个给定的格式。生成的文件将有 2 个视频流和 2 个音频流。但是 `-f bestvideo+best+bestaudio --no-video-multistreams` 将仅下载并合并 `bestvideo` 和 `bestaudio`。`best` 被忽略，因为已经选择了另一个包含视频流的格式（`bestvideo`）。因此，格式的顺序很重要。`-f best+bestaudio --no-audio-multistreams` 将仅下载 `best`，而 `-f bestaudio+best --no-audio-multistreams` 将忽略 `best` 并仅下载 `bestaudio`。

## 过滤格式

您还可以通过在括号中放置条件来过滤视频格式，例如 `-f "best[height=720]"`（或 `-f "[filesize>10M]"`，因为没有选择器的过滤器被解释为 `best`）。

以下数字元字段可以与比较运算符 `<`、`<=`、`>`、`>=`、`=`（等于）、`!=`（不等于）一起使用：

 - `filesize`：字节数，如果提前知道
 - `filesize_approx`：字节数的估计值
 - `width`：视频的宽度，如果已知
 - `height`：视频的高度，如果已知
 - `aspect_ratio`：视频的宽高比，如果已知
 - `tbr`：音频和视频的平均比特率，单位为 [kbps](## "1000 bits/sec")
 - `abr`：平均音频比特率，单位为 [kbps](## "1000 bits/sec")
 - `vbr`：平均视频比特率，单位为 [kbps](## "1000 bits/sec")
 - `asr`：音频采样率，单位为赫兹
 - `fps`：帧率
 - `audio_channels`：音频通道数
 - `stretched_ratio`：视频像素的 `width:height`，如果不是正方形

过滤也适用于比较运算符 `=`（等于）、`^=`（以...开头）、`$=`（以...结尾）、`*=`（包含）、`~=`（匹配正则表达式）和以下字符串元字段：

 - `url`：视频 URL
 - `ext`：文件扩展名
 - `acodec`：正在使用的音频编解码器名称
 - `vcodec`：正在使用的视频编解码器名称
 - `container`：容器格式的名称
 - `protocol`：将用于实际下载的协议，小写（`http`、`https`、`rtsp`、`rtmp`、`rtmpe`、`mms`、`f4m`、`ism`、`http_dash_segments`、`m3u8` 或 `m3u8_native`）
 - `language`：语言代码
 - `dynamic_range`：视频的动态范围
 - `format_id`：格式的简短描述
 - `format`：格式的人类可读描述
 - `format_note`：有关格式的其他信息
 - `resolution`：宽度和高度的文本描述

任何字符串比较都可以加上否定前缀 `!` 以产生相反的比较，例如 `!*=`（不包含）。字符串比较的比较操作数如果包含空格或除 `._-` 之外的特殊字符，则需要用双引号或单引号括起来。

**注意**：不能保证上述任何元字段都存在，因为这完全取决于特定提取器获得的元数据，即网站提供的元数据。提取器提供的任何其他字段也可以用于过滤。

除非在运算符后放置问号（`?`），否则将排除值未知的格式。您可以组合格式过滤器，因此 `-f "bv[height<=?720][tbr>500]"` 选择比特率至少为 500 kbps 的 720p 或更低视频（或高度未知的视频）。您还可以将过滤器与 `all` 一起使用以下载满足过滤器的所有格式，例如 `-f "all[vcodec=none]"` 选择所有仅音频格式。

格式选择器也可以使用括号分组；例如 `-f "(mp4,webm)[height<480]"` 将下载高度低于 480 的最佳预合并 mp4 和 webm 格式。

## 排序格式

您可以使用 `-S`（`--format-sort`）更改被视为 `best` 的标准。其一般格式是 `--format-sort field1,field2...`。

可用字段包括：

 - `hasvid`：优先考虑具有视频流的格式
 - `hasaud`：优先考虑具有音频流的格式
 - `ie_pref`：格式偏好
 - `lang`：由提取器确定的语言偏好（例如，原始语言优先于音频描述）
 - `quality`：格式的质量
 - `source`：源的偏好
 - `proto`：用于下载的协议（`https`/`ftps` > `http`/`ftp` > `m3u8_native`/`m3u8` > `http_dash_segments`> `websocket_frag` > `mms`/`rtsp` > `f4f`/`f4m`）
 - `vcodec`：视频编解码器（`av01` > `vp9.2` > `vp9` > `h265` > `h264` > `vp8` > `h263` > `theora` > 其他）
 - `acodec`：音频编解码器（`flac`/`alac` > `wav`/`aiff` > `opus` > `vorbis` > `aac` > `mp4a` > `mp3` > `ac4` > `eac3` > `ac3` > `dts` > 其他）
 - `codec`：相当于 `vcodec,acodec`
 - `vext`：视频扩展名（`mp4` > `mov` > `webm` > `flv` > 其他）。如果使用 `--prefer-free-formats`，则优先选择 `webm`。
 - `aext`：音频扩展名（`m4a` > `aac` > `mp3` > `ogg` > `opus` > `webm` > 其他）。如果使用 `--prefer-free-formats`，顺序更改为 `ogg` > `opus` > `webm` > `mp3` > `m4a` > `aac`
 - `ext`：相当于 `vext,aext`
 - `filesize`：确切的文件大小，如果提前知道
 - `fs_approx`：近似的文件大小
 - `size`：确切的文件大小（如果可用），否则为近似的文件大小
 - `height`：视频的高度
 - `width`：视频的宽度
 - `res`：视频分辨率，计算为最小维度
 - `fps`：视频的帧率
 - `hdr`：视频的动态范围（`DV` > `HDR12` > `HDR10+` > `HDR10` > `HLG` > `SDR`）
 - `channels`：音频通道数
 - `tbr`：总平均比特率，单位为 [kbps](## "1000 bits/sec")
 - `vbr`：平均视频比特率，单位为 [kbps](## "1000 bits/sec")
 - `abr`：平均音频比特率，单位为 [kbps](## "1000 bits/sec")
 - `br`：平均比特率，单位为 [kbps](## "1000 bits/sec")，`tbr`/`vbr`/`abr`
 - `asr`：音频采样率，单位为 Hz

**弃用警告**：这些字段中有许多具有（当前未记录的）别名，可能会在未来的版本中删除。建议仅使用记录的字段名称。

除非另有说明，否则所有字段都按降序排序。要反转此顺序，请在字段前加上 `+`。例如 `+res` 优先选择分辨率最小的格式。此外，您可以为字段添加首选值后缀，用 `:` 分隔。例如 `res:720` 优先选择较大的视频，但不大于 720p，如果没有小于 720p 的视频，则选择最小的视频。对于 `codec` 和 `ext`，您可以提供两个首选值，第一个用于视频，第二个用于音频。例如 `+codec:avc:m4a`（相当于 `+vcodec:avc,+acodec:m4a`）将视频编解码器偏好设置为 `h264` > `h265` > `vp9` > `vp9.2` > `av01` > `vp8` > `h263` > `theora`，将音频编解码器偏好设置为 `mp4a` > `aac` > `vorbis` > `opus` > `mp3` > `ac3` > `dts`。您还可以使用 `~` 作为分隔符，使排序优先选择最接近提供的值的值。例如 `filesize~1G` 优先选择文件大小最接近 1 GiB 的格式。

字段 `hasvid` 和 `ie_pref` 在排序中始终具有最高优先级，无论用户定义的顺序如何。可以使用 `--format-sort-force` 更改此行为。除此之外，使用的默认顺序是：`lang,quality,res,fps,hdr:12,vcodec,channels,acodec,size,br,asr,proto,ext,hasaud,source,id`。提取器可以覆盖此默认顺序，但不能覆盖用户提供的顺序。

请注意，hdr 的默认值是 `hdr:12`；即不首选 Dolby Vision。做出此选择是因为 DV 格式尚未与大多数设备完全兼容。这可能会在未来更改。

如果您的格式选择器是 `worst`，则在排序后选择最后一项。这意味着它将选择在所有方面都最差的格式。大多数情况下，您实际想要的是文件大小最小的视频。因此，通常最好使用 `-f best -S +size,+br,+res,+fps`。

如果您多次使用 `-S`/`--format-sort` 选项，每个后续排序参数将添加到前一个参数的前面，并且只保留任何重复字段的最高优先级条目。例如 `-S proto -S res` 相当于 `-S res,proto`，而 `-S res:720,fps -S vcodec,res:1080` 相当于 `-S vcodec,res:1080,fps`。您可以使用 `--format-sort-reset` 忽略任何以前传递的 `-S`/`--format-sort` 参数并重置为默认顺序。

**提示**：您可以使用 `-v -F` 查看格式如何排序（从最差到最佳）。

## 格式选择示例

```bash
# 下载并合并最佳仅视频格式和最佳仅音频格式，
# 或下载最佳组合格式（如果仅视频格式不可用）
$ yt-dlp -f "bv+ba/b"

# 下载包含视频的最佳格式，
# 如果它还没有音频流，则将其与最佳仅音频格式合并
$ yt-dlp -f "bv*+ba/b"

# 与上面相同
$ yt-dlp

# 下载最佳仅视频格式和最佳仅音频格式而不合并它们
# 对于这种情况，应该使用输出模板，因为
# 默认情况下，bestvideo 和 bestaudio 将具有相同的文件名。
$ yt-dlp -f "bv,ba" -o "%(title)s.f%(format_id)s.%(ext)s"

# 下载并合并具有视频流的最佳格式，
# 以及所有仅音频格式到一个文件中
$ yt-dlp -f "bv*+mergeall[vcodec=none]" --audio-multistreams

# 下载并合并具有视频流的最佳格式，
# 以及最佳的 2 个仅音频格式到一个文件中
$ yt-dlp -f "bv*+ba+ba.2" --audio-multistreams


# 以下示例显示了格式选择的旧方法（不使用 -S）
# 以及如何使用 -S 实现类似但（通常）更好的结果

# 下载可用的最差视频（旧方法）
$ yt-dlp -f "wv*+wa/w"

# 下载可用的最佳视频，但具有最小分辨率
$ yt-dlp -S "+res"

# 下载可用的最小视频
$ yt-dlp -S "+size,+br"



# 下载可用的最佳 mp4 视频，如果没有 mp4 可用，则下载最佳视频
$ yt-dlp -f "bv*[ext=mp4]+ba[ext=m4a]/b[ext=mp4] / bv*+ba/b"

# 下载具有最佳扩展名的最佳视频
# （对于视频，mp4 > mov > webm > flv。对于音频，m4a > aac > mp3 ...）
$ yt-dlp -S "ext"



# 下载可用的最佳视频，但不高于 480p，
# 如果没有低于 480p 的视频，则下载最差视频
$ yt-dlp -f "bv*[height<=480]+ba/b[height<=480] / wv*+ba/w"

# 下载可用的最大高度但不高于 480p 的最佳视频，
# 如果没有低于 480p 的视频，则下载最小分辨率的最佳视频
$ yt-dlp -S "height:480"

# 下载可用的最大分辨率但不高于 480p 的最佳视频，
# 如果没有低于 480p 的视频，则下载最小分辨率的最佳视频
# 分辨率通过使用最小维度来确定。
# 因此，这也适用于垂直视频
$ yt-dlp -S "res:480"



# 下载最佳视频（也有音频）但不大于 50 MB，
# 如果没有低于 50 MB 的视频，则下载最差视频（也有音频）
$ yt-dlp -f "b[filesize<50M] / w"

# 下载最大视频（也有音频）但不大于 50 MB，
# 如果没有低于 50 MB 的视频，则下载最小视频（也有音频）
$ yt-dlp -f "b" -S "filesize:50M"

# 下载大小最接近 50 MB 的最佳视频（也有音频）
$ yt-dlp -f "b" -S "filesize~50M"



# 通过 HTTP/HTTPS 协议通过直接链接下载可用的最佳视频，
# 如果没有这样的视频，则通过任何协议下载可用的最佳视频
$ yt-dlp -f "(bv*+ba/b)[protocol^=http][protocol!*=dash] / (bv*+ba/b)"

# 通过最佳协议下载可用的最佳视频
# （https/ftps > http/ftp > m3u8_native > m3u8 > http_dash_segments ...）
$ yt-dlp -S "proto"



# 下载具有 h264 或 h265 编解码器的最佳视频，
# 如果没有这样的视频，则下载最佳视频
$ yt-dlp -f "(bv*[vcodec~='^((he|a)vc|h26[45])']+ba) / (bv*+ba/b)"

# 下载具有最佳编解码器但不优于 h264 的最佳视频，
# 如果没有这样的视频，则下载具有最差编解码器的最佳视频
$ yt-dlp -S "codec:h264"

# 下载具有最差编解码器但不差于 h264 的最佳视频，
# 如果没有这样的视频，则下载具有最佳编解码器的最佳视频
$ yt-dlp -S "+codec:h264"



# 更复杂的示例

# 下载不高于 720p 且优先选择帧率大于 30 的最佳视频，
# 如果没有这样的视频，则下载（仍然优先选择帧率大于 30 的）最差视频
$ yt-dlp -f "((bv*[fps>30]/bv*)[height<=720]/(wv*[fps>30]/wv*)) + ba / (b[fps>30]/b)[height<=720]/(w[fps>30]/w)"

# 下载分辨率最大但不高于 720p 的视频，
# 如果没有这样的视频，则下载可用分辨率最小的视频，
# 对于相同分辨率的格式优先选择更大的帧率
$ yt-dlp -S "res:720,fps"



# 下载分辨率最小但不差于 480p 的视频，
# 如果没有这样的视频，则下载可用分辨率最大的视频，
# 对于相同分辨率优先选择更好的编解码器，然后选择更大的总比特率
$ yt-dlp -S "+res:480,codec,br"
```

# 修改元数据

可以使用 `--parse-metadata` 和 `--replace-in-metadata` 修改提取器获得的元数据

`--replace-in-metadata FIELDS REGEX REPLACE` 用于使用 [Python 正则表达式](https://docs.python.org/3/library/re.html#regular-expression-syntax)替换任何元数据字段中的文本。[反向引用](https://docs.python.org/3/library/re.html?highlight=backreferences#re.sub)可以在替换字符串中使用以进行高级操作。

`--parse-metadata FROM:TO` 的一般语法是给出要从中提取数据的字段名称或[输出模板](#output-template)，以及将其解释为的格式，用冒号 `:` 分隔。`TO` 可以使用带有命名捕获组的 [Python 正则表达式](https://docs.python.org/3/library/re.html#regular-expression-syntax)、单个字段名称或与[输出模板](#output-template)类似的语法（仅支持 `%(field)s` 格式化）。该选项可以多次使用以解析和修改各种字段。

请注意，这些选项保持其相对顺序，允许在解析的字段中进行替换，反之亦然。此外，任何以此方式创建的字段都可以在[输出模板](#output-template)中使用，并且还会影响使用 `--embed-metadata` 时添加的媒体文件的元数据。

此选项还有一些特殊用途：

* 您可以根据当前下载的视频的元数据下载额外的 URL。为此，将字段 `additional_urls` 设置为您想要下载的 URL。例如 `--parse-metadata "description:(?P<additional_urls>https?://www\.vimeo\.com/\d+)"` 将下载描述中找到的第一个 vimeo 视频

* 您可以使用此选项更改嵌入在媒体文件中的元数据。为此，使用 `meta_` 前缀设置相应字段的值。例如，您为 `meta_description` 字段设置的任何值都将添加到文件中的 `description` 字段 - 您可以使用此选项设置不同的 "description" 和 "synopsis"。要修改单个流的元数据，请使用 `meta<n>_` 前缀（例如 `meta1_language`）。为 `meta_` 字段设置的任何值都将覆盖所有默认值。

**注意**：元数据修改发生在格式选择、提取后和其他后处理操作之前。在这些步骤中可能会添加或更改某些字段，从而覆盖您的更改。

作为参考，以下是 yt-dlp 默认添加到文件元数据的字段：

| 元数据字段                | 来源                                                                    |
| :------------------------ | :---------------------------------------------------------------------- |
| `title`                   | `track` 或 `title`                                                      |
| `date`                    | `upload_date`                                                           |
| `description`、`synopsis` | `description`                                                           |
| `purl`、`comment`         | `webpage_url`                                                           |
| `track`                   | `track_number`                                                          |
| `artist`                  | `artist`、`artists`、`creator`、`creators`、`uploader` 或 `uploader_id` |
| `composer`                | `composer` 或 `composers`                                               |
| `genre`                   | `genre`、`genres`、`categories` 或 `tags`                               |
| `album`                   | `album` 或 `series`                                                     |
| `album_artist`            | `album_artist` 或 `album_artists`                                       |
| `disc`                    | `disc_number`                                                           |
| `show`                    | `series`                                                                |
| `season_number`           | `season_number`                                                         |
| `episode_id`              | `episode` 或 `episode_id`                                               |
| `episode_sort`            | `episode_number`                                                        |
| 每个流的 `language`       | 格式的 `language`                                                       |

**注意**：文件格式可能不支持其中某些字段


## 修改元数据示例

```bash
# 将标题解释为 "Artist - Title"
$ yt-dlp --parse-metadata "title:%(artist)s - %(title)s"

# 正则表达式示例
$ yt-dlp --parse-metadata "description:Artist - (?P<artist>.+)"

# 将 episode 字段复制到 title 字段（FROM 和 TO 为单个字段）
$ yt-dlp --parse-metadata "episode:title"

# 将标题设置为 "Series name S01E05"
$ yt-dlp --parse-metadata "%(series)s S%(season_number)02dE%(episode_number)02d:%(title)s"

# 优先将上传者作为视频元数据中的 "artist" 字段
$ yt-dlp --parse-metadata "%(uploader|)s:%(meta_artist)s" --embed-metadata

# 使用 description 而不是 webpage_url 在视频元数据中设置 "comment" 字段，
# 正确处理多行
$ yt-dlp --parse-metadata "description:(?s)(?P<meta_comment>.+)" --embed-metadata

# 不在视频元数据中设置任何 "synopsis"
$ yt-dlp --parse-metadata ":(?P<meta_synopsis>)"

# 通过将 infojson 中的 "formats" 字段设置为空字符串来删除它
$ yt-dlp --parse-metadata "video::(?P<formats>)" --write-info-json

# 将 title 和 uploader 中的所有空格和 "_" 替换为 "-"
$ yt-dlp --replace-in-metadata "title,uploader" "[ _]" "-"

```

# 提取器参数

某些提取器接受可以使用 `--extractor-args KEY:ARGS` 传递的附加参数。`ARGS` 是一个由 `;`（分号）分隔的 `ARG=VAL1,VAL2` 字符串。例如 `--extractor-args "youtube:player-client=tv,mweb;formats=incomplete" --extractor-args "twitter:api=syndication"`

注意：在 CLI 中，`ARG` 可以使用 `-` 代替 `_`；例如 `youtube:player-client"` 变为 `youtube:player_client"`

以下提取器使用此功能：

#### youtube
* `lang`：优先选择此语言代码的翻译元数据（`title`、`description` 等）（区分大小写）。默认情况下，优先选择视频主要语言元数据，回退到 `en` 翻译。有关支持的内容语言代码列表，请参阅 [youtube/_base.py](https://github.com/yt-dlp/yt-dlp/blob/415b4c9f955b1a0391204bd24a7132590e7b3bdb/yt_dlp/extractor/youtube/_base.py#L402-L409)
* `skip`：`hls`、`dash` 或 `translated_subs` 中的一个或多个，以分别跳过 m3u8 清单、dash 清单和[自动翻译的字幕](https://github.com/yt-dlp/yt-dlp/issues/4090#issuecomment-1158102032)的提取
* `player_client`：从中提取视频数据的客户端。当前可用的客户端有 `web`、`web_safari`、`web_embedded`、`web_music`、`web_creator`、`mweb`、`ios`、`android`、`android_vr`、`tv`、`tv_downgraded` 和 `tv_simply`。默认情况下，使用 `android_vr,web_safari`。如果没有可用的 JavaScript 运行时/引擎，则仅使用 `android_vr`。如果将登录的 cookie 传递给 yt-dlp，则免费帐户使用 `tv_downgraded,web_safari`，高级帐户使用 `tv_downgraded,web_creator`。当使用登录的 cookie 时，会为 `music.youtube.com` URL 添加 `web_music` 客户端。会为年龄受限视频添加 `web_embedded` 客户端，但有时只能成功绕过年龄限制（例如，如果视频可嵌入），如果 `android_vr` 无法访问视频，可能会将其添加为回退。如果需要帐户年龄验证，则会为年龄受限视频添加 `web_creator` 客户端。某些客户端（如 `web_creator` 和 `web_music`）需要 `po_token` 才能下载其格式。某些客户端（如 `web_creator`）只能在身份验证下工作。并非所有客户端都支持通过 cookie 进行身份验证。您可以使用 `default` 作为默认客户端，或者您可以使用 `all` 获取所有客户端（不推荐）。您可以在客户端前加上 `-` 来排除它，例如 `youtube:player_client=default,-web_safari`
* `player_skip`：跳过通常需要用于稳健提取的一些网络请求。`configs`（跳过客户端配置）、`webpage`（跳过初始网页）、`js`（跳过 js 播放器）、`initial_data`（跳过初始数据/下一集请求）中的一个或多个。虽然这些选项可以帮助减少所需的请求数量或避免某些速率限制，但它们可能会导致问题，例如缺少格式或元数据。有关更多详细信息，请参阅 [#860](https://github.com/yt-dlp/yt-dlp/pull/860) 和 [#12826](https://github.com/yt-dlp/yt-dlp/issues/12826)
* `webpage_skip`：跳过嵌入网页数据的提取。`player_response`、`initial_data` 中的一个或两个。这些选项用于测试目的，不会跳过任何网络请求。默认情况下都不会跳过；但是，如果使用的 `player_js_version` 值不是 `actual`，则隐含 `webpage_skip=player_response`
* `webpage_client`：用于视频网页请求的客户端。`web` 或 `web_safari`（默认）之一
* `player_params`：用于播放器请求的 YouTube 播放器参数。将覆盖 yt-dlp 设置的任何默认参数。
* `player_js_variant`：用于 n/sig 解密的播放器 javascript 变体。已知变体有：`main`、`tcc`、`tce`、`es5`、`es6`、`es6_tcc`、`es6_tce`、`tv`、`tv_es6`、`phone`、`house`。默认是 `main`，其他用于调试目的。您可以使用 `actual` 来遵循网站规定的
* `player_js_version`：用于 n/sig 解密的播放器 javascript 版本，格式为 `signature_timestamp@hash`（例如 `20348@0004de42`）。默认是使用网站规定的，可以使用 `actual` 选择。使用任何其他值将隐含 `webpage_skip=player_response`
* `comment_sort`：`top` 或 `new`（默认）- 选择评论排序模式（在 YouTube 端）
* `max_comments`：限制要收集的评论数量。表示 `max-comments,max-parents,max-replies,max-replies-per-thread,max-depth` 的逗号分隔的整数列表。默认为 `all,all,all,all,all`
    * `max-depth` 值为 `1` 将丢弃所有回复，无论给定的 `max-replies` 或 `max-replies-per-thread` 值如何
    * 例如 `all,all,1000,10,2` 将总共获得最多 1000 个回复，每个线程最多 10 个回复，并且只有 2 个深度级别（即顶级评论及其直接回复）。`1000,all,100` 将总共获得最多 1000 条评论，总共最多 100 个回复
* `formats`：更改要返回的格式类型。`dashy`（将 HTTP 转换为 DASH）、`duplicate`（相同内容但不同的 URL 或协议；包括 `dashy`）、`incomplete`（无法完全下载 - 实时 dash、实时自适应 https 和直播后 m3u8）、`missing_pot`（包括需要 PO Token 但缺少的格式）
* `innertube_host`：用于所有 API 请求的 Innertube API 主机；例如 `studio.youtube.com`、`youtubei.googleapis.com`。请注意，从一个子域导出的 cookie 在其他子域上不起作用
* `innertube_key`：用于所有 API 请求的 Innertube API 密钥。默认情况下，不使用 API 密钥
* `raise_incomplete_data`：`Incomplete Data Received` 引发错误而不是报告警告
* `data_sync_id`：覆盖 Innertube API 请求中使用的帐户数据同步 ID。如果您正在使用具有 `youtube:player_skip=webpage,configs` 或 `youtubetab:skip=webpage` 的帐户，则可能需要此选项
* `visitor_data`：覆盖 Innertube API 请求中使用的访客数据。这应该与 `player_skip=webpage,configs` 一起使用，而不使用 cookie。请注意：如果使用不当，这可能会产生不利影响。如果需要来自浏览器的会话，则应该传递 cookie（其中包含访客 ID）
* `po_token`：要使用的来源证明（PO）令牌。格式为 `CLIENT.CONTEXT+PO_TOKEN` 的 PO 令牌的逗号分隔列表，例如 `youtube:po_token=web.gvs+XXX,web.player=XXX,web_safari.gvs+YYY`。上下文可以是 `gvs`（Google 视频服务器 URL）、`player`（Innertube 播放器请求）或 `subs`（字幕）中的任何一个
* `pot_trace`：启用 PO 令牌获取的调试日志。`true` 或 `false`（默认）之一
* `fetch_pot`：用于从提供程序获取 PO 令牌的策略。`always`（无论客户端是否需要给定上下文的令牌，都始终尝试获取 PO 令牌）、`never`（从不获取 PO 令牌）或 `auto`（默认；仅当客户端需要给定上下文的令牌时才获取 PO 令牌）之一
* `jsc_trace`：启用 JS 挑战获取的调试日志。`true` 或 `false`（默认）之一
* `use_ad_playback_context`：跳过前置广告以消除下载前的强制性等待时间。在将高级帐户 cookie 传递给 yt-dlp 时，请勿使用此选项，因为它将导致高级格式的丢失。仅对 `mweb` 和 `web_music` 播放器客户端有效。`true` 或 `false`（默认）之一

#### youtube-ejs
* `jitless`：在无 JIT 模式下运行支持的 Javascript 引擎。支持的运行时有 `deno`、`node` 和 `bun`。以性能/速度为代价提供更好的安全性。请注意，`node` 和 `bun` 仍然被认为是不安全的。`true` 或 `false`（默认）之一

#### youtubepot-webpo
* `bind_to_visitor_id`：是否使用访客 ID 而不是访客数据来缓存 WebPO 令牌。`true`（默认）或 `false` 之一

#### youtubetab（YouTube 播放列表、频道、订阅源等）
* `skip`：`webpage`（跳过初始网页下载）、`authcheck`（允许在未下载初始网页时下载需要身份验证的播放列表。这可能会导致不良行为，有关更多详细信息，请参阅 [#1122](https://github.com/yt-dlp/yt-dlp/pull/1122)）中的一个或多个
* `approximate_date`：在扁平播放列表中提取近似的 `upload_date` 和 `timestamp`。这可能会导致基于日期的过滤器略有偏差

#### generic
* `fragment_query`：如果未提供值，则将 mpd/m3u8 清单 URL 中的任何查询传递到其片段，否则应用作为 `fragment_query=VALUE` 给定的查询字符串。请注意，如果流具有 HLS AES-128 密钥，则查询参数也将传递到密钥 URI，除非传递了 `key_query` 提取器参数，或者除非通过 `hls_key` 提取器参数提供了外部密钥 URI。不适用于 ffmpeg
* `variant_query`：如果未提供值，则将主 m3u8 URL 查询传递到其变体播放列表 URL，否则应用作为 `variant_query=VALUE` 给定的查询字符串
* `key_query`：如果未提供值，则将主 m3u8 URL 查询传递到其 HLS AES-128 解密密钥 URI，否则应用作为 `key_query=VALUE` 给定的查询字符串。请注意，如果通过 `hls_key` 提取器参数提供了密钥 URI，则这将不起作用。不适用于 ffmpeg
* `hls_key`：HLS AES-128 密钥 URI 或密钥（十六进制），以及可选的 IV（十六进制），格式为 `(URI|KEY)[,IV]`；例如 `generic:hls_key=ABCDEF1234567980,0xFEDCBA0987654321`。传递这些值中的任何一个都将强制使用原生 HLS 下载器并覆盖 m3u8 播放列表中找到的相应值
* `is_live`：绕过实时 HLS 检测并手动设置 `live_status` - 值为 `false` 将设置 `not_live`，任何其他值（或无值）将设置 `is_live`
* `impersonate`：尝试使用初始网页请求模拟的目标；例如 `generic:impersonate=safari,chrome-110`。使用 `generic:impersonate` 模拟任何可用目标，并使用 `generic:impersonate=false` 禁用模拟（默认）

#### vikichannel
* `video_types`：要下载的视频类型 - `episodes`、`movies`、`clips`、`trailers` 中的一个或多个

#### youtubewebarchive
* `check_all`：尝试以更多请求为代价检查更多内容。`thumbnails`、`captures` 中的一个或多个

#### gamejolt
* `comment_sort`：`hot`（默认）、`you`（需要 cookie）、`top`、`new` - 选择评论排序模式（在 GameJolt 端）

#### hotstar
* `res`：要忽略的分辨率 - `sd`、`hd`、`fhd` 中的一个或多个
* `vcodec`：要忽略的视频编解码器 - `h264`、`h265`、`dvh265` 中的一个或多个
* `dr`：要忽略的动态范围 - `sdr`、`hdr10`、`dv` 中的一个或多个

#### instagram
* `app_id`：用于 API 请求的 `X-IG-App-ID` 标头的值。默认是 Web 应用程序 ID，`936619743392459`

#### niconicochannelplus
* `max_comments`：要提取的最大评论数 - 默认为 `120`

#### tiktok
* `api_hostname`：用于移动 API 调用的主机名，例如 `api22-normal-c-alisg.tiktokv.com`
* `app_name`：用于移动 API 调用的默认应用程序名称，例如 `trill`
* `app_version`：用于移动 API 调用的默认应用程序版本 - 应与 `manifest_app_version` 一起设置，例如 `34.1.2`
* `manifest_app_version`：用于移动 API 调用的默认数字应用程序版本，例如 `2023401020`
* `aid`：用于移动 API 调用的默认应用程序 ID，例如 `1180`
* `app_info`：使用一个或多个应用程序信息字符串启用移动 API 提取，格式为 `<iid>/[app_name]/[app_version]/[manifest_app_version]/[aid]`，其中 `iid` 是唯一的应用程序安装 ID。`iid` 是唯一必需的值；可以省略所有其他值及其 `/` 分隔符，例如 `tiktok:app_info=1234567890123456789` 或 `tiktok:app_info=123,456/trill///1180,789//34.0.1/340001`
* `device_id`：使用用于移动 API 调用的真实设备 ID 启用移动 API 提取。默认是随机的 19 位字符串

#### rokfinchannel
* `tab`：要下载的选项卡 - `new`、`top`、`videos`、`podcasts`、`streams`、`stacks` 之一

#### twitter
* `api`：选择 `graphql`（默认）、`legacy` 或 `syndication` 之一作为用于推文提取的 API。如果登录则不起作用

#### stacommu, wrestleuniverse
* `device_id`：网站分配的 UUID 值，用于对付费直播内容执行设备限制。可以在浏览器本地存储中找到

#### twitch
* `client_id`：要与 GraphQL 请求一起发送的客户端 ID 值，例如 `twitch:client_id=kimne78kx3ncx6brgo4mv6wki5h1ko`

#### nhkradirulive（NHK らじる★らじる LIVE）
* `area`：要提取的区域变体。有效区域为：`sapporo`、`sendai`、`tokyo`、`nagoya`、`osaka`、`hiroshima`、`matsuyama`、`fukuoka`。默认为 `tokyo`

#### nflplusreplay
* `type`：要提取的游戏重播类型。有效类型为：`full_game`、`full_game_spanish`、`condensed_game` 和 `all_22`。您可以使用 `all` 提取所有可用的重播类型，这是默认设置

#### jiocinema
* `refresh_token`：可以传递浏览器本地存储中的 `refreshToken` UUID 以在使用 `token` 作为用户名和浏览器本地存储中的 `accessToken` 作为密码登录时延长登录会话的生命周期

#### jiosaavn
* `bitrate`：要请求的音频比特率。`16`、`32`、`64`、`128`、`320` 中的一个或多个。默认为 `128,320`

#### afreecatvlive
* `cdn`：用于流 URL 的 API 调用的一个或多个 CDN ID，例如 `gcp_cdn`、`gs_cdn_pc_app`、`gs_cdn_mobile_web`、`gs_cdn_pc_web`

#### soundcloud
* `formats`：要从 API 请求的格式。请求的值应采用 `{protocol}_{codec}` 的格式，例如 `hls_opus,http_aac`。`*` 字符作为通配符，例如 `*_mp3`，可以单独传递以请求所有格式。已知协议包括 `http`、`hls` 和 `hls-aes`；已知编解码器包括 `aac`、`opus` 和 `mp3`。始终提取原始 `download` 格式。默认为 `http_aac,hls_aac,http_opus,hls_opus,http_mp3,hls_mp3`

#### orfon (orf:on)
* `prefer_segments_playlist`：在可用时优先选择节目段播放列表而不是单个完整视频。如果需要单个段，请使用 `--concat-playlist never --extractor-args "orfon:prefer_segments_playlist"`

#### bilibili
* `prefer_multi_flv`：对于仍提供旧格式的较旧视频，优先提取 flv 格式而不是 mp4 格式

#### sonylivseries
* `sort_order`：系列提取的剧集排序顺序 - `asc`（升序，最旧的在前）或 `desc`（降序，最新的在前）之一。默认为 `asc`

#### tver
* `backend`：用于提取的后端 API - `streaks`（默认）或 `brightcove`（已弃用）之一

#### vimeo
* `client`：从中提取视频数据的客户端。当前可用的客户端有 `android`、`ios`、`macos` 和 `web`。只能使用一个客户端。默认使用 `macos` 客户端，但在登录时使用 `web` 客户端。`web` 客户端仅适用于帐户 cookie 或登录凭据。`android` 和 `ios` 客户端仅适用于以前缓存的 OAuth 令牌
* `original_format_policy`：何时尝试提取原始格式的策略。`always`、`never` 或 `auto` 之一。默认的 `auto` 策略仅在 Vimeo 公布视频的可下载性时才发出额外请求，以避免超过 Web 客户端的 API 速率限制

**注意**：这些选项可能会在未来更改/删除，而不考虑向后兼容性

<!-- MANPAGE: MOVE "INSTALLATION" SECTION HERE -->


# 插件

请注意，**所有**插件都会被导入，即使未被调用，并且**不对插件代码执行任何检查**。**请自行承担使用插件的风险，并且仅在您信任代码时使用！**

插件可以是 `<type>` 为 `extractor` 或 `postprocessor` 的类型。
- 提取器插件不需要从 CLI 启用，当输入 URL 适合时会自动调用。
- 提取器插件优先于内置提取器。
- 后处理器插件可以使用 `--use-postprocessor NAME` 调用。


插件从命名空间包 `yt_dlp_plugins.extractor` 和 `yt_dlp_plugins.postprocessor` 加载。

换句话说，磁盘上的文件结构如下所示：

        yt_dlp_plugins/
            extractor/
                myplugin.py
            postprocessor/
                myplugin.py

yt-dlp 在许多位置（见下文）中查找这些 `yt_dlp_plugins` 命名空间文件夹，并从**所有**文件夹中加载插件。
将环境变量 `YTDLP_NO_PLUGINS` 设置为非空值以完全禁用加载插件。

请参阅 [wiki 了解一些已知插件](https://github.com/yt-dlp/yt-dlp/wiki/Plugins)

## 安装插件

可以使用各种方法和位置安装插件。

1. **配置目录**：
   插件包（包含 `yt_dlp_plugins` 命名空间文件夹）可以放入以下标准[配置位置](#configuration)：
    * **用户插件**
      * `${XDG_CONFIG_HOME}/yt-dlp/plugins/<package name>/yt_dlp_plugins/`（推荐在 Linux/macOS 上使用）
      * `${XDG_CONFIG_HOME}/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
      * `${APPDATA}/yt-dlp/plugins/<package name>/yt_dlp_plugins/`（推荐在 Windows 上使用）
      * `${APPDATA}/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
      * `~/.yt-dlp/plugins/<package name>/yt_dlp_plugins/`
      * `~/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
    * **系统插件**
      * `/etc/yt-dlp/plugins/<package name>/yt_dlp_plugins/`
      * `/etc/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
2. **可执行文件位置**：插件包可以类似地安装在可执行文件位置下的 `yt-dlp-plugins` 目录中（推荐用于便携式安装）：
    * 二进制文件：其中 `<root-dir>/yt-dlp.exe`，`<root-dir>/yt-dlp-plugins/<package name>/yt_dlp_plugins/`
    * 源代码：其中 `<root-dir>/yt_dlp/__main__.py`，`<root-dir>/yt-dlp-plugins/<package name>/yt_dlp_plugins/`

3. **pip 和 `PYTHONPATH` 中的其他位置**
    * 插件包可以使用 `pip` 安装和管理。有关示例，请参阅 [yt-dlp-sample-plugins](https://github.com/yt-dlp/yt-dlp-sample-plugins)。
      * 注意：使用 pip 安装的插件包之间的插件文件必须具有唯一的文件名。
    * 搜索 `PYTHONPATH` 中的任何路径以查找 `yt_dlp_plugins` 命名空间文件夹。
      * 注意：这不适用于 Pyinstaller 构建。


在其根目录中包含 `yt_dlp_plugins` 命名空间文件夹的 `.zip`、`.egg` 和 `.whl` 归档文件也支持作为插件包。

* 例如 `${XDG_CONFIG_HOME}/yt-dlp/plugins/mypluginpkg.zip`，其中 `mypluginpkg.zip` 包含 `yt_dlp_plugins/<type>/myplugin.py`

使用 `--verbose` 运行 yt-dlp 以检查插件是否已加载。

## 开发插件

请参阅 [yt-dlp-sample-plugins](https://github.com/yt-dlp/yt-dlp-sample-plugins) 存储库以获取模板插件包，并参阅 wiki 的 [插件开发](https://github.com/yt-dlp/yt-dlp/wiki/Plugin-Development) 部分以获取插件开发指南。

从每个文件中分别导入名称以 `IE`/`PP` 结尾的所有公共类，用于提取器和后处理器。这尊重下划线前缀（例如 `_MyBasePluginIE` 是私有的）和 `__all__`。可以通过在模块名前加上下划线来类似地排除模块（例如 `_myplugin.py`）。

要使用子类替换现有提取器，请设置 `plugin_name` 类关键字参数（例如 `class MyPluginIE(ABuiltInIE, plugin_name='myplugin')` 将用 `MyPluginIE` 替换 `ABuiltInIE`）。由于提取器替换了父类，您应该通过使用上述方法之一使子类提取器成为私有来排除它被单独导入。

如果您是插件作者，请将 [yt-dlp-plugins](https://github.com/topics/yt-dlp-plugins) 作为主题添加到您的存储库以提高可发现性。

请参阅 [开发者说明](https://github.com/yt-dlp/yt-dlp/blob/master/CONTRIBUTING.md#developer-instructions) 了解如何编写和测试提取器。

# 嵌入 YT-DLP

yt-dlp 尽最大努力成为一个优秀的命令行程序，因此应该可以从任何编程语言调用。

您的程序应该避免解析正常的 stdout，因为它们可能会在将来的版本中更改。相反，它们应该使用 `-J`、`--print`、`--progress-template`、`--exec` 等选项来创建可以可靠地重现和解析的控制台输出。

从 Python 程序中，您可以以更强大的方式嵌入 yt-dlp，如下所示：

```python
from yt_dlp import YoutubeDL

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']
with YoutubeDL() as ydl:
    ydl.download(URLS)
```

很可能，您需要使用各种选项。有关可用选项的列表，请查看 [`yt_dlp/YoutubeDL.py`](yt_dlp/YoutubeDL.py#L183) 或 Python shell 中的 `help(yt_dlp.YoutubeDL)`。如果您已经熟悉 CLI，可以使用 [`devscripts/cli_to_api.py`](https://github.com/yt-dlp/yt-dlp/blob/master/devscripts/cli_to_api.py) 将任何 CLI 开关转换为 `YoutubeDL` 参数。

**提示**：如果您将代码从 youtube-dl 移植到 yt-dlp，需要注意的一个重要点是，我们不保证 `YoutubeDL.extract_info` 的返回值是 json 可序列化的，甚至是字典。它将是类似字典的，但如果您想确保它是可序列化的字典，请通过 `YoutubeDL.sanitize_info` 传递它，如下面的[示例](#extracting-information)所示

## 嵌入示例

#### 提取信息

```python
import json
import yt_dlp

URL = 'https://www.youtube.com/watch?v=BaW_jenozKc'

# ℹ️ 有关可用选项和公共函数的列表，请参阅 help(yt_dlp.YoutubeDL)
ydl_opts = {}
with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    info = ydl.extract_info(URL, download=False)

    # ℹ️ ydl.sanitize_info 使信息可 json 序列化
    print(json.dumps(ydl.sanitize_info(info)))
```
#### 使用 info-json 下载

```python
import yt_dlp

INFO_FILE = 'path/to/video.info.json'

with yt_dlp.YoutubeDL() as ydl:
    error_code = ydl.download_with_info_file(INFO_FILE)

print('Some videos failed to download' if error_code
      else 'All videos successfully downloaded')
```

#### 提取音频

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

ydl_opts = {
    'format': 'm4a/bestaudio/best',
    # ℹ️ 有关可用的后处理器及其参数的列表，请参阅 help(yt_dlp.postprocessor)
    'postprocessors': [{  # 使用 ffmpeg 提取音频
        'key': 'FFmpegExtractAudio',
        'preferredcodec': 'm4a',
    }]
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    error_code = ydl.download(URLS)
```

#### 过滤视频

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

def longer_than_a_minute(info, *, incomplete):
    """仅下载长于一分钟的视频（或持续时间未知的视频）"""
    duration = info.get('duration')
    if duration and duration < 60:
        return 'The video is too short'

ydl_opts = {
    'match_filter': longer_than_a_minute,
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    error_code = ydl.download(URLS)
```

#### 添加日志记录器和进度挂钩

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

class MyLogger:
    def debug(self, msg):
        # 为了与 youtube-dl 兼容，debug 和 info 都会传递到 debug 中
        # 您可以通过前缀 '[debug] ' 来区分它们
        if msg.startswith('[debug] '):
            pass
        else:
            self.info(msg)

    def info(self, msg):
        pass

    def warning(self, msg):
        pass

    def error(self, msg):
        print(msg)


# ℹ️ 请参阅 help(yt_dlp.YoutubeDL) 中的 "progress_hooks"
def my_hook(d):
    if d['status'] == 'finished':
        print('Done downloading, now post-processing ...')


ydl_opts = {
    'logger': MyLogger(),
    'progress_hooks': [my_hook],
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    ydl.download(URLS)
```

#### 添加自定义后处理器

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

# ℹ️ 请参阅 help(yt_dlp.postprocessor.PostProcessor)
class MyCustomPP(yt_dlp.postprocessor.PostProcessor):
    def run(self, info):
        self.to_screen('Doing stuff')
        return [], info


with yt_dlp.YoutubeDL() as ydl:
    # ℹ️ "when" 可以采用 yt_dlp.utils.POSTPROCESS_WHEN 中的任何值
    ydl.add_post_processor(MyCustomPP(), when='pre_process')
    ydl.download(URLS)
```


#### 使用自定义格式选择器

```python
import yt_dlp

URLS = ['https://www.youtube.com/watch?v=BaW_jenozKc']

def format_selector(ctx):
    """ 选择最佳视频和最佳音频，不会导致 mkv。
    注意：这只是一个示例，并不处理所有情况 """

    # 格式已经从最差到最佳排序
    formats = ctx.get('formats')[::-1]

    # acodec='none' 表示没有音频
    best_video = next(f for f in formats
                      if f['vcodec'] != 'none' and f['acodec'] == 'none')

    # 查找兼容的音频扩展名
    audio_ext = {'mp4': 'm4a', 'webm': 'webm'}[best_video['ext']]
    # vcodec='none' 表示没有视频
    best_audio = next(f for f in formats if (
        f['acodec'] != 'none' and f['vcodec'] == 'none' and f['ext'] == audio_ext))

    # 这些是合并格式的最低必需字段
    yield {
        'format_id': f'{best_video["format_id"]}+{best_audio["format_id"]}',
        'ext': best_video['ext'],
        'requested_formats': [best_video, best_audio],
        # 必须是 + 分隔的协议列表
        'protocol': f'{best_video["protocol"]}+{best_audio["protocol"]}'
    }


ydl_opts = {
    'format': format_selector,
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    ydl.download(URLS)
```


# 与 YOUTUBE-DL 的变化

### 新功能

* 从 [**yt-dlc@f9401f2**](https://github.com/blackjack4494/yt-dlc/commit/f9401f2a91987068139c5f757b12fc711d4c0cee) 分支并与 [**youtube-dl@a08f2b7**](https://github.com/ytdl-org/youtube-dl/commit/a08f2b7e4567cdc50c0614ee0a4ffdff49b8b6e6) 合并（[例外](https://github.com/yt-dlp/yt-dlp/issues/21)）

* **[SponsorBlock 集成](#sponsorblock-options)**：您可以通过利用 [SponsorBlock](https://sponsor.ajay.app) API 来标记/删除 YouTube 视频中的赞助商部分

* **[格式排序](#sorting-formats)**：默认格式排序选项已更改，因此现在首选更高的分辨率和更好的编解码器，而不是简单地使用更大的比特率。此外，您现在可以使用 `-S` 指定排序顺序。这比仅使用 `--format` 更容易进行格式选择（[示例](#format-selection-examples)）

* **与 animelover1984/youtube-dl 合并**：您可以从 [animelover1984/youtube-dl](https://github.com/animelover1984/youtube-dl) 获得大部分功能和改进，包括 `--write-comments`、`BiliBiliSearch`、`BilibiliChannel`、在 mp4/ogg/opus 中嵌入缩略图、播放列表 infojson 等。有关详细信息，请参阅 [#31](https://github.com/yt-dlp/yt-dlp/pull/31)。

* **YouTube 改进**：
    * 支持 Clips、Stories（`ytstories:<channel UCID>`）、搜索（包括过滤器）**\***、YouTube 音乐搜索、频道特定搜索、搜索前缀（`ytsearch:`）**\***、Mixes 和订阅源（`:ytfav`、`:ytwatchlater`、`:ytsubs`、`:ythistory`、`:ytrec`、`:ytnotif`）
    * 修复 [基于 n-sig 的限速](https://github.com/ytdl-org/youtube-dl/issues/29326) **\***
    * 使用 `--live-from-start` 从开始下载直播（*实验性*）
    * 频道 URL 下载频道的所有上传内容，包括 shorts 和直播

* **从浏览器获取 Cookie**：可以使用 `--cookies-from-browser BROWSER[+KEYRING][:PROFILE][::CONTAINER]` 从所有主要 Web 浏览器自动提取 Cookie

* **下载时间范围**：可以使用 `--download-sections` 根据时间戳或章节部分下载视频

* **按章节分割视频**：可以使用 `--split-chapters` 根据章节将视频分割为多个文件

* **多线程片段下载**：并行下载 m3u8/mpd 视频的多个片段。使用 `--concurrent-fragments`（`-N`）选项设置使用的线程数

* **HLS/DASH 使用 Aria2c**：您可以使用 `aria2c` 作为 DASH(mpd) 和 HLS(m3u8) 格式的外部下载器

* **新的和修复的提取器**：添加了许多新的提取器，并修复了许多现有的提取器。请参阅 [更新日志](https://github.com/yt-dlp/yt-dlp/blob/master/Changelog.md) 或 [支持的站点列表](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md)

* **新的 MSO**：Philo、Spectrum、SlingTV、Cablevision、RCN 等

* **从清单中提取字幕**：可以从流媒体清单中提取字幕。有关详细信息，请参阅 [commit/be6202f](https://github.com/yt-dlp/yt-dlp/commit/be6202f12b97858b9d716e608394b51065d0419f)

* **多个路径和输出模板**：您可以为不同类型的文件提供不同的[输出模板](#output-template)和下载路径。您还可以使用 `--paths`（`-P`）设置中间文件下载到的临时路径

* **便携式配置**：配置文件从主目录和根目录自动加载。有关详细信息，请参阅 [CONFIGURATION](#configuration)

* **输出模板改进**：输出模板现在可以具有日期时间格式化、数字偏移、对象遍历等。有关详细信息，请参阅 [输出模板](#output-template)。借助 `--parse-metadata` 和 `--replace-in-metadata` 还可以执行更高级的操作

* **其他新选项**：添加了许多新选项，例如 `--alias`、`--print`、`--concat-playlist`、`--wait-for-video`、`--retry-sleep`、`--sleep-requests`、`--convert-thumbnails`、`--force-download-archive`、`--force-overwrites`、`--break-match-filters` 等

* **改进**：`--format`/`--match-filters` 中的正则表达式和其他运算符、多个 `--postprocessor-args` 和 `--downloader-args`、更快的存档检查、更多[格式选择选项](#format-selection)、合并多视频/音频、多个 `--config-locations`、不同阶段的 `--exec` 等

* **插件**：提取器和后处理器可以从外部文件加载。有关详细信息，请参阅 [插件](#plugins)

* **自动更新器**：可以使用 `yt-dlp -U` 更新版本，如果需要，可以使用 `--update-to` 降级

* **自动构建**：可以使用 `--update-to nightly` 和 `--update-to master` 使用 [Nightly/master 构建](#update-channels)

请参阅 [更新日志](https://github.com/yt-dlp/yt-dlp/blob/master/Changelog.md) 或 [提交](https://github.com/yt-dlp/yt-dlp/commits) 以获取完整的更改列表

标有 **\*** 的功能已反向移植到 youtube-dl

### 默认行为的差异

yt-dlp 的一些默认选项与 youtube-dl 和 youtube-dlc 不同：

* yt-dlp 仅支持 [Python 3.10+](## "Windows 8")，并且会在更多版本[成为 EOL](https://devguide.python.org/versions/#python-release-cycle)时移除对它们的支持；而 [youtube-dl 仍然支持 Python 2.6+ 和 3.2+](https://github.com/ytdl-org/youtube-dl/issues/30568#issue-1118238743)
* 选项 `--auto-number`（`-A`）、`--title`（`-t`）和 `--literal`（`-l`）不再起作用。有关详细信息，请参阅 [已删除的选项](#Removed)
* 不支持将 `avconv` 作为 `ffmpeg` 的替代品
* yt-dlp 在与 youtube-dl 略有不同的位置存储配置文件。有关正确位置列表，请参阅 [CONFIGURATION](#configuration)
* 默认[输出模板](#output-template)是 `%(title)s [%(id)s].%(ext)s`。此更改没有真正的理由。这是在 yt-dlp 公开之前更改的，现在没有计划将其更改回 `%(title)s-%(id)s.%(ext)s`。相反，您可以使用 `--compat-options filename`
* 默认[格式排序](#sorting-formats)与 youtube-dl 不同，首选更高的分辨率和更好的编解码器，而不是更高的比特率。您可以使用 `--format-sort` 选项将其更改为您喜欢的任何顺序，或使用 `--compat-options format-sort` 使用 youtube-dl 的排序顺序。旧版本的 yt-dlp 由于 VP9 的更广泛兼容性而首选 VP9；您可以使用 `--compat-options prefer-vp9-sort` 恢复到该格式排序首选项。这两个兼容选项不能一起使用
* 默认格式选择器是 `bv*+ba/b`。这意味着如果找到比最佳仅视频格式更好的组合视频 + 音频格式，则首选前者。使用 `-f bv+ba/b` 或 `--compat-options format-spec` 恢复此设置
* 与 youtube-dlc 不同，yt-dlp 默认不允许将多个音频/视频流合并到一个文件中（因为这与使用 `-f bv*+ba` 冲突）。如果需要，必须使用 `--audio-multistreams` 和 `--video-multistreams` 启用此功能。您还可以使用 `--compat-options multistreams` 启用两者
* 默认启用 `--no-abort-on-error`。使用 `--abort-on-error` 或 `--compat-options abort-on-error` 在错误时中止
* 编写元数据文件（如缩略图、描述或 infojson）时，相同的信息（如果可用）也会为播放列表编写。使用 `--no-write-playlist-metafiles` 或 `--compat-options no-playlist-metafiles` 不编写这些文件
* 当与 `--write-info-json` 一起使用时，`--add-metadata` 除了编写元数据外，还会将 `infojson` 附加到 `mkv` 文件。使用 `--no-embed-info-json` 或 `--compat-options no-attach-info-json` 恢复此设置
* 与 youtube-dl 相比，使用 `--add-metadata` 时，某些元数据嵌入到不同的字段中。最值得注意的是，`comment` 字段包含 `webpage_url`，`synopsis` 包含 `description`。您可以[使用 `--parse-metadata`](#modifying-metadata) 根据您的喜好修改此设置，或使用 `--compat-options embed-metadata` 恢复此设置
* 与 `--playlist-reverse` 和 `--playlist-items` 等选项一起使用时，`playlist_index` 的行为不同。有关详细信息，请参阅 [#302](https://github.com/yt-dlp/yt-dlp/issues/302)。如果您想保留较早的行为，可以使用 `--compat-options playlist-index`
* `-F` 的输出以新格式列出。使用 `--compat-options list-formats` 恢复此设置
* 实时聊天（如果可用）被视为字幕。使用 `--sub-langs all,-live_chat` 下载除实时聊天之外的所有字幕。您还可以使用 `--compat-options no-live-chat` 防止下载任何实时聊天/弹幕
* YouTube 频道 URL 下载频道的所有上传内容。要仅下载特定选项卡中的视频，请传递选项卡的 URL。如果频道不显示请求的选项卡，则会引发错误。此外，如果没有实时视频，`/live` URL 会引发错误，而不是静默下载整个频道。您可以使用 `--compat-options no-youtube-channel-redirect` 恢复所有这些重定向
* YouTube 播放列表也会列出不可用的视频。使用 `--compat-options no-youtube-unavailable-videos` 删除此设置
* 从 YouTube 提取的上传日期是 UTC 格式。
* 如果 `ffmpeg` 用作下载器，则在可能的情况下，格式的下载和合并在单个步骤中完成。使用 `--compat-options no-direct-merge` 恢复此设置
* 如果可能，使用 mutagen 在 `mp4` 中嵌入缩略图。使用 `--compat-options embed-thumbnail-atomicparsley` 强制使用 AtomicParsley 代替
* 默认情况下，某些内部元数据（如文件名）会从 infojson 中删除。使用 `--no-clean-infojson` 或 `--compat-options no-clean-infojson` 恢复此设置
* 当 `--embed-subs` 和 `--write-subs` 一起使用时，字幕会写入磁盘并嵌入到媒体文件中。您可以仅使用 `--embed-subs` 嵌入字幕并自动删除单独的文件。有关更多信息，请参阅 [#630 (comment)](https://github.com/yt-dlp/yt-dlp/issues/630#issuecomment-893659460)。可以使用 `--compat-options no-keep-subs` 恢复此设置
* 如果安装了 `certifi`，则将其用于 SSL 根证书。如果要使用系统证书（例如自签名），请使用 `--compat-options no-certifi`
* yt-dlp 对文件名中无效字符的清理与 youtube-dl 不同/更智能。您可以使用 `--compat-options filename-sanitization` 恢复到 youtube-dl 的行为
* ~~yt-dlp 尝试尽可能将外部下载器输出解析为标准进度输出（当前已实现：[aria2c](https://github.com/yt-dlp/yt-dlp/issues/5931)）。您可以使用 `--compat-options no-external-downloader-progress` 获取下载器输出的原始内容~~
* 2021.09.01 和 2023.01.02 之间的 yt-dlp 版本将 `--match-filters` 应用于嵌套播放列表。这是 [8f18ac](https://github.com/yt-dlp/yt-dlp/commit/8f18aca8717bb0dd49054555af8d386e5eda3a88) 的意外副作用，并在 [d7b460](https://github.com/yt-dlp/yt-dlp/commit/d7b460d0e5fc710950582baed2e3fc616ed98a80) 中修复。使用 `--compat-options playlist-match-filter` 恢复此设置
* 2021.11.10 和 2023.06.21 之间的 yt-dlp 版本估计碎片/清单格式的 `filesize_approx` 值。这是为了方便起见在 [f2fe69](https://github.com/yt-dlp/yt-dlp/commit/f2fe69c7b0d208bdb1f6292b4ae92bc1e1a7444a) 中添加的，但由于估计值可能极其不准确，因此在 [0dff8e](https://github.com/yt-dlp/yt-dlp/commit/0dff8e4d1e6e9fb938f4256ea9af7d81f42fd54f) 中恢复。使用 `--compat-options manifest-filesize-approx` 继续提取估计值
* yt-dlp 使用现代 http 客户端后端，如 `requests`。使用 `--compat-options prefer-legacy-http-handler` 首选传统 http 处理程序（`urllib`）用于标准 http 请求。
* 子模块 `swfinterp`、`casefold` 已被删除。
* 传递 `--simulate`（或使用 `download=False` 调用 `extract_info`）不再更改默认格式选择。有关详细信息，请参阅 [#9843](https://github.com/yt-dlp/yt-dlp/issues/9843)。
* yt-dlp 默认不再将服务器修改时间应用于下载的文件。使用 `--mtime` 或 `--compat-options mtime-by-default` 恢复此设置。

为了方便起见，可以使用一些兼容选项别名：

* `--compat-options all`：使用所有兼容选项（**不要使用此选项！**）
* `--compat-options youtube-dl`：与 `--compat-options all,-multistreams,-playlist-match-filter,-manifest-filesize-approx,-allow-unsafe-ext,-prefer-vp9-sort` 相同
* `--compat-options youtube-dlc`：与 `--compat-options all,-no-live-chat,-no-youtube-channel-redirect,-playlist-match-filter,-manifest-filesize-approx,-allow-unsafe-ext,-prefer-vp9-sort` 相同
* `--compat-options 2021`：与 `--compat-options 2022,no-certifi,filename-sanitization` 相同
* `--compat-options 2022`：与 `--compat-options 2023,playlist-match-filter,no-external-downloader-progress,prefer-legacy-http-handler,manifest-filesize-approx` 相同
* `--compat-options 2023`：与 `--compat-options 2024,prefer-vp9-sort` 相同
* `--compat-options 2024`：与 `--compat-options 2025,mtime-by-default` 相同
* `--compat-options 2025`：目前不起作用。使用此选项启用所有未来的兼容选项

使用年度兼容选项别名之一会将 yt-dlp 的默认行为固定到该日历年度*结束*时的行为。

以下兼容选项恢复安全补丁之前的易受攻击的行为：

* `--compat-options allow-unsafe-ext`：允许下载具有任何扩展名（包括不安全的扩展名）的文件（[GHSA-79w7-vh3h-8g4j](<https://github.com/yt-dlp/yt-dlp/security/advisories/GHSA-79w7-vh3h-8g4j>)）

    > :warning: 仅当有效的文件下载因其扩展名被检测为不常见而被拒绝时使用
    >
    > **此选项可以启用远程代码执行！请考虑改为[打开问题](<https://github.com/yt-dlp/yt-dlp/issues/new/choose>)！**

### 已弃用的选项

这些是所有已弃用的选项以及实现相同效果的当前替代方案

#### 几乎冗余的选项
虽然这些选项与其新对应项几乎相同，但存在一些差异，使它们不冗余

    -j, --dump-json                  --print "%()j"
    -F, --list-formats               --print formats_table
    --list-thumbnails                --print thumbnails_table --print playlist:thumbnails_table
    --list-subs                      --print automatic_captions_table --print subtitles_table

#### 冗余选项
虽然这些选项是冗余的，但由于易于使用，仍然预期会被使用

    --get-description                --print description
    --get-duration                   --print duration_string
    --get-filename                   --print filename
    --get-format                     --print format
    --get-id                         --print id
    --get-thumbnail                  --print thumbnail
    -e, --get-title                  --print title
    -g, --get-url                    --print urls
    --match-title REGEX              --match-filters "title ~= (?i)REGEX"
    --reject-title REGEX             --match-filters "title !~= (?i)REGEX"
    --min-views COUNT                --match-filters "view_count >=? COUNT"
    --max-views COUNT                --match-filters "view_count <=? COUNT"
    --break-on-reject                使用 --break-match-filters
    --user-agent UA                  --add-headers "User-Agent:UA"
    --referer URL                    --add-headers "Referer:URL"
    --playlist-start NUMBER          -I NUMBER:
    --playlist-end NUMBER            -I :NUMBER
    --playlist-reverse               -I ::-1
    --no-playlist-reverse            默认
    --no-colors                      --color no_color

#### 不推荐
虽然这些选项仍然有效，但不推荐使用它们，因为还有其他替代方案可以实现相同的效果

    --force-generic-extractor        --ies generic,default
    --exec-before-download CMD       --exec "before_dl:CMD"
    --no-exec-before-download        --no-exec
    --all-formats                    -f all
    --all-subs                       --sub-langs all --write-subs
    --print-json                     -j --no-simulate
    --autonumber-size NUMBER         使用字符串格式化，例如 %(autonumber)03d
    --autonumber-start NUMBER        使用内部字段格式化，如 %(autonumber+NUMBER)s
    --id                             -o "%(id)s.%(ext)s"
    --metadata-from-title FORMAT     --parse-metadata "%(title)s:FORMAT"
    --hls-prefer-native              --downloader "m3u8:native"
    --hls-prefer-ffmpeg              --downloader "m3u8:ffmpeg"
    --list-formats-old               --compat-options list-formats（别名：--no-list-formats-as-table）
    --list-formats-as-table          --compat-options -list-formats [默认]
    --geo-bypass                     --xff "default"
    --no-geo-bypass                  --xff "never"
    --geo-bypass-country CODE        --xff CODE
    --geo-bypass-ip-block IP_BLOCK   --xff IP_BLOCK

#### 开发者选项
这些选项不打算供最终用户使用

    --test                           仅下载视频的一部分以测试提取器
    --load-pages                     加载由 --write-pages 转储的页面
    --allow-unplayable-formats       同时列出不可播放的格式
    --no-allow-unplayable-formats    默认

#### 旧别名
这些是由于各种原因不再记录的别名

    --clean-infojson                 --clean-info-json
    --force-write-download-archive   --force-write-archive
    --no-clean-infojson              --no-clean-info-json
    --no-split-tracks                --no-split-chapters
    --no-write-srt                   --no-write-subs
    --prefer-unsecure                --prefer-insecure
    --rate-limit RATE                --limit-rate RATE
    --split-tracks                   --split-chapters
    --srt-lang LANGS                 --sub-langs LANGS
    --trim-file-names LENGTH         --trim-filenames LENGTH
    --write-srt                      --write-subs
    --yes-overwrites                 --force-overwrites

#### SponSkrub 选项
对 [SponSkrub](https://github.com/faissaloo/SponSkrub) 的支持已被移除，取而代之的是 `--sponsorblock` 选项

    --sponskrub                      --sponsorblock-mark all
    --no-sponskrub                   --no-sponsorblock
    --sponskrub-cut                  --sponsorblock-remove all
    --no-sponskrub-cut               --sponsorblock-remove -all
    --sponskrub-force                不适用
    --no-sponskrub-force             不适用
    --sponskrub-location             不适用
    --sponskrub-args                 不适用

#### 不再支持
这些选项可能不再按预期工作

    --prefer-avconv                  avconv 不受 yt-dlp 官方支持（别名：--no-prefer-ffmpeg）
    --prefer-ffmpeg                  默认（别名：--no-prefer-avconv）
    -C, --call-home                  未实现
    --no-call-home                   默认
    --include-ads                    不再支持
    --no-include-ads                 默认
    --write-annotations              没有支持的站点现在有注释
    --no-write-annotations           默认
    --avconv-location                已移除 --ffmpeg-location 的别名
    --cn-verification-proxy URL      已移除 --geo-verification-proxy URL 的别名
    --dump-headers                   已移除 --print-traffic 的别名
    --dump-intermediate-pages        已移除 --dump-pages 的别名
    --youtube-skip-dash-manifest     已移除 --extractor-args "youtube:skip=dash" 的别名（别名：--no-youtube-include-dash-manifest）
    --youtube-skip-hls-manifest      已移除 --extractor-args "youtube:skip=hls" 的别名（别名：--no-youtube-include-hls-manifest）
    --youtube-include-dash-manifest  默认（别名：--no-youtube-skip-dash-manifest）
    --youtube-include-hls-manifest   默认（别名：--no-youtube-skip-hls-manifest）
    --youtube-print-sig-code         已移除测试功能
    --dump-user-agent                不再支持
    --xattr-set-filesize             不再支持
    --compat-options seperate-video-versions  不再需要
    --compat-options no-youtube-prefer-utc-upload-date  不再支持

#### 已删除
这些选项自 2014 年以来已被弃用，现在已完全删除

    -A, --auto-number                -o "%(autonumber)s-%(id)s.%(ext)s"
    -t, -l, --title, --literal       -o "%(title)s-%(id)s.%(ext)s"


# 贡献
请参阅 [CONTRIBUTING.md](https://github.com/yt-dlp/yt-dlp/blob/master/CONTRIBUTING.md#contributing-to-yt-dlp) 以获取有关[打开问题](https://github.com/yt-dlp/yt-dlp/blob/master/CONTRIBUTING.md#opening-an-issue)和[为项目贡献代码](https://github.com/yt-dlp/yt-dlp/blob/master/CONTRIBUTING.md#developer-instructions)的说明

# WIKI
请参阅 [Wiki](https://github.com/yt-dlp/yt-dlp/wiki) 以获取更多信息
