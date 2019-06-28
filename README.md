Ansible Role for Gitea - a Sourcecode Management Server
=======================================================

This Ansible role can be used to **install** and keep your Gitea server **up to date**.
Gitea is a Git server with a great web interface such as GitHub.
Please take a look at the official [Gitea Site](https://gitea.io/) for more information on Gitea.

## Host Vars

```yaml
# Systemd service user
gitea_user: gitea
gitea_version: 1.8.3
gitea_directory: /var/lib/gitea
gitea_disable_ssh: 'false'
gitea_domain: git.example.net
gitea_root_url: 'https://git.example.net/'
gitea_ssh_domain: git.example.net
gitea_ssh_port: 22
gitea_http_port: 3000
gitea_mailer_host: 'mailserver.example.net:587'
gitea_mailer_from: '"Gitea" <gitea@example.net>'
gitea_mailer_user: ''
gitea_mailer_passwd: ''
gitea_mailer_skip_ssl_verify: 'true'
gitea_disable_registration: 'true'
gitea_no_reply_address: noreply.example.net
# memory , redis or memcache
gitea_cache_adapter: memory
# cache interval in seconds (only for memory adapter)
gitea_cache_interval: 60
# gitea_cache_host examples (multiple backends separated by ";")
# Redis: network=tcp,addr=127.0.0.1:6379,password=macaron,db=0,pool_size=100,idle_timeout=180
# Memache: 127.0.0.1:9090;127.0.0.1:9091
gitea_cache_host: ''
# garbage collection interval in seconds (default: 1 day)
gitea_gc_interval_time: 86400
```

## Updating Gitea

This Ansible role automatically compares the installed version with the version set by ```gitea_version``` and upgrades if ```gitea_version``` is higher than the currently installed one.

## License

>Copyright <YEAR> <COPYRIGHT HOLDER>
>
>Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
>
>1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
>2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
>3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
>
>THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
