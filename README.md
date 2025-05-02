Using the following firj should allow all issues or bugs with slow schemas or just want faster ones. 




{
  "type": "object",
  "properties": {
    "userId": {
      "$ref": "#/schemas/positiveInteger"
    },
    "email": {
      "$ref": "#/schemas/email"
    },
    "createdAt": {
      "$ref": "#/schemas/dateTimeISO"
    }
  },
  "required": ["userId", "email", "createdAt"]
}