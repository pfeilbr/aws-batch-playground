# aws-batch-fargate-example

example of creating fargate batch compute environment, queue, definition and submitting a job

## Demo

```sh
# deploy stack
# note the outputs for the following commands
sam deploy

# submit job
aws batch submit-job \
    --job-name aws-batch-fargate-example-my-job-01 \
    --job-queue aws-batch-fargate-example-fargate \
    --job-definition aws-batch-fargate-example-my-job-01:1

# view job output logs
aws logs tail "/aws/batch/job"

# delete stack
sam delete --no-prompt
```

## Screenshots

job output log

![](https://www.evernote.com/l/AAExdhVv45VBpqBFFVxrcs9cMdX99wFYqPgB/image.png)

## Resources

- 