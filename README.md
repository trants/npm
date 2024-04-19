# Nginx Proxy Manager

This repository provides a base on [`nginx-proxy-manager`](https://nginxproxymanager.com/), that enables you to easily
forward to your websites running at home or otherwise, including free SSL, without having to know too much about Nginx
or Letsencrypt.

### 📦 Requirements

The Docker & Docker Compose system requirements are Linux Ubuntu as the OS (other operating systems are supported as
well), an absolute minimum 512MB RAM (2GB recommended)

In order to install docker Ubuntu, you will need to meet the following requirements:

- OS: Linux Ubuntu
- Memory: 512MB RAM (2GB Recommended)
- Disk: Sufficient amount to run the Docker containers you wish to use
- CPU: Dependent on the applications you wish to run in the containers

### 📋 Features

- Beautiful and Secure Admin Interface based on [`Tabler`](https://tabler.io/)
- Easily create forwarding domains, redirections, streams and 404 hosts without knowing anything about Nginx
- Free SSL using Let's Encrypt or provide your own custom SSL certificates
- Access Lists and basic HTTP Authentication for your hosts
- Advanced Nginx configuration available for super users
- User management, permissions and audit log

### 🔧 Installation

1. Install Docker and Docker-Compose

- [Docker Install documentation](https://docs.docker.com/install/)
- [Docker-Compose Install documentation](https://docs.docker.com/compose/install/)

2. Bring up your stack by running

```shell
git clone https://github.com/trants/npm.git \
    && cd npm \
    && cp .env.example .env
```

3. Edit environment variable

```dotenv
# NPM
DB_MYSQL_HOST=npm-db
DB_MYSQL_PORT=3306
DB_MYSQL_USER=npm
DB_MYSQL_NAME=npm-production
DB_MYSQL_PASSWORD=npmPassword

# DB
MYSQL_USER=npm
MYSQL_DATABASE=npm-production
MYSQL_PASSWORD=npmPassword
MYSQL_ROOT_PASSWORD=npmRootPassword

# Backup
TZ=UTC
SCHEDULE=@weekly
BACKUP_KEEP_DAYS=7
PASSPHRASE=platonic-subdued-curvy-tweet-backroom
S3_BUCKET=my-s3-bucket
S3_REGION=us-east-1
S3_PREFIX=prefix
S3_ACCESS_KEY_ID=
S3_SECRET_ACCESS_KEY=
MYSQL_HOST=mysql
```

4. Start NPM

```shell
docker-compose up -d
```

### 📝 Usage

Reader-friendly documentation can be found [here][link-docs].

### 📨 Message

I hope you find this useful. If you have any questions, please create an issue.

### 🔐 Security

If you discover any security related issues, please email opensource@vspc.vn instead of using the issue tracker.

### 📖 License

This software is released under the [BSD 3-Clause][link-license] License. Please see the [LICENSE](LICENSE) file
or https://vspc.vn/license for more information.

### ✨ Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <td align="center" valign="top" width="14.28%">
    <a href="https://trants.me">
      <img src="https://avatars.githubusercontent.com/u/5866677?v=4?s=100" width="100px;" alt="Son Tran Thanh" />
      <br />
      <sub>
        <b>Son Tran Thanh</b>
      </sub>
    </a>
    <br />
    <a href="https://github.com/trants/npm/commits?author=trants" title="Code">💻</a>
    <a href="https://github.com/trants/npm/commits?author=trants" title="Documentation">📝</a>
  </td>
</table>
<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://allcontributors.org) specification.
Contributions of any kind welcome!

[link-docs]: https://nginxproxymanager.com
[link-license]: https://opensource.org/license/bsd-3-clause
