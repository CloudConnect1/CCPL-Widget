# widget

Here we have 2 files which you need to keep in the same location. 

1. Widget.html is the main file where you need to pass the credentials in it integrate the script in your CRM or website.
2. Credentials will be provided by CloudConnect Team.
3. widgetjs.js file is mandatory to be kept in the same location of Widget.html


Widget.html Contains the following controls which customer can set according to his/her call flow. 

## Color Codes for widgets are set by default if you want to change then you need to make changes in Widget.html color theme settings 

Sample: 

"colors": {
                "primary": "#5E95E8",
                "secondary": "#0d8099",
                "main-text": "#414C59",
                "secondary-text": "#8292A5",
                "button-pressed-text": "#FFF",
                "border-lines": "#DDD",
                "primary-bg": "#FFF",
                "secondary-bg": "#F0F2F4",
                "inactive-bg": "#B9C2CC",
                "success": "#7CC24F",
                "danger": "#EC2A2A",
                "additional-danger-bg": "#F44C4C",
                "additional-success-bg": "#75B8A0",
                "additional-bg": "#B0BFC2"

## Widget location and display configurational settings are under layoutconfig.

Sample:

  "layoutConfig": {
                "type": "rounded",
                "mode": "floating",
                "position": {
                    "bottom": "unset",
                    "anchor": "bottom-center",
                    "top": "unset",
                    "right": "unset",
                    "left": "50vw"
                }

## Call Controls configuration settings are under call settings section.

Sample:

  const callSettings = {
            "allowTransfer": true,
            "autoAnswer": {
                "allowChange": false,
                "defaultBehavior": false
            },
            "outgoingCalls": true,
            "callerInfo": {
                "displayName": true,
                "callerId": {
                    "display": true,
                    "mask": false
                }

Description: 

1. allowTransfer : If its set to true then agent would be allow to transfer calls if false then icon for transfer would be removed from agent widget.
2. autoAnswer :  there are 2 parameters under this "allowChange" which means if true then agent can manually turn OFF or ON  auto answer. Second is defaultBehavior if set to true then default behaviour of autoanswer is ON.
3. outgoingCalls : if set to true then agent would be able to make manual calls by typing number. If set false then agent can make calls only via API.
4. mask : if set to false then agent would be able to see the customer's number and if true system will mask the number. 

                
