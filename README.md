# portainer-app-template-megalist
There's already a ton of thesee on the web, I'm just hosting one for my own intereests without having to reinvent the wheel or, worse, have to remember where I found it.

## Usage (In less than 9 steps)
1. Go to your Portainer instance
2. Go to "Settings" -> "App Templates"
3. Click the url field and paste in the following: `https://raw.githubusercontent.com/mackmoe/portainer-app-template-megalist/main/default_template.json`
4. Click "Save settings"
5. Go back to to "Home" again and select your enviroment
6. Click "Application Templates" on the left pane
7. Select the stack you want to deploy to
8. Click "Deploy the template"


## Proper Jason format
Simple Template Block - using git:
```
{
  "type": ,  # Valid values: 1 = container; 2 = Swarm stack; 3 = Compose stack - Type 3 is limited to using the version "2" stack format (this is a docker/libcompose limitation).
  "title": "", 
  "description": "",
  "note": "",
  "categories": [""],
  "platform": "", # Valid values: "linux"; "windows" - Displays a small platform-related icon in the Portainer UI.
  "logo": "", # Valid img url
  "repository": {
    "url": "https://github.com/portainer/templates",
    "stackfile": "stacks/cockroachdb/docker-stack.yml"
  }
}
```
Template Block - using env:
```
{
    "type": 3,
    "title": "",
    "description": "",
    "image": "",
    "administrator-only": false,
    "name": "",
    "logo": "",
     "env": [{
        "name": "",
        "label": "",
        "default": "",
        "preset": "", # "boolean. If set to true, the UI will not generate an input (optional)",
        "description": "what-I-do"
     }
    ],
    "volumes": [{
        "container": "",
        "bind": ""
    }],
    "ports": [""],
    "privileged": true,
    "restart_policy": "",
    "hostname": "",
    "platform": "",
    "categories": ["", "", ""]
},
```
Template Block :
```
{
    "type": 3,
    "title": "",
    "description": "",
    "administrator-only": false,
    "image": "",
    "name": "",
    "logo": "",
    "volumes": [{
        "container": "",
        "bind": ""
    },
    {
        "container": "",
        "bind": ""
    }],
    "ports": ["",""],
    "privileged": true,
    "restart_policy": "unless-stopped",
    "hostname": "",
    "note": "",
    "platform": "",
    "categories": ["", "", ""]
},
```
