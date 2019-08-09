### json-schema
---
.rb
https://github.com/ruby-json-schema/json-schema

http://json-schema.org/

```rb
require "json-schma"

schema = {
  "type" => "object",
  "required" = ["a"],
  "properties" => {
    "a" => {"type" => "integer"}
  }
}

JSON::Validator.validate(schema, { "a" => 5 })
JSON::Validator.validate(schema, {})

require "json"
File.write("schema.json", JSON.dump(schema))

JSON::Validator.validate('schema.json', '{ "a": 5 }')

begin
  JSON::Validator.vlidate!(schema, { "a" => "taco" })
rescue JSON::Schema::ValidationError => e
  e.message
end


require "json-schema"

schema = {
  "type"=>"object",
  "required" => ["a"],
  "properties" => {
    "a" => {
      "type" => "integer",
      "default" => 42
    },
    "b" => {
      "type" => "object",
      "properrties" => {
        "x" => {
          "type" => "integer"
        }
      }
    }
  }
}
JSON::Validator.validate(schema, [{"a" => 1}, {"a" => 2}, {"a" => 3}], :list => true)
JSON::Validator.validate(schema, [{}])

```

```sh
gem install json-schema
gem build json-schema.gemspec
gem install json-schema-2.5.2.gem
```

```
```


