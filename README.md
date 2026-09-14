# Практична робота № 1

**Дисципліна:** Основи побудови інформаційних систем та мереж

**Тема:** Спостереження за процесом звернення до вебресурсу. Побудова власної моделі рівнів взаємодії

| | |
|---|---|
| **Прізвище, ім'я** | Кузьменко Дмитро |
| **Група** | ІПЗ-2.01 |
| **Номер варіанта** | 13 |
| **Домен варіанта** | voidlinux.org |
| **Середовище виконання** | *Windows* |
| **Версія curl** | *curl 8.13.0 (Windows) libcurl/8.13.0 Schannel zlib/1.3.1 WinIDN* |
| **Дата виконання** | 13.09.26 |

---

## Частина A. Збір експериментальних даних

### A.1. Запит із діагностичним виводом

**Команда:**

```
curl -v https://voidlinux.org
```

**Вивід:**

```
* Host voidlinux.org:443 was resolved.
* IPv6: (none)
* IPv4: 185.199.109.153
*   Trying 185.199.109.153:443...
* schannel: disabled automatic use of client certificate
* ALPN: curl offers http/1.1
* ALPN: server accepted http/1.1
* Connected to voidlinux.org (185.199.109.153) port 443
* using HTTP/1.x
> GET / HTTP/1.1
> Host: voidlinux.org
> User-Agent: curl/8.13.0
> Accept: */*
>
* Request completely sent off
< HTTP/1.1 200 OK
< Connection: keep-alive
< Content-Length: 23199
< Server: GitHub.com
< Content-Type: text/html; charset=utf-8
< Last-Modified: Tue, 10 Mar 2026 22:49:51 GMT
< Access-Control-Allow-Origin: *
< Strict-Transport-Security: max-age=31557600
< ETag: "69b0a00f-5a9f"
< expires: Mon, 07 Sep 2026 11:46:23 GMT
< Cache-Control: max-age=600
< x-proxy-cache: MISS
< X-GitHub-Request-Id: BDB2:1F6248:4EE74A4:4FC3943:6A9EA1B7
< x-github-edge-region: fra
< Accept-Ranges: bytes
< Date: Sun, 13 Sep 2026 08:53:31 GMT
< Via: 1.1 varnish
< Age: 288
< X-Served-By: cache-fra-eddf8230129-FRA
< X-Cache: HIT
< X-Cache-Hits: 1
< X-Timer: S1789289612.835201,VS0,VE12
< Vary: Accept-Encoding
< X-Fastly-Request-ID: 33192770e1406c93878955247b78f3649f64cde6
<
<!DOCTYPE html>
<html lang="en" prefix="og: https://ogp.me/ns# article: http://ogp.me/ns/article#">
        <head>
                <meta charset="utf-8">
                <meta http-equiv="X-UA-Compatible" content="IE=edge">
                <meta name="viewport" content="width=device-width, initial-scale=1">
                <title>Enter the void</title>

                <meta property="og:title" content="Enter the void">

                <meta property="og:description" content="Welcome to the Void">

                <meta property="og:site_name" content="Void Linux">
                <meta property="og:image:url" content="/assets/img/voidlogo.png">
                <meta property="og:image:alt" content="Void Linux Logo">
                <meta name="theme-color" content="#478061">

                <link rel="icon" type="image/png" href="/assets/img/favicon.png" />
                <link rel="stylesheet" href="/assets/css/bootstrap.min.css">
                <link rel="stylesheet" href="/assets/css/screen.css">
                <link rel="stylesheet" href="/assets/css/misc.css">
                <link href='/assets/css/font-ubuntu.css' rel='stylesheet' type='text/css'>

                <link rel="alternate" type="application/atom+xml" title="Void Linux News feed" href="/atom.xml" />
                <script src="/assets/js/jquery.min.js"></script>
                <script src="/assets/js/bootstrap.min.js"></script>
                <script src="/assets/js/tabbar.js"></script>
        </head>
        <body role="document">
                <nav class="navbar navbar-default navbar-inverse navbar-sticky" role="navigation">
                        <div class="container">
                                <div class="navbar-header">
                                        <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#void-collapsed-navbar">
                                                <span class="sr-only">Toggle navigation</span>
                                                <span class="icon-bar"></span>
                                                <span class="icon-bar"></span>
                                                <span class="icon-bar"></span>
                                        </button>
                                </div>
                                <div class="collapse navbar-collapse" id="void-collapsed-navbar">
                                        <ul class="nav navbar-left navbar-nav">
                                                <li><a href="/">Home</a></li>
                                                <li><a href="/news/">News</a></li>
                                                <li><a href="/download/">Download</a></li>
                                                <li><a href="/packages/">Packages</a></li>
                                                <li><a href="/acknowledgments/">Acknowledgments</a></li>
                                        </ul>
                                        <ul class="nav navbar-right navbar-nav">
                                                <li><a href="https://docs.voidlinux.org">Documentation</a></li>
                                                <li><a href="https://man.voidlinux.org/">Manual Pages</a></li>
                                                <li><a href="https://xmirror.voidlinux.org/">Mirrors</a></li>
                                                <li><a href="https://github.com/void-linux">GitHub</a></li>
                                        </ul>
                                </div>
                        </div>
                </nav>
                <div class="container">
                        <div class="row">
        <div class="col-md-3">
                <div id="davoid">

                        <img class="bg img-responsive standard-mode" alt="void logo" src="/assets/img/void_bg.png">
                        <img class="fg img-responsive standard-mode" alt="void logo">

                </div>
        </div>
        <div class="col-md-9">
                <h2>The Void (Linux) distribution</h2>
                <p>
                Void is a general purpose operating system, based on the monolithic <a href="https://www.kernel.org">Linux</a> kernel. Its package system allows you to quickly install, update and remove software; software is provided in binary packages or can be built directly from sources with the help of the XBPS source packages collection.
                </p>
                <p>It is available for a variety of platforms. Software packages can be built natively or cross compiled through the <a href="https://github.com/void-linux/void-packages">XBPS source packages collection</a>.
                </p>
                <p>Follow us on <a rel="me" href="https://chaos.social/@voidlinux" title="Void on Mastodon">Mastodon</a>, visit the <a href="ircs://irc.libera.chat/#voidlinux">#voidlinux</a> IRC channel on <a href="https://libera.chat">libera.chat</a>, and join the <a href="https://www.reddit.com/r/voidlinux/">Void Linux subreddit</a>.
                </p>
                <p>Visit the <a href="https://build.voidlinux.org" title="Void builder">Void build server console</a> for package build status updates.
                </p>
                <p>Contribute to the Void Linux project by <a href="https://github.com/void-linux/void-packages/blob/master/CONTRIBUTING.md">adding and updating packages</a> and <a href="https://github.com/void-linux/void-docs/blob/master/CONTRIBUTING.md">extending the documentation</a>. More information can be found <a href="https://docs.voidlinux.org/contributing/index.html">in the Handbook</a>.
                </p>
        </div>
</div>
<hr>
<div class="container">
        <div class="row">
                <div class="col-md-4">
                        <h3>Not a fork!</h3>
                        <p>Void Linux is an independent distribution, developed entirely by volunteers.</p>
                        <p>Unlike trillions of other existing distros, Void is not a modification of an existing distribution.  Void's package manager and build system have been written from scratch.</p>
                </div>
                <div class="col-md-4">
                        <h3>Stable rolling release</h3>
                        <p>Void focuses on stability, rather than on being bleeding-edge. Install once, update routinely and safely.</p>
                        <p>Thanks to our <a href="https://build.voidlinux.org">continuous build system</a>, new software is built into binary packages as soon as the changes are pushed to the <em>void-packages</em> repository.</p>
                </div>
                <div class="col-md-4">
                        <h3>runit</h3>
                        <p>We use <a href="http://smarden.org/runit/">runit</a> as the init system and service supervisor.</p>
                        <p>runit is a simple and effective approach to initialize the system with reliable service supervision. Refer to the <a href="https://docs.voidlinux.org/config/services/index.html">Void Handbook</a> for an introduction.</p>
                </div>
        </div>
                <div class="row">
                        <div class="col-md-4">
                                <h3>C library diversity</h3>
                                <p>Void Linux supports both the <a href="http://musl.libc.org/">musl</a> and <a href="https://www.gnu.org/software/libc/">GNU</a> libc implementations, patching incompatible software when necessary and working with upstream developers to improve the correctness and portability of their projects.</p>
                        </div>
                <div class="col-md-4">
                        <h3>XBPS</h3>
                        <p><a href="https://github.com/void-linux/xbps">xbps</a> is the native system package manager, written from scratch with a <em>2-clause BSD</em> license.</p>
                        <p><em>XBPS</em> allows you to quickly install/update/remove software in your system and features detection of <em>incompatible shared libraries</em> and <em>dependencies</em> while updating or removing packages (among others). Refer to the Handbook for <a href="https://docs.voidlinux.org/xbps/index.html">an overview</a>.</p>
                </div>
                <div class="col-md-4">
                        <h3>xbps-src</h3>
                        <p><a href="https://github.com/void-linux/void-packages">xbps-src</a> is the xbps package builder, written from scratch with a <em>2-clause BSD</em> license.</p>
                        <p>This builds the software in <em>containers</em> through the use of <em>Linux namespaces</em>, providing isolation of processes and bind mounts (among others). No root required!</p>
                        <p>Additionally, xbps-src can build natively or cross compile for the target machine, and supports multiple <em>C libraries</em> (glibc and musl currently).</p>
                </div>
        </div>
        <hr>
        <div class="row">
                <div class="col-md-4">
                        <h3>void-packages changes <span class="rssdev"><a href="https://github.com/void-linux/void-packages/commits/master.atom" title="Subscribe to void-packages"><i class="fa fa-rss fa-lg"></i></a></span></h3>
                        <script src="/assets/js/voidcommits.js"></script>
                        <script src="https://api.github.com/repos/void-linux/void-packages/commits?page=1&amp;per_page=10&amp;callback=voidcommits&amp;sha=master"></script>
                </div>
                <div class="col-md-4">
                        <h3>void-packages pull requests</h3>
                        <script src="/assets/js/voidcommits.js"></script>
                        <script src="https://api.github.com/repos/void-linux/void-packages/pulls?page=1&amp;per_page=10&amp;callback=voidpulls&amp;sha=master"></script>
                </div>
                <div class="col-md-4">
                        <h3>xbps changes <span class="rssdev"><a href="https://github.com/void-linux/xbps/commits/master.atom" title="Subscribe to xbps"><i class="fa fa-rss fa-lg"></i></a></span></h3>
                        <script src="/assets/js/voidcommits.js"></script>
                        <script src="https://api.github.com/repos/void-linux/xbps/commits?page=1&amp;per_page=10&amp;callback=voidcommits&amp;sha=master"></script>
                </div>
        </div>
        <hr>
        <div class="page-header">
                <h2>Recent news <a href="/atom.xml" title="Subscribe to the news"><i class="fa fa-rss fa-lg"></i></a></h2>
        </div>
        <div class="row">

                        <div class="col-md-10">
                                <h4>March 10, 2026</h4>
                                <h3><a href="/news/2026/03/firmware-compression.html">Changes to linux-firmware may require manual intervention</a></h3>
                                <p>To reduce installation size, firmware provided by <code class="language-plaintext highlighter-rouge">linux-firmware</code> is now
compressed with zstd. Ensure you are running a supported kernel when updating to
<code class="language-plaintext highlighter-rouge">linux-firmware-20260309_1</code> or later:</p>

<ul>
  <li><code class="language-plaintext highlighter-rouge">linux5.10&gt;=5.10.251_1</code></li>
  <li><code class="language-plaintext highlighter-rouge">linux5.15&gt;=5.15.201_1</code></li>
  <li><code class="language-plaintext highlighter-rouge">linux6.1&gt;=6.1.127_1</code></li>
  <li><code class="language-plaintext highlighter-rouge">linux6.6&gt;=6.6.68_1</code></li>
  <li><code class="language-plaintext highlighter-rouge">linux6.12&gt;=6.12.7_1</code></li>
  <li><code class="language-plaintext highlighter-rouge">linux6.18</code>, <code class="language-plaintext highlighter-rouge">linux6.19</code>, or any later version</li>
  <li><code class="language-plaintext highlighter-rouge">rpi-kernel&gt;=6.12.67_1</code></li>
  <li><code class="language-plaintext highlighter-rouge">pinephone-kernel&gt;=6.1.7_2</code></li>
</ul>

<p>If you cannot run one of these kernels, you can hold the <code class="language-plaintext highlighter-rouge">linux-firmware</code> packages
at their currently-installed version:</p>

<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code># xbps-pkgdb -m hold linux-firmware linux-firmware-amd linux-firmware-broadcom \
    linux-firmware-intel linux-firmware-network linux-firmware-nvidia linux-firmware-qualcomm
</code></pre></div></div>

                        </div>

                        <div class="col-md-10">
                                <h4>June 14, 2025</h4>
                                <h3><a href="/news/2025/06/xbps-0.60.html">XBPS 0.60</a></h3>
                                <h2 id="whats-changed">What’s Changed</h2>

<ul>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix issues with updating packages in unpacked state. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: run all scripts before and after unpacking all packages,
to avoid running things in a half unpacked state. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix configuration parsing with missing trailing newline
and remove trailing spaces from values. <a href="https://github.com/eater">eater</a>, <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix XBPS_ARCH environment variable if architecture
is also defined in a configuration file. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix memory leaks. <a href="https://github.com/ArsenArsen">ArsenArsen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix file descriptor leaks. <a href="https://github.com/gt7-void">gt7-void</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix temporary redirect in libfetch. <a href="https://github.com/ericonr">ericonr</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix how the automatic/manual mode is set when replacing a
 package using replaces. This makes it possible to correctly replace
 manually installed packages using a transitional packages. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix inconsistent dependency resolution when a dependency
is on hold. xbps will now exit with <code class="language-plaintext highlighter-rouge">ENODEV</code> (19) if a held dependency
breaks the installation or update of a package instead of just ignoring
it, resulting in an inconsistent pkgdb. <a href="https://github.com/void-linux/xbps/pull/393">#393</a> <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix issues with <code class="language-plaintext highlighter-rouge">XBPS_FLAG_INSTALL_AUTO</code> where already installed
packages would get marked automatically installed when they are being
updated while installing new packages in automatically installed mode.
<a href="https://github.com/void-linux/xbps/pull/557">#557</a> <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: when reinstalling a package, don’t remove directories that are still
part of the new package. This avoids the recreation of directories which
trips up runsv, as it keeps an fd to the service directory open that would
be deleted and recreated. <a href="https://github.com/void-linux/xbps/pull/561">#561</a> <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-install(1)</code>: list reinstalled packages. <a href="https://github.com/chocimier">chocimier</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-install(1)</code>: in dry-run mode, ignore out of space error. <a href="https://github.com/chocimier">chocimier</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-install(1)</code>: fix bug where a repo-locked dependency could be updated
from a repository it was not locked to. <a href="https://github.com/chocimier">chocimier</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-fetch(1)</code>: make sure to exit with failure if a failure was encountered.
<a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-fetch(1)</code>: fix printing uninitialized memory in error cases. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-pkgdb(1)</code>: remove mtime checks, they are unreliable on fat filesystems
and xbps does not rely on mtime matching the package anymore. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-checkvers(1)</code>: with <code class="language-plaintext highlighter-rouge">--installed</code> also list subpackages. <a href="https://github.com/chocimier">chocimier</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-remove(1)</code>: fix dry-run cache cleaning inconsistencies. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-remove(1)</code>: allow removing “uninstalled” packages (packages in the cache
that are still up to date but no long installed) from the package
cache by specifying the <code class="language-plaintext highlighter-rouge">-O/--clean-cache</code> flag twice. <a href="https://github.com/void-linux/xbps/pull/530">#530</a> <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-query(1)</code>: <code class="language-plaintext highlighter-rouge">--cat</code> now works in either repo or pkgdb mode. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-query(1)</code>: <code class="language-plaintext highlighter-rouge">--list-repos/-L</code> list all repos including ones that
fail to open. <a href="https://github.com/chocimier">chocimier</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps.d(5)</code>: describe ignorepkg more precisely. <a href="https://github.com/chocimier">chocimier</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>, <code class="language-plaintext highlighter-rouge">xbps-install(1)</code>, <code class="language-plaintext highlighter-rouge">xbps-remove(1)</code>, <code class="language-plaintext highlighter-rouge">xbps-reconfigure(1)</code>,
<code class="language-plaintext highlighter-rouge">xbps-alternatives(1)</code>: add <code class="language-plaintext highlighter-rouge">XBPS_SYSLOG</code> environment variable to overwrite
syslog configuration option. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: Resolve performance issue caused by the growing number of virtual packages
in the Void Linux repository. <a href="https://github.com/void-linux/xbps/pull/625">#625</a> <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: Merge the staging data into the repository index (repodata) file.
This allows downloading the staging index from remote repositories without
having to keep the two index files in sync. <a href="https://github.com/void-linux/xbps/pull/575">#575</a> <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-install(1)</code>, <code class="language-plaintext highlighter-rouge">xbps-query(1)</code>, <code class="language-plaintext highlighter-rouge">xbps-checkvers(1)</code>, <code class="language-plaintext highlighter-rouge">xbps.d(5)</code>: Added <code class="language-plaintext highlighter-rouge">--staging</code> flag,
<code class="language-plaintext highlighter-rouge">XBPS_STAGING</code> environment variable and <code class="language-plaintext highlighter-rouge">staging=true|false</code> configuration option.
Enabling staging allows xbps to use staged packages from remote repositories.
<a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-install(1)</code>, <code class="language-plaintext highlighter-rouge">xbps-remove(1)</code>: Print package install and removal messages once,
below the transaction summary, before applying the transaction. <a href="https://github.com/void-linux/xbps/pull/572">#572</a> <a href="https://github.com/chocimier">chocimier</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-query(1)</code>: Improved argument parsing allows package arguments anywhere in the
arguments. <a href="https://github.com/void-linux/xbps/pull/588">#588</a> <a href="https://github.com/classabbyamp">classabbyamp</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-install(1)</code>: Make dry-run output consistent/machine parsable. <a href="https://github.com/void-linux/xbps/pull/611">#611</a> <a href="https://github.com/classabbyamp">classabbyamp</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: Do not url-escape tilde character in path for better compatibility with
some servers. <a href="https://github.com/void-linux/xbps/pull/607">#607</a> <a href="https://github.com/gmbeard">gmbeard</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: use the proper ASN1 signature type for packages. Signatures now have a <code class="language-plaintext highlighter-rouge">.sig2</code>
extension. <a href="https://github.com/void-linux/xbps/pull/565">#565</a> <a href="https://github.com/classabbyamp">classabbyamp</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-uhelper(1)</code>: add verbose output for <code class="language-plaintext highlighter-rouge">pkgmatch</code> and <code class="language-plaintext highlighter-rouge">cmpver</code> subcommands if the
<code class="language-plaintext highlighter-rouge">-v/--verbose</code> flag is specified. <a href="https://github.com/void-linux/xbps/pull/549">#549</a> <a href="https://github.com/classabbyamp">classabbyamp</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-uhelper(1)</code>: support multiple arguments for many subcommands to improve pipelined
performance. <a href="https://github.com/void-linux/xbps/pull/536">#536</a> <a href="https://github.com/classabbyamp">classabbyamp</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-alternatives(1)</code>: Add <code class="language-plaintext highlighter-rouge">-R/--repository</code> mode to <code class="language-plaintext highlighter-rouge">-l/--list</code> to show alternatives
of packages in the repository. <a href="https://github.com/void-linux/xbps/pull/340">#340</a> <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: fix permanent (308) redirects when fetching packages and repositories. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-remove(1)</code>: ignores file not found errors for files it deletes. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">libxbps</code>: the <code class="language-plaintext highlighter-rouge">preserve</code> package metadata is now also respected for package removals. <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
  <li>
    <p><code class="language-plaintext highlighter-rouge">xbps-pkgdb(1)</code>: new <code class="language-plaintext highlighter-rouge">--checks</code> allows to choose which checks are run. <a href="https://github.com/void-linux/xbps/pull/352">#352</a> <a href="https://github.com/ericonr">ericonr</a>, <a href="https://github.com/duncaen">duncaen</a></p>
  </li>
</ul>

<p><strong>Full Changelog</strong>: <a href="https://github.com/void-linux/xbps/compare/0.59.2...0.60">https://github.com/void-linux/xbps/compare/0.59.2...0.60</a></p>

                        </div>

        </div>
</div>


                        <div class="container col-md-8 col-md-offset-2">
                                <hr>
                                <footer class="footer">
                                        <p class="text-center">Copyright 2026 <a href="https://github.com/orgs/void-linux/people">VoidLinux contributors</a></p>
                                        <p class="text-center">Copyright 2008-2018 <a href="https://gitlab.com/xtraeme">Juan RP</a> and contributors</p>
                                        <p class="text-center">Linux&#174; is a registered trademark of Linus Torvalds (<a href="https://www.linuxfoundation.org/programs/legal/trademark/attribution">info</a>)</p>
                                </footer>
                        </div>
                </div>
        </body>
</html>
* Connection #0 to host voidlinux.org left intact
```

