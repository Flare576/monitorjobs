# monitorjobs

<img src="./preview.png" alt="Image showing colors and icons of tool" width=900></img>

Shell script driven by your .aws/config and a few settings

## Installation

monitorjobs is a bash script, so putting it anywhere in your $PATH is all you really need to do!

You can also do `brew install flare576/scripts/monitorjobs`

## Setup

You will need to have [aws-cli](https://aws.amazon.com/cli/) setup and authenticated.

You will also need [jq](https://jqlang.github.io/jq/download/).

If you have ZSH, export your list of jobs somewhere in your profile:

```
export AWS_JOBS_LIST=(
  SUCCESSFUL_INACTIVE_AND_HAPPY
  I_AM_FAIL
  IN_PROGRESS_JOB
)
```

If you're not using ZSH, you'll need to make a configuration file where each line is a project:

```
SUCCESSFUL_INACTIVE_AND_HAPPY
I_AM_FAIL
IN_PROGRESS_JOB
```

and include it in the call with -f

```
monitorjobs -f /my/config/file
```
