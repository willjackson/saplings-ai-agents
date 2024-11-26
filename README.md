![saplings](https://github.com/kanopi/saplings/assets/5177009/a6377e32-deb2-49d8-873a-f3dd5a36fa7c)

# Saplings - AI Agents

Adds an AI powered chatbot for Drupal site building.

This is a fork of [drupal/ai_agents_chatbot_evaluation_recipe](https://www.drupal.org/project/ai_agents_chatbot_evaluation_recipe)
with additional OpenAI configuration for faster setup.

## Features
- Creates the following Drupal site building agents available to the chatbot:
  - Views
  - Taxonomy
  - Enable module
  - Webform
  - Content type
  - Field type

## Installation

```
composer require kanopi/saplings-ai-agents
drush recipe ../recipes/saplings-ai-agents
```

To unpack the dependencies of this recipe, you can use the `recipe-unpack` 
command that comes in the `kanopi/drupal-starter` repository

```
fin recipe-unpack kanopi/saplings-ai-agents
```

Export configuration and commit to git as normal.


### Configure OpenAI

While the AI module supports many AI services, this recipe is configure to use
OpenAI. If you have set up the Saplings AI CKEditor recipe, this is the same
process/key.

1. Create an API key at https://platform.openai.com
2. Create a key file at `private://keys/openai_provider.key`. That is usually at
   `[webroot]/sites/default/files/private/keys/openai_provider.key`.
3. Once you are ready to deploy, be sure to place that key in your cloud
environments on the site's host. If you place it in the canonical environment,
it will get cloned on subsequent multidev clones.


## Usage

Users with the Administrator will now have a Chatbot in the bottom right of any
page that appears in the admin theme.
