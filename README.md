{
  "description": "A collection of reusable JSON schema snippets for faster data validation.",
  "schemas": {
    "positiveInteger": {
      "type": "integer",
      "minimum": 1,
      "description": "A positive integer."
    },
    "nonNegativeInteger": {
      "type": "integer",
      "minimum": 0,
      "description": "A non-negative integer."
    },
    "stringNotEmpty": {
      "type": "string",
      "minLength": 1,
      "description": "A non-empty string."
    },
    "email": {
      "type": "string",
      "format": "email",
      "description": "A valid email address."
    },
    "uuid": {
      "type": "string",
      "format": "uuid",
      "description": "A universally unique identifier (UUID)."
    },
    "dateISO": {
      "type": "string",
      "format": "date",
      "description": "A date in ISO 8601 format (YYYY-MM-DD)."
    },
    "dateTimeISO": {
      "type": "string",
      "format": "date-time",
      "description": "A date and time in ISO 8601 format (YYYY-MM-DDTHH:mm:ssZ)."
    },
    "phoneNumber": {
      "type": "string",
      "pattern": "^\\+?[1-9]\\d{1,14}$",
      "description": "An international phone number (basic format)."
    },
    "boolean": {
      "type": "boolean",
      "description": "A boolean value (true or false)."
    },
    "arrayNotEmpty": {
      "type": "array",
      "minItems": 1,
      "description": "A non-empty array."
    },
    "arrayOfPositiveIntegers": {
      "type": "array",
      "items": {
        "$ref": "#/schemas/positiveInteger"
      },
      "description": "An array of positive integers."
    },
    "objectWithId": {
      "type": "object",
      "properties": {
        "id": {
          "$ref": "#/schemas/positiveInteger"
        }
      },
      "required": [
        "id"
      ],
      "description": "An object that must have an 'id' which is a positive integer."
    }
  },
  "usage": "Reference these schema definitions using the '$ref' keyword in your JSON Schema validation rules. For example: {\"type\": \"string\", \"$ref\": \"#/schemas/email\"}"
}
