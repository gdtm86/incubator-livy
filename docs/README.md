<!--
{% comment %}
Licensed to the Apache Software Foundation (ASF) under one or more
contributor license agreements.  See the NOTICE file distributed with
this work for additional information regarding copyright ownership.
The ASF licenses this file to you under the Apache License, Version 2.0
(the "License"); you may not use this file except in compliance with
the License.  You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
{% endcomment %}
-->

# Apache Livy Documentation

This documentation is generated using [Jekyll](https://jekyllrb.com/).

# How to deploy the documentation

## Installing Jekyll and dependencies

The steps below will install the latest [Jekyll](https://jekyllrb.com/) version
and any dependencies required to get this documentation built.

```
1. sudo gem install jekyll bundler
2. cd docs
3. sudo bundle install
```

For more information, see [Installing Jekyll](https://jekyllrb.com/docs/installation/).

## Running locally

Before opening a pull request, you can preview your contributions by running from within the directory:

```
1. cd docs
2. bundle exec jekyll serve --watch
3. Open http://localhost:4000
```

## Publishing Docs to [livy.incubator.apache.org]

1. Build Livy Docs (`cd docs` then `bundle exec jekyll build`).
2. Copy the contents of `docs/target/` excluding `assets/` into a new directory (eg. `0.4.0/`) and
move it into the `docs/` directory in your local fork of `apache/incubator-livy-website`.
3. If this is a major version, update the `latest` symlink to point to the new directory.
4. Open a pull request to `apache/incubator-livy-website` with the update.

Note: If you made any changes to files in the `assets/` directory you will need to replicate those
changes in the corresponding files in `apache/incubator-livy-website` in the pull request.