---

### A.2. Запит без захисту з'єднання

**Команда:**

```
curl -v http://voidlinux.org
```

**Вивід:**

```
* Host voidlinux.org:80 was resolved.
* IPv6: (none)
* IPv4: 185.199.109.153
*   Trying 185.199.109.153:80...
* Connected to voidlinux.org (185.199.109.153) port 80
* using HTTP/1.x
> GET / HTTP/1.1
> Host: voidlinux.org
> User-Agent: curl/8.13.0
> Accept: */*
>
* Request completely sent off
< HTTP/1.1 301 Moved Permanently
< Connection: keep-alive
< Content-Length: 162
< Server: GitHub.com
< Content-Type: text/html
< Location: https://voidlinux.org/
< X-GitHub-Request-Id: 5446:215CED:35BED26:364BE65:6AA66418
< x-github-edge-region: fra
< Accept-Ranges: bytes
< Date: Sun, 13 Sep 2026 08:59:39 GMT
< Via: 1.1 varnish
< Age: 483
< X-Served-By: cache-fra-eddf8230191-FRA
< X-Cache: HIT
< X-Cache-Hits: 1
< X-Timer: S1789289980.953465,VS0,VE2
< Vary: Accept-Encoding
< X-Fastly-Request-ID: 7d1a697adf063af44935e3c9291d05f37540d551
<
<html>
<head><title>301 Moved Permanently</title></head>
<body>
<center><h1>301 Moved Permanently</h1></center>
<hr><center>nginx</center>
</body>
</html>
* Connection #0 to host voidlinux.org left intact
```

