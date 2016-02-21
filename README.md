# Webmerge Relay

Server-side script that parses NationBuilder webhooks into [Webmerge](https://www.webmerge.me/). Originally written to send users pre-filled voter registration PDFs for printing and mailing.

Before uploading, update the following:

*   **Line 62** with your Webmerge document ID
*   **Line 63** with your [Webmerge API Key](https://www.webmerge.me/manage/account?page=api)
*   **Line 18** with the tag given to signups on your NationBuilder signup page

Set the script's URL as your [NationBuilder webhooks](http://nationbuilder.com/webhooks_overview) endpoint. You will need to update your document's field map to use the provided field names. Currently, relay.php provides the following:

*   {$FirstName}
*   {$LastName}
*   {$City}
*   {$State}
*   {$Address}
*   {$Zip}
*   {$Email}
*   {$DOB}
*   {$County}*

_*Due to the way NationBuilder handles submitted addresses, **county** will likely not be included unless it's been manually entered by an administrator beforehand_