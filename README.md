# Example for precompilation error with new requirejs-rails

This is a fresh rails-3.2.19 app created with command:
```bash
rails new . -O -J -T
```

## To reproduce error:
```bash
bundle install
rake assets:precompile
```

```
rake aborted!
TypeError: can't modify immutable index
/<ruby>/gems/sprockets-2.2.2/lib/sprockets/index.rb:80:in `expire_index!'
/<ruby>/gems/sprockets-2.2.2/lib/sprockets/processing.rb:259:in `js_compressor='
/<ruby>/bundler/gems/requirejs-rails-9d51ed8fffe9/lib/tasks/requirejs-rails_tasks.rake:100:in `block (3 levels) in <top (required)>'
Tasks: TOP => requirejs:precompile:all => requirejs:precompile:prepare_source
```
