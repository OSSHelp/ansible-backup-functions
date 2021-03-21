# Backup-functions

[![Build Status](https://drone.osshelp.ru/api/badges/ansible/backup-functions/status.svg)](https://drone.osshelp.ru/ansible/backup-functions)

The role which installs [backup-functions](https://github.com/OSSHelp/backup-functions) and backup scripts. For cronjobs you need to use [cron role](https://github.com/OSSHelp/ansible-cron).

## Deploy example

```yaml
  roles:
    - role: backup-functions
```

## Available parameters

### Main

| Param | Default | Description |
| -------- | -------- | -------- |
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
- [Ansible role for cron](https://github.com/OSSHelp/ansible-cron)

## TODO

None, so far.

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
