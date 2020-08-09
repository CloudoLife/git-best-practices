The best practices for Git.

# Git Best Practices

## Ignore Files

Use allowlist and denylist to ignore files.
```bash
# cat .gitignore

# First, Denylist ignore everything
*

# Now, Allowlist allow anything that's a directory, but not a file.
!*/

# Allowlist the file or folder
# !NotIgnoredFile
# !NotIgnoredFolder/

# Recursively allowlist its contents
# !NotIgnoredFolder/**

!docker/**
!docker-compose/**

!.dockerignore
!.gitignore

!README.md
```

## Configuration

Specify git configuration for project.
```bash
# Specify SSH private key.
git config core.sshCommand "ssh -i ~/.ssh/<Your SSH private key> -F /dev/null"

# Specify email and name.
git config user.email "<Your email>" && git config user.name "<Your Name>"
```