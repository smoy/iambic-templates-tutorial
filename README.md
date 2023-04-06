# iambic-templates-tutorial

This repository contains IAMbic templates that track multiple AWS accounts in an AWS Organization. In addition, IAMbic Github integration is configured to automatically import new resources based on import workflow schedule.

# What is IAMbic

Visit the [repo](https://github.com/noqdev/iambic). IAMbic is an ecosystem of core tools and plugins to manage cloud IAM across multi-cloud providers. It stores cloud IAM in declarative YAML with validators and both pushes and pull changes from cloud services.

# Directory Structure

IAMbic does not enforce directory structure for supported templates. It does come with opinion default when it imports resources from plugin. (like AWS)

For example

```console
smoy@mbp iambic-templates-tutorial % tree
.
├── LICENSE
├── README.md
├── config
│   └── iambic_config.yaml
└── resources
    └── aws
        ├── iam
        │   ├── managed_policy
        │   │   └── iambic-tutorial-aws-dev
        │   │       ├── amazon-eventbridge-scheduler-execution-policy-3cbacae5-aec0-4f7d-8225-e4c971c46e18.yaml
        │   │       └── awslambdabasicexecutionrole-78a8ff97-2ce1-463c-8ade-3ebefaa55e39.yaml
        │   ├── role
        │   │   ├── all_accounts
        │   │   │   ├── awsservicerolefororganizations.yaml
        │   │   │   ├── awsserviceroleforsso.yaml
        │   │   │   ├── awsserviceroleforsupport.yaml
        │   │   │   ├── awsservicerolefortrustedadvisor.yaml
        │   │   │   └── iambicspokerole.yaml
        │   │   ├── iambic-tutorial-aws-dev
        │   │   │   ├── amazon_eventbridge_scheduler_lambda_0a11868946.yaml
        │   │   │   ├── awsreservedsso_administratoraccess_a8b8dc74ce313286.yaml
        │   │   │   ├── import-sensor.yaml
        │   │   │   ├── sample-app-role-dev.yaml
        │   │   │   └── update_role_description-role-j21873m9.yaml
        │   │   ├── iambic-tutorial-aws-mgmt
        │   │   │   ├── awsreservedsso_administratoraccess_c46a6fdefb24c150.yaml
        │   │   │   ├── awsserviceroleforcloudformationstacksetsorgadmin.yaml
        │   │   │   ├── iambic_github_app_lambda_execution.yaml
        │   │   │   └── iambichubrole.yaml
        │   │   ├── iambic-tutorial-aws-prod
        │   │   │   ├── awsreservedsso_administratoraccess_6dc64117fc3def79.yaml
        │   │   │   └── sample-app-role-prod.yaml
        │   │   ├── iambic-tutorial-aws-stage
        │   │   │   ├── awsreservedsso_administratoraccess_ebe7cc3131876224.yaml
        │   │   │   └── sample-app-role-stage.yaml
        │   │   └── multi_account
        │   │       ├── awsserviceroleforcloudformationstacksetsorgmember.yaml
        │   │       ├── organizationaccountaccessrole.yaml
        │   │       └── stacksets-exec-3a13bad69ee5cf8afa9722d7c9573dc1.yaml
        │   └── user
        │       └── multi_account
        │           ├── alice.yaml
        │           ├── bob.yaml
        │           └── charlie.yaml
        └── identity_center
            └── permission_set
                └── administratoraccess.yaml

```

# IAMbic Github integration

Check out the [PR #2](https://github.com/smoy/iambic-templates-tutorial/pull/2) in which the integration automatically plans the effect of the template change. The integration uploads markup response directly in the PR. In addition, it places machine artifacts in the companion [repository](https://github.com/smoy/iambic-templates-tutorial-gist). 

# Repository Visibility

This repository and its companion repository are public for illustrative purposes. You do not have to make your iambic templates repository public. Some of the template will contain PII (personal identifiable information) because email may be an required attribute in some cloud resources. Most organization will not make their infrastructure as code repository public. 
