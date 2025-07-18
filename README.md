# Baseline

Configure Sigaint SOE for FreeBSD and Linux (Red Hat Enterprise Linux)

```
git clone https://github.com/mhahl/freebsd-baseline.git 
cd freebsd-baseline
bash bootstrap.sh
```

## Installation

Run the `bootstrap.sh` script and enter the vault password.

```bash
../bootstrap.sh
Vault Password: xxxxxxxxx
```

The system will install the necessary packages and configure the system. Check MOONLIGHT to see if the system has
checked in and is working correctly.

## Configuration
You can update the `/usr/local/etc/baseline.yaml` with the following toggles, the default for each setting is `True`

* `configure_dns` - Configure the DNS settings in `dns_servers` and `dns_search`
* `configure_motd` - Print a pretty dinosaur.
* `configure_skel` - Copy the `skel` directory to new users.
* `configure_sssd` - Configure the `sssd.conf` file for ldap authentication.
* `configure_sshd` - Configure the system to allow access only from (TODO: mhahl) `hbac_allow_groups`
* `configure_sudo` - Configure the system to allow access only from (TODO: mhahl) `hbac_sudo_commands`
* `configure_baseline` - Deploy a cronjob and ansible-pull to keep the system configured.

More options are available by looking at `baseline.yaml`