---

### A.3. Запит до служби доменних імен

*Windows: `Resolve-DnsName ВАШ_ДОМЕН`*

**Команда (перше виконання):**

```
Resolve-DnsName voidlinux.org
```

**Вивід:**

```
Name                                           Type   TTL   Section    IPAddress
----                                           ----   ---   -------    ---------
voidlinux.org                                  AAAA   642   Answer     2606:50c0:8000::153
voidlinux.org                                  A      241   Answer     185.199.109.153
```

**Команда (повторне виконання через 5–7 хвилин):**

```
Resolve-DnsName voidlinux.org
```

**Вивід:**

```
Name                                           Type   TTL   Section    IPAddress
----                                           ----   ---   -------    ---------
voidlinux.org                                  AAAA   151   Answer     2606:50c0:8000::153
voidlinux.org                                  A      1527  Answer     185.199.109.153
```

**Зафіксовані значення:**

| Параметр | Перше виконання | Повторне виконання |
|---|---|---|
| Час виконання (год:хв) | 12:25 | 12:33 |
| IP-адреса | 2606:50c0:8000::153, 185.199.109.153 | 2606:50c0:8000::153, 185.199.109.153 |
| Значення TTL | 642, 241 | 151, 1527 |

> Якщо друге значення TTL виявилося більшим за перше — це нормально: кеш резолвера встиг оновитися. Зафіксуйте як є.

