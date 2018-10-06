# TFE_WorkspaceBackup
This tool provides the ability to backup terraform enterprise workspaces.
It will use the TFE Rest API and collect data about your workspaces, then using templates, will create proper terraform configurations to allow you to rebuild the workspaces.


## Usage

### Backup All Workspaces in Organization:
The following command will:
- backup all workspaces in an organization
- format the configuration files correctly
- validate the configuration files
- perform init to to update the providers
```bash
tfe-backup -o <tfe_organization_name> -b <base_directory> --fmt --init --validate
```

### Backup Single Workspace in Organization:
The following command will:
- backup a single in an organization
- format the configuration files correctly
- validate the configuration files
- perform init to to update the providers
```bash
tfe-backup -o <tfe_organization_name> -w <workspace_name> -b <base_directory> --fmt --init --validate
```

### Clone Single Workspace in Organization:
The following command will:
- backup a single in an organization
- set name of workspace in configuration to new workspace name
- write out configuration for new workspace into a properly named configuration file
- format the configuration files correctly
- validate the configuration files
- perform init to to update the providers
```bash
tfe-backup -o <tfe_organization_name> -w <workspace_name> --new-ws <new_workspace_name -b <base_directory> --fmt --init --validate
```
