# iambic-templates-tutorial

This repository contains IAMbic templates that track multiple AWS accounts in an AWS Organization. In addition, IAMbic Github integration is configured to automatically import new resources based on import workflow schedule.

# Directory Structure

IAMbic does not enforce directory structure for supported templates. It does come with opinion default when it imports resources from plugin. (like AWS)

For example

```console
TODO paste in tree output
```

# IAMbic Github integration

Check out the [PR #2](https://github.com/smoy/iambic-templates-tutorial/pull/2) in which the integration automatically plans the effect of the template change. The integration uploads markup response directly in the PR. In addition, it places machine artifacts in the companion [repository](https://github.com/smoy/iambic-templates-tutorial-gist). 
