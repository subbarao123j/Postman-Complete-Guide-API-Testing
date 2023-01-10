https://developer.atlassian.com/cloud/trello/rest/api-group-actions/#api-actions-idaction-reactions-id-get

Actions
Applications
Batch
Boards
Cards
Checklists
CustomFields
Emoji
Enterprises
Labels
Lists
Members
Notifications
Organizations
Plugins
Search
Tokens
Webhooks


Actions
Get an Action
GET /1/actions/{id}

Get an Action

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the Action

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
display
boolean

Default: true
entities
boolean

Default: false
fields
string

all or a comma-separated list of action fields

Default: all
member
boolean

Default: true
member_fields
string

all or a comma-separated list of member fields

Default: avatarHash,fullName,initials,username
memberCreator
boolean

Whether to include the member object for the creator of the action

Default: true
memberCreator_fields
string

all or a comma-separated list of member fields

Default: avatarHash,fullName,initials,username
Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{id}?key=APIKey&token=APIToken'
Responses
200
Success

A schema has not been defined for this response code.

Update an Action
PUT /1/actions/{id}

Update a specific Action. Only comment actions can be updated. Used to edit the content of a comment.

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the Action

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
text REQUIRED
string

The new text for the comment

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request PUT \
  --url 'https://api.trello.com/1/actions/{id}?text={text}&key=APIKey&token=APIToken'
Responses
200
Success

A schema has not been defined for this response code.

Delete an Action
DELETE /1/actions/{id}

Delete a specific action. Only comment actions can be deleted.

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the Action

Pattern: ^[0-9a-fA-F]{24}$
Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request DELETE \
  --url 'https://api.trello.com/1/actions/{id}?key=APIKey&token=APIToken'
Responses
200
Success

A schema has not been defined for this response code.

Get a specific field on an Action
GET /1/actions/{id}/{field}

Get a specific property of an action

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the Action

Pattern: ^[0-9a-fA-F]{24}$
field REQUIRED
string

An action field

Valid values: id, idMemberCreator, data, type, date, limits, display, memberCreator

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{id}/{field}?key=APIKey&token=APIToken' \
  --header 'Accept: application/json'
Responses
200
Success

Content type	Value
application/json	
Action

Get the Board for an Action
GET /1/actions/{id}/board

Get the Board for an Action

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the action

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
fields
string

all or a comma-separated list of board fields

Valid values: id, name, desc, descData, closed, idMemberCreator, idOrganization, pinned, url, shortUrl ...(Show more)

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{id}/board?key=APIKey&token=APIToken' \
  --header 'Accept: application/json'
Responses
200
Success

Content type	Value
application/json	
Board

Get the Card for an Action
GET /1/actions/{id}/card

Get the card for an action

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the action

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
fields
string

all or a comma-separated list of card fields

Valid values: id, address, badges, checkItemStates, closed, coordinates, creationMethod, dueComplete, dateLastActivity, desc ...(Show more)

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{id}/card?key=APIKey&token=APIToken' \
  --header 'Accept: application/json'
Responses
200
Success

Content type	Value
application/json	
Card

Get the List for an Action
GET /1/actions/{id}/list

Get the List for an Action

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the action

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
fields
string

all or a comma-separated list of list fields

Valid values: id

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{id}/list?key=APIKey&token=APIToken' \
  --header 'Accept: application/json'
Responses
200
Success

Content type	Value
application/json	
TrelloList

Get the Member of an Action
GET /1/actions/{id}/member

Gets the member of an action (not the creator)

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the Action

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
fields
string

all or a comma-separated list of member fields

Valid values: id

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{id}/member?key=APIKey&token=APIToken' \
  --header 'Accept: application/json'
Responses
200
Success

Content type	Value
application/json	
Member

Get the Member Creator of an Action
GET /1/actions/{id}/memberCreator

Get the Member who created the Action

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the Action

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
fields
string

all or a comma-separated list of member fields

Valid values: id

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{id}/memberCreator?key=APIKey&token=APIToken' \
  --header 'Accept: application/json'
