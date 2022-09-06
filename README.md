# ECS Deploy

Updates an existing ECS task with a new image

`key`: The Buildkite pipeline key for the generated step. Defaults to tag. Must be set if this plugin is used multiple times in a single pipeline.
`label`: Label for generated step. Defaults to Tag.
`arn_role`: Full role to run this operation with. Must be able to read the old tag's manifest and create a new image with that manifest.
`command`: The command for ecs deploy container to run
`depends_on`: An array of tasks to depend_on in a buildkite sense

This plugin injects a new step into your pipeline immediately after it has executed to perform this operation
