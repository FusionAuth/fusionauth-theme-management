# Theme management

This repository has some tools to help with FusionAuth theme management. More about FusionAuth themes: https://fusionauth.io/docs/v1/tech/themes/

## Prerequisites

You need to have curl, jq and python3 installed.

You also need to have an API key with sufficient privileges.

Finally, you'll have to create a new theme and have associated it with your tenant.

## Message property files

The default messages files allows you to customize messages in the FusionAuth login screens.

### Retrieving messages

`retrieve-default-messages.sh <API_KEY> <THEME_ID>`

This will produce a file `defaultmessages.txt` in your current directory. Edit this with your new messages. You can also version control this file.

### Updating messages

`patch-default-messages.sh <API_KEY> <THEME_ID>`

This will load the `defaultmessages.txt` file up to FusionAuth, making any changes live.

### Limitations

This only works for the default messages file, not for any localizations. 
