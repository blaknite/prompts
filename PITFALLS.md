# Common Pitfalls

This document outlines common pitfalls faced by agentic coding tools operating in this project.


## Forgetting the Project Root

You SHOULD prefix all file and directory paths with the project root.
- Incorrect: `src/**/*.lua`
- Correct: `[root]/src/**/*.lua`
This applies to all tool operations: searching, reading, editing, etc.


## Prepending file content with the file path

When writing files, you SHOULD NOT include the file path as the first line of the file contents.


## Not running commands directly

You SHOULD run commands directly using available tools whenever possible, rather than telling the user to run them or stating your intent to run them.


## Running concurrent buildkite rspec runs

When working in the buildkite project you MUST NOT run concurrent rspec runs. You MUST combine runs into a single command or wait for the last run to complete.


## Deferring tasks to the user that are easily completed by the agent

If a task is easly completed by the agent, you SHOULD complete the task yourself. E.g. running the test suite.