Responses
200
Success

Content type	Value
application/json	
Member

Get the Organization of an Action
GET /1/actions/{id}/organization

Get the Organization of an Action

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the action

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
fields
string

all or a comma-separated list of organization fields

Valid values: id, name

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{id}/organization?key=APIKey&token=APIToken' \
  --header 'Accept: application/json'
Responses
200
Success

Content type	Value
application/json	
Organization

Update a Comment Action
PUT /1/actions/{id}/text

Update a comment action

Request
PATH PARAMETERS
id REQUIRED
string

The ID of the action to update

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
value REQUIRED
string

The new text for the comment

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request PUT \
  --url 'https://api.trello.com/1/actions/{id}/text?value={value}&key=APIKey&token=APIToken'
Responses
200
Success

A schema has not been defined for this response code.

Get Action's Reactions
GET /1/actions/{idAction}/reactions

List reactions for an action

Request
PATH PARAMETERS
idAction REQUIRED
string

The ID of the action

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
member
boolean

Whether to load the member as a nested resource. See Members Nested Resource

Default: true
emoji
boolean

Whether to load the emoji as a nested resource.

Default: true
Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{idAction}/reactions?key=APIKey&token=APIToken'
Responses
200
Success

A schema has not been defined for this response code.

Create Reaction for Action
POST /1/actions/{idAction}/reactions

Adds a new reaction to an action

Request
PATH PARAMETERS
idAction REQUIRED
string

The ID of the action

Pattern: ^[0-9a-fA-F]{24}$
BODY PARAMETERS
shortName
string

The primary shortName of the emoji to add. See /emoji

skinVariation
string

The skinVariation of the emoji to add. See /emoji

native
string

The emoji to add as a native unicode emoji. See /emoji

unified
string

The unified value of the emoji to add. See /emoji

Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request POST \
  --url 'https://api.trello.com/1/actions/{idAction}/reactions?key=APIKey&token=APIToken' \
  --header 'Content-Type: application/json' \
  --data '{
  "shortName": "<string>",
  "skinVariation": "<string>",
  "native": "<string>",
  "unified": "<string>"
}'
Responses
200
Success

A schema has not been defined for this response code.

Get Action's Reaction
GET /1/actions/{idAction}/reactions/{id}

Get information for a reaction

Request
PATH PARAMETERS
idAction REQUIRED
string

The ID of the Action

Pattern: ^[0-9a-fA-F]{24}$
id REQUIRED
string

The ID of the reaction

Pattern: ^[0-9a-fA-F]{24}$
QUERY PARAMETERS
member
boolean

Whether to load the member as a nested resource. See Members Nested Resource

Default: true
emoji
boolean

Whether to load the emoji as a nested resource.

Default: true
Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{idAction}/reactions/{id}?key=APIKey&token=APIToken'
Responses
200
Success

A schema has not been defined for this response code.

Delete Action's Reaction
DELETE /1/actions/{idAction}/reactions/{id}

Deletes a reaction

Request
PATH PARAMETERS
idAction REQUIRED
string

The ID of the Action

Pattern: ^[0-9a-fA-F]{24}$
id REQUIRED
string

The ID of the reaction

Pattern: ^[0-9a-fA-F]{24}$
Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request DELETE \
  --url 'https://api.trello.com/1/actions/{idAction}/reactions/{id}?key=APIKey&token=APIToken'
Responses
200
Success

A schema has not been defined for this response code.

List Action's summary of Reactions
GET /1/actions/{idAction}/reactionsSummary

List a summary of all reactions for an action

Request
PATH PARAMETERS
idAction REQUIRED
string

The ID of the action

Pattern: ^[0-9a-fA-F]{24}$
Example
cURL
Node.js
Java
Python
PHP
Copy
curl --request GET \
  --url 'https://api.trello.com/1/actions/{idAction}/reactionsSummary?key=APIKey&token=APIToken'
Responses
200
Success

A schema has not been defined for this response code.
