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












```

```sh
gem install json-schema
gem build json-schema.gemspec
gem install json-schema-2.5.2.gem
```

```
```


