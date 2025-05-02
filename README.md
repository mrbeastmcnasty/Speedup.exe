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