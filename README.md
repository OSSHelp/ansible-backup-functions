# Backup-functions

[![Build Status](https://drone.osshelp.io/api/badges/ansible/backup-functions/status.svg)](https://drone.osshelp.io/ansible/backup-functions)

The role which installs [backup-functions](https://github.com/OSSHelp/backup-functions) and backup scripts. Make sure to install [pushgateway-functions](https://gitea.osshelp.io/ansible/pushgateway-functions) for metrics export. For cronjobs you need to use [cron role](https://github.com/OSSHelp/ansible-cron).

## Deploy example

```yaml
  roles:
    - role: backup-functions
      backup_functions_version: 2-latest
```

Where 1-latest is backup-functions version 3.x.x and 2-latest is version 4.x.x.

## Available parameters

### Main

| Param | Default | Description |
| -------- | -------- | -------- |
| `backup_functions_version` | `2-latest` | Version to install. You need to select a release the tag, not the library version itself. For example, `1.1.3` here will result in library v3.26.1 installlation. |
| `backup_dir` | `/backup` | Directory for backup saving |
| `create_backup_dir` | `true` | Create backup directory |
| `add_template` | `false` | Download custom.backup template |
| `install_pbzip2` | `true` | Install pbzip2|
| `install_backup_scripts` | `true` | Copy scripts from `scr_script_location` |
| `src_script_location` | `files/backup/` | Directory with your backup scripts |

## FAQ

None

## Useful links

- [Official documentation](https://github.com/OSSHelp/backup-functions)
- [Ansible role for cron configuration](https://github.com/OSSHelp/ansible-cron)
- [Ansible role for pushgateway-functions installation](https://gitea.osshelp.io/ansible/pushgateway-functions)

## TODO

None, so far.

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