---

### A.4. Контрольний ресурс

**Команда:**

```
curl -v https://google.com
```

**Вивід:**

```
* Host google.com:443 was resolved.
* IPv6: (none)
* IPv4: 142.251.140.78
*   Trying 142.251.140.78:443...
* schannel: disabled automatic use of client certificate
* ALPN: curl offers http/1.1
* ALPN: server accepted http/1.1
* Connected to google.com (142.251.140.78) port 443
* using HTTP/1.x
> GET / HTTP/1.1
> Host: google.com
> User-Agent: curl/8.13.0
> Accept: */*
>
* Request completely sent off
< HTTP/1.1 301 Moved Permanently
< Location: https://www.google.com/
< Content-Type: text/html; charset=UTF-8
< Content-Security-Policy-Report-Only: object-src 'none';base-uri 'self';script-src 'nonce-ANGlENVPyzGFUDTNwvHdsA' 'strict-dynamic' 'report-sample' 'unsafe-eval' 'unsafe-inline' https: http:;report-uri https://csp.withgoogle.com/csp/gws/other-hp
< Date: Sun, 13 Sep 2026 09:37:17 GMT
< Expires: Tue, 13 Oct 2026 09:37:17 GMT
< Cache-Control: public, max-age=2592000
< Server: gws
< Content-Length: 220
< X-XSS-Protection: 0
< X-Frame-Options: SAMEORIGIN
< Alt-Svc: h3=":443"; ma=2592000,h3-29=":443"; ma=2592000
<
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="https://www.google.com/">here</A>.
</BODY></HTML>
* Connection #0 to host google.com left intact
```

