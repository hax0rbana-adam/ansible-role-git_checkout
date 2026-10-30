A simple role to check out a particular git repo, into a specific directory, as
the specified user, with the specified ownership and group.

# Variables

See defaults/main.yml for the variables and an explanation as to what they do.

# Examples
## Playbook
Here's an example of a playbook to check out the linux repo, as the user linus,
and put it in ~/git/linux.

```yaml
- hosts: all
  remote_user: root
  vars:
    git_checkout_user: linus
  roles:
    - role: hax0rbana_adam.git_checkout
```

If there wasn't a `linus` user before, this role will create it.

If ~/git didn't exist, it will be created and be owned by linus:linus with a mode of 700.

# Official repo location
All activity takes place on the official GitLab instance:
[https://gitlab.hax0rbana.org/public-repos/ansible/ansible-role-git_checkout](https://gitlab.hax0rbana.org/public-repos/ansible/ansible-role-git_checkout)

Any other hosting providers, such as GitHub.com and GitLab.com, are just mirrors
and we do not monitor the issue trackers over there.

# Support
## Matrix channel
You can also join our Matrix channel: #ansible:hax0rbana.org

This is a good place to ask questions or make requests without having to sign
up for another account.

# Contributing
See [contributor guidelines](CONTRIBUTING.md).

# License
This project is licensed under MIT License. See [LICENSE](LICENSE) for more details.
