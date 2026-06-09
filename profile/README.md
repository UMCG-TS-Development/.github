# Overview

HMS Public Projects are organized across the following GitHub organizations:

* **UMCG-TS-Development** – Active repositories, maintained projects, shared tools, libraries, templates, infrastructure, and documentation.
* **UMCG-TS-Archive** – Historical repositories that are retained for reference but are no longer actively maintained. Repositories in this organization should be considered read-only.

## Repository Naming Standards

Repositories should be named according to their primary purpose.

| Prefix   | Purpose                                                     |
| -------- | ----------------------------------------------------------- |
| `proj-`  | Project repositories                                        |
| `tool-`  | Standalone utilities, applications, or scripts              |
| `lib-`   | Reusable libraries and shared code                          |
| `tmpl-`  | Template repositories used to create new projects           |
| `fork-`  | Forks of third-party repositories                           |
| `infra-` | Infrastructure, automation, and administrative repositories |
| `docs-`  | Documentation and guidance                                  |

### Examples

```text
proj-room-booking
tool-report-generator
lib-pdf-processing
tmpl-python-tool
fork-openemr
infra-github-management
docs-development-standards
```

## Repository Lifecycle

Repositories generally move through the following lifecycle:

### Active

The repository is currently under development.

### Maintenance

The repository is still in use but only receives occasional updates, bug fixes, or maintenance.

### Archived

The repository is no longer actively maintained and is retained for historical reference. Archived repositories should not be modified without authorization.

Repositories that are permanently retired should be transferred to the **UMCG-TS-Archive** organization whenever appropriate.

---

# Access

Organization membership alone does not grant access to repositories.

By default:

* Members have **No Permissions**.
* Access is granted through **Teams** or **Direct Repository Access**.
* Organization membership is restricted to approved users.

When a member creates a repository within the organization, GitHub automatically grants that user administrative access to the repository.

## Recommended Access Model

For repositories with multiple contributors, access should be managed through **Teams** rather than individual user assignments.

Benefits include:

* Easier user management
* Consistent permissions
* Reduced administrative overhead
* Improved project visibility

> [!NOTE]
> When assigning permissions to a team, review the GitHub documentation on Repository Roles:
>
> https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization

---

# Creating New Repositories

Before creating a repository, determine its purpose and select the appropriate naming convention.

Examples:

| Purpose                 | Repository Name           |
| ----------------------- | ------------------------- |
| New application project | `proj-equipment-tracker`  |
| Shared Python library   | `lib-data-processing`     |
| Standalone utility      | `tool-file-renamer`       |
| Documentation           | `docs-training-materials` |

Avoid creating repositories with generic names such as:

```text
TestProject
PythonCode
NewRepo
Project1
```

Repository names should clearly describe their purpose.

---

# Adding Existing Repositories

If you wish to create a version of an existing repository, there are multiple options depending on how the source repository is configured.

## Download ZIP

Download the repository contents directly to your local machine.

A new repository can then be created and populated with the downloaded files.

This method does **not** preserve commit history.

## Template Repository

If a repository has been configured as a template, a **Use this template** button will appear on the repository page.

Selecting this option creates a new repository based on the template.

> [!WARNING]
> Repositories created from templates do not inherit commit history from the original repository.

## Fork a Repository

Forking creates a copy of an existing repository while preserving commit history.

Forks can continue to receive updates from the upstream repository.

This option is recommended when preserving project history is important.

> [!CAUTION]
> Forks should be used carefully when the resulting repository is expected to diverge significantly from the original project.

## Transfer from Another Account or Organization

Repositories may also be transferred from another GitHub account or organization.

> [!CAUTION]
> GitHub does not treat a repository transfer as repository creation.
>
> Administrative permissions are not automatically reassigned during a transfer.
>
> Repository access may need to be granted manually by an Organization Administrator after the transfer is completed.

---

# Managing Permissions

Repository permissions can be viewed and managed from:

**Repository → Settings → Collaborators and Teams**

This page displays all users and teams with access to the repository.

## Permission Sources

### Base Role

The permission level granted to all members of the organization.

Current default:

```text
No Permissions
```

### Direct Access

Permissions granted directly to individual users or teams.

### Organization Access

Permissions inherited through organization-level teams or roles.

For example, an organization-wide team may automatically receive access to multiple repositories.

## Team-Based Access

For repositories with multiple contributors, create a dedicated Team and assign permissions to the Team rather than to individual users.

Example:

```text
Project Team
├── Alice
├── Bob
└── Charlie
```

The Team is granted repository access once, and membership changes can be managed without modifying repository permissions.