---

### A.5. Ресурси з некоректною конфігурацією сертифіката

**Випадок 1**

```
curl -v https://expired.badssl.com
```

```
* Host expired.badssl.com:443 was resolved.
* IPv6: (none)
* IPv4: 104.154.89.105
*   Trying 104.154.89.105:443...
* schannel: disabled automatic use of client certificate
* ALPN: curl offers http/1.1
* schannel: next InitializeSecurityContext failed: SEC_E_CERT_EXPIRED (0x80090328) - Получен сертификат с истекшим сроком действия.
* closing connection #0
curl: (35) schannel: next InitializeSecurityContext failed: SEC_E_CERT_EXPIRED (0x80090328) - Получен сертификат с истекшим сроком действия.
```

**Випадок 2**

```
curl -v https://wrong.host.badssl.com
```

```
* Host wrong.host.badssl.com:443 was resolved.
* IPv6: (none)
* IPv4: 104.154.89.105
*   Trying 104.154.89.105:443...
* schannel: disabled automatic use of client certificate
* ALPN: curl offers http/1.1
* schannel: SNI or certificate check failed: SEC_E_WRONG_PRINCIPAL (0x80090322) - Главное конечное имя неверно.
* closing connection #0
curl: (60) schannel: SNI or certificate check failed: SEC_E_WRONG_PRINCIPAL (0x80090322) - Главное конечное имя неверно.
More details here: https://curl.se/docs/sslcerts.html

curl failed to verify the legitimacy of the server and therefore could not
establish a secure connection to it. To learn more about this situation and
how to fix it, please visit the webpage mentioned above.
```

