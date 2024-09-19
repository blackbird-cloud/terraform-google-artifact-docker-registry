<!-- BEGIN_TF_DOCS -->
# Terraform Google Artifact Docker Registry Module
A Terraform module which helps you create Artifact Registry repositories.

[![blackbird-logo](https://raw.githubusercontent.com/blackbird-cloud/terraform-module-template/main/.config/logo_simple.png)](https://blackbird.cloud)

## Example
```hcl

```

## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1 |
| <a name="requirement_google"></a> [google](#requirement\_google) | ~> 4 |
| <a name="requirement_google-beta"></a> [google-beta](#requirement\_google-beta) | ~> 4 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_google-beta"></a> [google-beta](#provider\_google-beta) | ~> 4 |

## Resources

| Name | Type |
|------|------|
| [google-beta_google_artifact_registry_repository.default](https://registry.terraform.io/providers/hashicorp/google-beta/latest/docs/resources/google_artifact_registry_repository) | resource |
| [google-beta_google_artifact_registry_repository_iam_member.readers](https://registry.terraform.io/providers/hashicorp/google-beta/latest/docs/resources/google_artifact_registry_repository_iam_member) | resource |
| [google-beta_google_artifact_registry_repository_iam_member.writers](https://registry.terraform.io/providers/hashicorp/google-beta/latest/docs/resources/google_artifact_registry_repository_iam_member) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_description"></a> [description](#input\_description) | (Optional) The user-provided description of the repository. | `string` | `null` | no |
| <a name="input_immutable_tags"></a> [immutable\_tags](#input\_immutable\_tags) | (Optional) The repository which enabled this flag prevents all tags from being modified, moved or deleted. This does not prevent tags from being created. Defaults to `true`. | `bool` | `true` | no |
| <a name="input_kms_key_name"></a> [kms\_key\_name](#input\_kms\_key\_name) | (Optional) The Cloud KMS resource name of the customer managed encryption key that’s used to encrypt the contents of the Repository. Has the form: `projects/my-project/locations/my-region/keyRings/my-kr/cryptoKeys/my-key`. This value may not be changed after the Repository has been created. | `string` | `null` | no |
| <a name="input_labels"></a> [labels](#input\_labels) | (Optional) Labels with user-defined metadata. This field may contain up to 64 entries. Label keys and values may be no longer than 63 characters. Label keys must begin with a lowercase letter and may only contain lowercase letters, numeric characters, underscores, and dashes. | `map(string)` | `{}` | no |
| <a name="input_location"></a> [location](#input\_location) | (Optional) The name of the location this repository is located in. | `string` | `null` | no |
| <a name="input_project"></a> [project](#input\_project) | (Optional) The ID of the project in which the resource belongs. If it is not provided, the provider project is used. | `string` | `null` | no |
| <a name="input_readers"></a> [readers](#input\_readers) | (Optional) Identities that will be granted the read privilege in role. Each entry can have one of the following values:<br><br>- allUsers: A special identifier that represents anyone who is on the internet; with or without a Google account.<br>- allAuthenticatedUsers: A special identifier that represents anyone who is authenticated with a Google account or a service account.<br>- user:{emailid}: An email address that represents a specific Google account. For example, alice@gmail.com or joe@example.com.<br>- serviceAccount:{emailid}: An email address that represents a service account. For example, my-other-app@appspot.gserviceaccount.com.<br>- group:{emailid}: An email address that represents a Google group. For example, admins@example.com.<br>- domain:{domain}: A G Suite domain (primary, instead of alias) name that represents all the users of that domain. For example, google.com or example.com.<br>- projectOwner:projectid: Owners of the given project. For example, "projectOwner:my-example-project"<br>- projectEditor:projectid: Editors of the given project. For example, "projectEditor:my-example-project"<br>- projectViewer:projectid: Viewers of the given project. For example, "projectViewer:my-example-project" | `list(string)` | `[]` | no |
| <a name="input_repository_id"></a> [repository\_id](#input\_repository\_id) | (Required) The last part of the repository name, for example: 'repo1'. | `string` | n/a | yes |
| <a name="input_writers"></a> [writers](#input\_writers) | (Optional) Identities that will be granted the write privilege in role. Each entry can have one of the following values:<br><br>- allUsers: A special identifier that represents anyone who is on the internet; with or without a Google account.<br>- allAuthenticatedUsers: A special identifier that represents anyone who is authenticated with a Google account or a service account.<br>- user:{emailid}: An email address that represents a specific Google account. For example, alice@gmail.com or joe@example.com.<br>- serviceAccount:{emailid}: An email address that represents a service account. For example, my-other-app@appspot.gserviceaccount.com.<br>- group:{emailid}: An email address that represents a Google group. For example, admins@example.com.<br>- domain:{domain}: A G Suite domain (primary, instead of alias) name that represents all the users of that domain. For example, google.com or example.com.<br>- projectOwner:projectid: Owners of the given project. For example, "projectOwner:my-example-project"<br>- projectEditor:projectid: Editors of the given project. For example, "projectEditor:my-example-project"<br>- projectViewer:projectid: Viewers of the given project. For example, "projectViewer:my-example-project" | `list(string)` | `[]` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_registry"></a> [registry](#output\_registry) | n/a |

## About

We are [Blackbird Cloud](https://blackbird.cloud), Amsterdam based cloud consultancy, and cloud management service provider. We help companies build secure, cost efficient, and scale-able solutions.

Checkout our other :point\_right: [terraform modules](https://registry.terraform.io/namespaces/blackbird-cloud)

## Copyright

Copyright © 2017-2024 [Blackbird Cloud](https://blackbird.cloud)
<!-- END_TF_DOCS -->