# Terraform Provider JumpCloud

[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=sagewave_terraform-provider-jumpcloud&metric=alert_status)](https://sonarcloud.io/dashboard?id=sagewave_terraform-provider-jumpcloud)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=sagewave_terraform-provider-jumpcloud&metric=coverage)](https://sonarcloud.io/dashboard?id=sagewave_terraform-provider-jumpcloud)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=sagewave_terraform-provider-jumpcloud&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=sagewave_terraform-provider-jumpcloud)
[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=sagewave_terraform-provider-jumpcloud&metric=ncloc)](https://sonarcloud.io/dashboard?id=sagewave_terraform-provider-jumpcloud)

The JumpCloud provider provides resources to interact with the JumpCloud API v1 and v2. 

This provider was forked from [https://github.com/sagewave/terraform-provider-jumpcloud](https://github.com/sagewave/terraform-provider-jumpcloud), somehow a year later when I needed to use it the organization name changed and my changes got deleted during a force push. Right now I do not have the time and resource to re-factor to current version and re-create the PR, so I'm just going to publish this fork for now and according to the license I should disclose the source which I am doing right here.

## Usage

The provider is published to the Terraform registry and can be used in the same way as any other provider. For detailed documentation with usage examples [view the generated docs in the Terraform registry](https://registry.terraform.io/providers/sagewave/jumpcloud/latest/docs).

## Requirements

-	[Terraform](https://www.terraform.io/downloads.html) >= 0.13.x
-	[Go](https://golang.org/doc/install) >= 1.15

## Building The Provider

1. Clone the repository
1. Enter the repository directory
1. Build the provider using the Go `install` command: 
```sh
$ go install
```

## Adding Dependencies   

This provider uses [Go modules](https://github.com/golang/go/wiki/Modules).
Please see the Go documentation for the most up to date information about using Go modules.

To add a new dependency `github.com/author/dependency` to your Terraform provider:

```
go get github.com/author/dependency
go mod tidy
```

Then commit the changes to `go.mod` and `go.sum`.

## Developing the Provider

If you wish to work on the provider, you'll first need [Go](http://www.golang.org) installed on your machine (see [Requirements](#requirements) above).

To compile the provider, run `go install`. This will build the provider and put the provider binary in the `$GOPATH/bin` directory.

To generate or update documentation, run `go generate`.

In order to run the full suite of Acceptance tests, run `make testacc`.

*Note:* Acceptance tests create real resources, and often cost money to run.

```sh
$ JUMPCLOUD_API_KEY=xxx JUMPCLOUD_ORG_ID=xxx make testacc
```
## Acknowledgement

This repo is based on [https://github.com/CognotektGmbH/terraform-provider-jumpcloud](https://github.com/CognotektGmbH/terraform-provider-jumpcloud)