**Випадок 3**

```
curl -v https://self-signed.badssl.com
```

```
* Host self-signed.badssl.com:443 was resolved.
* IPv6: (none)
* IPv4: 104.154.89.105
*   Trying 104.154.89.105:443...
* schannel: disabled automatic use of client certificate
* ALPN: curl offers http/1.1
* schannel: SEC_E_UNTRUSTED_ROOT (0x80090325) - Цепочка сертификатов выпущена центром сертификации, не имеющим доверия.
* closing connection #0
curl: (60) schannel: SEC_E_UNTRUSTED_ROOT (0x80090325) - Цепочка сертификатов выпущена центром сертификации, не имеющим доверия.
More details here: https://curl.se/docs/sslcerts.html

curl failed to verify the legitimacy of the server and therefore could not
establish a secure connection to it. To learn more about this situation and
how to fix it, please visit the webpage mentioned above.
```

> Якщо використано альтернативний спосіб із параметром `--resolve` — зазначити це та навести фактичну команду.

---

## Частина B. Власна модель рівнів

**Кількість виділених груп:** ___

| № | Назва групи (власне формулювання) | Рядки виводу, віднесені до групи | Обґрунтування |
|---|---|---|---|
| 1 | Запити на протокол підключення | curl -v https://voidlinux.org<br>curl -v http://voidlinux.org | Виконання запитів до вебсайту з використанням різних протоколів — HTTP та HTTPS. Отримання детальної інформації про встановлення з'єднання, запит клієнта та відповідь сервера. При використанні HTTPS отримано повний доступ до HTML-вмісту вебсторінки, тоді як HTTP-запит отримав відповідь із перенаправленням на захищене HTTPS-з'єднання. |
| 2 | Запити діагностики | Resolve-DnsName voidlinux.org<br>curl -v https://google.com | Виконання діагностичних запитів для отримання інформації про домен, його IP-адреси, типи DNS-записів та параметри їх актуальності (TTL), а також перевірки встановлення HTTPS-з'єднання із контрольним ресурсом Google. |
| 3 | Запити до доменів із проблемними сертифікатами | curl -v https://expired.badssl.com<br>curl -v https://wrong.host.badssl.com<br>curl -v https://self-signed.badssl.com | Виконання запитів до ресурсів із навмисно некоректною конфігурацією TLS-сертифікатів. У всіх трьох випадках захищене з'єднання не було встановлено через проблеми із сертифікатом: закінчення строку його дії, невідповідність доменного імені або відсутність довіри до центру сертифікації. Такі помилки можуть створювати серйозні ризики для безпеки HTTPS-з'єднання. |

