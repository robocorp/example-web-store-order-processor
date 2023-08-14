# Development data placeholder

This directory should contain local development data only.

This info should not be used in the actual Robocorp Process run but can be
used when you are building and debugging your configuration and robots.

## What to put here?

- Local Work Item data
- Local environment variables (in JSON format)
- Local custom data files (\*.xlsx, \*.csv etc.)

## The environment file

Our default template [*env-local.json*](./env-local.json) file lists the default
environment variables to run with, useful during local runs and not suitable in the
cloud. You need to configure the Control Room process with such variables if you want
them available there as well.
