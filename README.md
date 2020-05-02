# How to deploy

Note: If you set Security Hub up to [collect findings across multiple accounts to master account](https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-accounts.html), you do the following in the master account.

1. Deploy CloudFormation stack using Notifier.yaml as the template.
Make note of stack's outputs.

1. Subscribe for SNS topic from the previous.

1. Create CloudFormation stack set using EventsCollector as the template.

1. Deploy EventsCollector stack instances in regions where AWS Security Hub is enabled.

# How to add a new account

Make sure that AWS Security Hub in the account is configured to share finding with the master account. You do nothing with the stacks from the above.

# How to add a new region

Deploy EventsCollector stack instance in the region.
