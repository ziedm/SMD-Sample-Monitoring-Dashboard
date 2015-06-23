# Sample-Monitor-Dash

[![Linux Dash Gitter chat](https://badges.gitter.im/gitterHQ/gitter.png)](https://github.com/ziedm/Sample-Monitor-Dash.git)

A simple, low-overhead web dashboard for GNU / Linux. (~1MB)

[**Installation Instructions**](#installation) | [**Support**](#support)



## Features
* A beautiful, simple web-based dashboard for monitoring a linux server
* Only ~1MB on disk! *(.git removed)*
* Live graphs, refresh-able widgets, and a growing # of supported modules
* Drop-in installation for PHP, Node.js, Python, and Go 

## Installation

### 1. Download Sample-Monitor-Dash

Clone the git repo: 
```shell
git clone https://github.com/ziedm/Sample-Monitor-Dash.git
```
*Alternatives*: 
- Install the [Composer] package
```bash
composer create-project ziedm/Sample-Monitor-Dash -s dev
```
- Download the source at: https://github.com/ziedm/Sample-Monitor-Dash/archive/master.zip

### 2. Secure Sample-Monitor-Dash
*It is strongly recommended that all Sample-Monitor-Dash installations be password protected. Please add htaccess protection or another security measure of your choice.*


### 3. Start Sample-Monitor-Dash
See the section for your platform. 

#### PHP
1. Make sure you have the `exec`, `shell_exec`, and `escapeshellarg` functions enabled
2. Restart your web server (Apache, nginx, etc.) 
  - For PHP + Apache setup follow the [Digital Ocean tutorial](https://www.digitalocean.com/community/tutorials/how-to-install-linux-dash-on-ubuntu-14-04).
  - For help with nginx setup, see [this gist](https://gist.github.com/sergeifilippov/8909839) by [@sergeifilippov](https://github.com/sergeifilippov).

#### Node.js
Install NPM dependencies
```
npm install
```
Start Sample-Monitor-Dash
```
node server
```
  - Default port is 80. You may change this in [server/index.js on line 8](https://github.com/ziedm/Sample-Monitor-Dash/blob/master/server/index.js#L8)

#### Go
Go to the `Sample-Monitor-Dash/server` folder and run 
```
go run index.go
```

To build a binary, run `go build && ./server -h`. See [@tehbilly](https://github.com/sergeifilippov)'s notes [here](https://github.com/ziedm/NetMon-Dash/pull/281) for binary usage options

## Goals for v2.0
- [x] Backend ported to ~~Python~~ shell scripts & python from PHP
- [x] Add config file
- [x] Segregate core code-base and modules
- [ ] ~~Each module in a separate directory with front-end template, back-end file, bash script~~
- [ ] Add angular element to show info section for a module
- [ ] Angular tests
- [ ] Back-end tests
  - [ ] for shell files
  - [ ] for PHP, NodeJS, & Go
- [ ] "Quick Guide to Contributing" Wiki page
- Add project to package managers
  - [x] npm
  - [x] composer
  - [ ] aur
  - [ ] apt
- [x] Bonus: 
  - [x] multiple server side languages supported
  - [ ] use websockets in PHP & NodeJS

## Support

For help with general setup and configuration issues please use the [Linux Dash Gitter](https://github.com/ziedm/Sample-Monitor-Dash.git).

The following categories are targeted by the NetMon Dash project:
* OS
 * Arch
 * Debian 6,7
 * Ubuntu 11.04+
 * Linux Mint 16+
 * CentOS 5, 6
* Backend
 * Node.js
 * Go
 * PHP 5