*Групи впорядковано від найближчої до користувача (№ 1) до найближчої до апаратного забезпечення. Зайві рядки вилучити, за потреби — додати.*

**Рядки, які не вдалося віднести до жодної групи:**

| Рядок виводу | Причина утруднення |
|---|---|
| | |
| | |
| | |

---

## Контрольні питання

**1. Скільки рядків діагностичного виводу передує отриманню даних сторінки (завдання A.1)?**

> 39 рядків діагностичного виводу (до частини html коду)

**2. Які рядки наявні у виводі A.1 і відсутні у виводі A.2? Чим це зумовлено?**

> * schannel: disabled automatic use of client certificate
* ALPN: curl offers http/1.1
* ALPN: server accepted http/1.1

< Last-Modified: Tue, 10 Mar 2026 22:49:51 GMT
< Access-Control-Allow-Origin: *
< Strict-Transport-Security: max-age=31557600
< ETag: "69b0a00f-5a9f"
< expires: Mon, 07 Sep 2026 11:46:23 GMT
< Cache-Control: max-age=600
< x-proxy-cache: MISS
+ відсутні рядки з тегу <body> док-та html - близько трьоїста рядків коду.

**3. Звідки у виводі з'явилося значення `443`, якщо його не було вказано в адресі?**

> Location: https://voidlinux.org/ - сервер пропонує більш захищений протокол з'єднання за допомогою порту 443.

**4. Як змінилося значення TTL між двома запитами (A.3)? Що означає це число?**

> Значення TTL | 642, 241 | 151, 1527 -> беручи друге число з кожної пари (АААА), TTL збільшився, що може говорити про те що кеш	встиг оновитися.

**5. Чим відрізняються між собою три причини помилок із завдання A.5? Сформулювати кожну однією фразою.**

| Випадок | Причина недовіри |
|---|---|
| `expired` | термін дії сертифікати вичерпано |
| `wrong.host` | сертифікат не відповідає домену, взятий з іншого домену |
| `self-signed` | сертифікат не підтверджений центром перевірки |

**6. Три рядки з власних виводів, про які не йшлося на лекції 1:**

