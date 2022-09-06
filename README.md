# ECS Deploy

Updates an existing ECS task with a new image

`key`: The Buildkite pipeline key for the generated step. Defaults to tag. Must be set if this plugin is used multiple times in a single pipeline.
`label`: Label for generated step. Defaults to Tag.
`arn_role`: Full role to run this operation with. Must be able to read the old tag's manifest and create a new image with that manifest.
`cluster`: The ECS cluster to deploy to
`task`: The ECS task to update
`image`: The image in the ECS task to update
`ecr_url`: DNS entry of ECR
`repository`: ECR repository name
`new_tag`: The new image tag which this plugin will deploy
`depends_on`: An array of tasks to depend_on in a buildkite sense

This plugin injects a new step into your pipeline immediately after it has executed to perform this operation
