[![Build Status](https://travis-ci.com/marcomc/ansible-role-splinter-toolkit.svg?branch=master)](https://travis-ci.com/marcomc/ansible-role-splinter-toolkit)

# ansible-role-splinter-toolkit
Provides foundamenta Ansible tasks for the [Splinter provisioning tool for macOS](https://github.com/marcomc/splinter).

Provides:
- Change profile picture for the current user
- Toggle App Quarantine on/off
- GNUTar installation and addition to $PATH
- Toggle passwordless SUDO on/off
- Restore preferences with Macpres

# Usage
    vars:
      install_macos_apps: yes  # will allow GNUTar installation
      current_user_profile_picture: "/path/to/picture"
      passwordless_sudo: yes
      restore_preferences_and_dotfiles_from_export: yes

    roles:
      - role: marcomc.splinter_toolkit

    tasks:
      - name: Load the Splinter post provision tasks.
        include_role:
          name: marcomc.splinter_toolkit
          tasks_from: post-provision


# Requirements

## Soft Requirements

    marcomc.macos_new_user
    marcomc.macos_macprefs

## Variables

# License & Copyright

License: [GPLv2](LICENSE.md)

2020 (c) Marco Massari Calderone <marco@marcomc.com>
