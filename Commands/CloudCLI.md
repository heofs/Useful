# Cloud

## AWS

### AWS CLI

To set up AWS access you first need to install [AWS Command Line Interface](https://aws.amazon.com/cli/).

Then follow the [instructions for setting up the CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html).

For available commands, see [reference for CLI](https://docs.aws.amazon.com/cli/latest/index.html).

### DynamoDB

To set up AWS access you first need to install [AWS Command Line Interface](https://aws.amazon.com/cli/).

Then run `aws configure` and fill in the requested information.

```
AWS Access Key ID [None]: AWS IAM access key
AWS Secret Access Key [None]: AWS IAM secret key
Default region name [None]: Your dynamo location, for example eu-central-1
Default output format [None]: ENTER
```

You should now be able to run commands like this:

To create a new table.
```sql
aws dynamodb create-table \
    --table-name Music \
    --attribute-definitions \
        AttributeName=Artist,AttributeType=S \
        AttributeName=SongTitle,AttributeType=S \
    --key-schema AttributeName=Artist,KeyType=HASH AttributeName=SongTitle,KeyType=RANGE \
    --provisioned-throughput ReadCapacityUnits=1,WriteCapacityUnits=1
```
Or to describe a table.
```sql
aws dynamodb describe-table --table-name Music
```

