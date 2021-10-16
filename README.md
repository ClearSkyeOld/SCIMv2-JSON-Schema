# SCIMv2-JSON-Schema
Data validation for Identity objects in transit


## User
User object
```json
{
  "schemas": ["urn:ietf:params:scim:schemas:core:2.0:User"],
  "id":"2819c223-7f76-453a-919d-413861904646",
  "externalId":"dschrute",
  "meta":{
    "resourceType": "User",
    "created":"2011-08-01T18:29:49.793Z",
    "lastModified":"2011-08-01T18:29:49.793Z",
    "location":"https://example.com/v2/Users/2819c223...",
    "version":"W\/\"f250dd84f0671c3\""
  },
  "name":{
    "formatted": "Mr. Dwight K Schrute, III",
    "familyName": "Schrute",
    "givenName": "Dwight",
    "middleName": "Kurt",
    "honorificPrefix": "Mr.",
    "honorificSuffix": "III"
  },
  "userName":"dschrute",
  "phoneNumbers":[
    {
      "value":"555-555-8377",
      "type":"work"
    }
  ],
  "emails":[
    {
      "value":"dschrute@example.com",
      "type":"work",
      "primary": true
    }
  ]
}
```

User ValidationSchema
```
{
	"definitions": {},
	"$schema": "http://json-schema.org/draft-07/schema#", 
	"$id": "https://example.com/object1634331345.json", 
	"title": "Root", 
	"type": "object",
	"required": [
		"schemas",
		"id",
		"externalId",
		"meta",
		"name",
		"userName",
		"phoneNumbers",
		"emails"
	],
	"properties": {
		"schemas": {
			"$id": "#root/schemas", 
			"title": "Schemas", 
			"type": "array",
			"default": [],
			"items":{
				"$id": "#root/schemas/items", 
				"title": "Items", 
				"type": "string",
				"default": "",
				"examples": [
					"urn:ietf:params:scim:schemas:core:2.0:User"
				],
				"pattern": "^.*$"
			}
		},
		"id": {
			"$id": "#root/id", 
			"title": "Id", 
			"type": "string",
			"default": "",
			"examples": [
				"2819c223-7f76-453a-919d-413861904646"
			],
			"pattern": "^.*$"
		},
		"externalId": {
			"$id": "#root/externalId", 
			"title": "Externalid", 
			"type": "string",
			"default": "",
			"examples": [
				"dschrute"
			],
			"pattern": "^.*$"
		},
		"meta": {
			"$id": "#root/meta", 
			"title": "Meta", 
			"type": "object",
			"required": [
				"resourceType",
				"created",
				"lastModified",
				"location",
				"version"
			],
			"properties": {
				"resourceType": {
					"$id": "#root/meta/resourceType", 
					"title": "Resourcetype", 
					"type": "string",
					"default": "",
					"examples": [
						"User"
					],
					"pattern": "^.*$"
				},
				"created": {
					"$id": "#root/meta/created", 
					"title": "Created", 
					"type": "string",
					"default": "",
					"examples": [
						"2011-08-01T18:29:49.793Z"
					],
					"pattern": "^.*$"
				},
				"lastModified": {
					"$id": "#root/meta/lastModified", 
					"title": "Lastmodified", 
					"type": "string",
					"default": "",
					"examples": [
						"2011-08-01T18:29:49.793Z"
					],
					"pattern": "^.*$"
				},
				"location": {
					"$id": "#root/meta/location", 
					"title": "Location", 
					"type": "string",
					"default": "",
					"examples": [
						"https://example.com/v2/Users/2819c223..."
					],
					"pattern": "^.*$"
				},
				"version": {
					"$id": "#root/meta/version", 
					"title": "Version", 
					"type": "string",
					"default": "",
					"examples": [
						"W/\"f250dd84f0671c3\""
					],
					"pattern": "^.*$"
				}
			}
		}
,
		"name": {
			"$id": "#root/name", 
			"title": "Name", 
			"type": "object",
			"required": [
				"formatted",
				"familyName",
				"givenName",
				"middleName",
				"honorificPrefix",
				"honorificSuffix"
			],
			"properties": {
				"formatted": {
					"$id": "#root/name/formatted", 
					"title": "Formatted", 
					"type": "string",
					"default": "",
					"examples": [
						"Mr. Dwight K Schrute, III"
					],
					"pattern": "^.*$"
				},
				"familyName": {
					"$id": "#root/name/familyName", 
					"title": "Familyname", 
					"type": "string",
					"default": "",
					"examples": [
						"Schrute"
					],
					"pattern": "^.*$"
				},
				"givenName": {
					"$id": "#root/name/givenName", 
					"title": "Givenname", 
					"type": "string",
					"default": "",
					"examples": [
						"Dwight"
					],
					"pattern": "^.*$"
				},
				"middleName": {
					"$id": "#root/name/middleName", 
					"title": "Middlename", 
					"type": "string",
					"default": "",
					"examples": [
						"Kurt"
					],
					"pattern": "^.*$"
				},
				"honorificPrefix": {
					"$id": "#root/name/honorificPrefix", 
					"title": "Honorificprefix", 
					"type": "string",
					"default": "",
					"examples": [
						"Mr."
					],
					"pattern": "^.*$"
				},
				"honorificSuffix": {
					"$id": "#root/name/honorificSuffix", 
					"title": "Honorificsuffix", 
					"type": "string",
					"default": "",
					"examples": [
						"III"
					],
					"pattern": "^.*$"
				}
			}
		}
,
		"userName": {
			"$id": "#root/userName", 
			"title": "Username", 
			"type": "string",
			"default": "",
			"examples": [
				"dschrute"
			],
			"pattern": "^.*$"
		},
		"phoneNumbers": {
			"$id": "#root/phoneNumbers", 
			"title": "Phonenumbers", 
			"type": "array",
			"default": [],
			"items":{
				"$id": "#root/phoneNumbers/items", 
				"title": "Items", 
				"type": "object",
				"required": [
					"value",
					"type"
				],
				"properties": {
					"value": {
						"$id": "#root/phoneNumbers/items/value", 
						"title": "Value", 
						"type": "string",
						"default": "",
						"examples": [
							"555-555-8377"
						],
						"pattern": "^.*$"
					},
					"type": {
						"$id": "#root/phoneNumbers/items/type", 
						"title": "Type", 
						"type": "string",
						"default": "",
						"examples": [
							"work"
						],
						"pattern": "^.*$"
					}
				}
			}

		},
		"emails": {
			"$id": "#root/emails", 
			"title": "Emails", 
			"type": "array",
			"default": [],
			"items":{
				"$id": "#root/emails/items", 
				"title": "Items", 
				"type": "object",
				"required": [
					"value",
					"type",
					"primary"
				],
				"properties": {
					"value": {
						"$id": "#root/emails/items/value", 
						"title": "Value", 
						"type": "string",
						"default": "",
						"examples": [
							"dschrute@example.com"
						],
						"pattern": "^.*$"
					},
					"type": {
						"$id": "#root/emails/items/type", 
						"title": "Type", 
						"type": "string",
						"default": "",
						"examples": [
							"work"
						],
						"pattern": "^.*$"
					},
					"primary": {
						"$id": "#root/emails/items/primary", 
						"title": "Primary", 
						"type": "boolean",
						"examples": [
							true
						],
						"default": true
					}
				}
			}

		}
	}
}

```

## Group
Group object
```json
{"sss":"444"}
```

Group Validation Schema
```
{"bbbb":"123"}
```

## References / Libraries
* JSON Validation Standard - https://github.com/json-schema-org
* SCIM v2 Standard - http://www.simplecloud.info/