| № | Рядок виводу | Джерело (номер завдання) |
|---|---|---|
| 1 | * schannel: disabled automatic use of client certificate | А1 |
| 2 | * ALPN: curl offers http/1.1 | А1 |
| 3 | * ALPN: server accepted http/1.1 | А1 |

*Пояснення до цих рядків не потрібне.*

---

## Висновки

*150–300 слів. Спиратися на власні спостереження, а не на матеріал лекції.*

**D.1. Що виявилося неочевидним або несподіваним**

*Назвати конкретно, з посиланням на рядок виводу.*

> У пункті А3 на початку зіткнувся з тим, що команда Resolve-DnsName <ДОМЕН> не розпізнавалась в середовищі cmd. Після кількох невдалих спроб та звернувшись за допомогою до Його Величності Google, дізнався що перевіряти треба у Windows PowerShell. Отримавши output, спочатку не міг зрозуміти чому наче для одного домена виводить 2 ip та 2 TTL. Перевіривши, дійшов висновку що це 2 способи ip-адресаціх в Інтернеті - IP-v4 та IP-v6 для А та АААА відповідно.

**D.2. Чому саме така кількість груп у частині B**

*На якій підставі ухвалено рішення. Що змусило б його змінити.*

> По-перше, сама кількість блоків у завданні (А1 - А5) невелика, тож я не бачив сенсу розділяти їх на велику кількість груп. Щодо класифікації, яку я обрав: все з власного досвіду. Опрацювавши команди А1 - А2 в мене виникло розуміння, що це способи за різними портами з'єднатися до одного й того ж інтернет-ресурсу, тож і назвав відповідно: "Запити на протокол підключення".

Далі в більш поглибленому середовищі Windows PowerShell провів діагностику домену voidlinux.org, дізнавшись його IP та TTL у різних версіях адресації. Звертання до https://google.com теж вирішив віднести у цю категорію, бо в output можна побачити усі стати з'єднання, що є еталоном нормальної роботи браузера.

Третя категорія - команди з поверненням помилок. Блок був про те, які помилки та при яких ситуаціях можуть виникати у разі проблем з сертифікатом. Тож тут все просто.

**D.3. Питання, яке залишилося без відповіді**

> Уявімо що вебсайт в режимі реального часу стежить за тим, скільки людей зараз його відвідують. У разі успішного з'єднання через команду curl, чи буде це рахуватися ніби юзер на сайті?

---

## Використання штучного інтелекту

*Розділ обов'язковий. Заповнюється незалежно від того, чи використовувався ШІ. Детальні вимоги — у документі «Політика використання технологій штучного інтелекту».*

**Факт використання:** використано

**Установлений рівень для цієї роботи:** Р3 — ШІ як співвиконавець

**Фактичний рівень використання:** Р3

### Використані системи

| Система | Версія або модель | Період використання |
|---|---|---|
| GPT OpenAI | GPT-5.6 | 13.09.26 |

### Промпти

*Наводити дослівно, у тому вигляді, у якому запит було надано системі. Переказ не приймається.*

| № | Розділ роботи | Текст промпта |
|---|---|---|
| 1 | A3 | Мне гововрили, чтотип если через время TTL меняется - єто нормально, что типо кеш очищается. Но не совсем понятно. кеш чего? И почему у меня дважды в обоих случаях вывело сайт? какой IP за что отвечает, и почему в первом 4А, а во втором А просто |
| 2 | A5 | 1) curl -v https://expired.badssl.com - Получен сертификат с истекшим сроком действия<br>2) curl -v https://wrong.host.badssl.com - Главное конечное имя неверно.<br>3) curl -v https://self-signed.badssl.com - Цепочка сертификатов выпущена центром сертификации, не имеющим доверия.<br>Обьясни, почему именно такие результаты вышли для каждой из трёх команд |

### Дії з отриманим результатом

| № промпта | Що перевірено | Що змінено | Що відхилено і чому |
|---|---|---|---|
| 1 | А3 - Dns діагностика | - | - |
| 2 | А5 - output команд з блоку А5 | - | - |

### Підтвердження

Підтверджую, що всі наведені в цьому звіті виводи команд отримано мною особисто внаслідок фактичного виконання відповідних дій, а відомості цього розділу є повними та достовірними.

> Виводи `curl`, `dig` та інші артефакти не можуть бути згенеровані. Це стосується будь-якого рівня використання ШІ.

---

## Примітки виконавця

*(необов'язковий розділ: що не спрацювало, які команди довелося змінити, які виникли труднощі)*

> часу на виконання даної роботи пішло значно більше ніж очікував. Але думаю справа банально в новому оформлені роботи, з чим раніше ще не стикався.