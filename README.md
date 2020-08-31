我是光年实验室高级招聘经理。
我在github上访问了你的开源项目，你的代码超赞。你最近有没有在看工作机会，我们在招软件开发工程师，拉钩和BOSS等招聘网站也发布了相关岗位，有公司和职位的详细信息。
我们公司在杭州，业务主要做流量增长，是很多大型互联网公司的流量顾问。公司弹性工作制，福利齐全，发展潜力大，良好的办公环境和学习氛围。
公司官网是http://www.gnlab.com,公司地址是杭州市西湖区古墩路紫金广场B座，若你感兴趣，欢迎与我联系，
电话是0571-88839161，手机号：18668131388，微信号：echo 'bGhsaGxoMTEyNAo='|base64 -D ,静待佳音。如有打扰，还请见谅，祝生活愉快工作顺利。

# sshcode

[!["Open Issues"](https://img.shields.io/github/issues-raw/codercom/sshcode.svg)](https://github.com/codercom/sshcode/issues)
[!["Latest Release"](https://img.shields.io/github/release/codercom/sshcode.svg)](https://github.com/codercom/sshcode/releases/latest)
[![MIT license](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/codercom/sshcode/blob/master/LICENSE)
[![Discord](https://img.shields.io/discord/463752820026376202.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/zxSwN8Z)

`sshcode` is a CLI to automatically install and run [code-server](https://github.com/codercom/code-server) over SSH.

It uploads your extensions and settings automatically, so you can seamlessly use
remote servers as VS Code hosts.

If you have Chrome installed, it opens the browser in app mode. That means
there's no keybind conflicts, address bar, or indication that you're coding within a browser.
**It feels just like native VS Code.**

![Demo](/demo.gif)

## Install

Chrome is recommended.

Install with `go`:

```bash
go get go.coder.com/sshcode
```

Or, grab a [pre-built binary](https://github.com/codercom/sshcode/releases).

## Usage

```bash
sshcode kyle@dev.kwc.io
# Starts code-server on dev.kwc.io and opens in a new browser window.
```

You can specify a remote directory as the second argument:

```bash
sshcode kyle@dev.kwc.io ~/projects/sourcegraph
```

## Extensions & Settings Sync

By default, `sshcode` will `rsync` your local VS Code settings and extensions
to the remote server every time you connect.

This operation may take a while on a slow connections, but will be fast
on follow-up connections to the same server.

To disable this feature entirely, pass the `--skipsync` flag.

### Sync-back

By default, VS Code changes on the remote server won't be synced back
when the connection closes. To synchronize back to local when the connection ends,
pass the `-b` flag.
