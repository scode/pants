# Copyright 2015 Pants project contributors (see CONTRIBUTORS.md).
# Licensed under the Apache License, Version 2.0 (see LICENSE).

python_library(
  name = 'jvm_tool_mixin',
  sources = ['jvm_tool_mixin.py'],
  dependencies = [
    'src/python/pants/base:address_lookup_error',
    'src/python/pants/base:exceptions',
  ],
)

python_library(
  name = 'jar_tool',
  sources = ['jar_tool.py'],
  dependencies = [
    ':jvm_tool_mixin',
    'src/python/pants/backend/jvm/targets:jvm',
    'src/python/pants/base:workunit',
    'src/python/pants/option',
    'src/python/pants/subsystem',
  ],
)

python_library(
  name = 'jvm',
  sources = ['jvm.py'],
  dependencies = [
    'src/python/pants/option',
    'src/python/pants/subsystem',
    'src/python/pants/util:strutil',
  ],
)

python_library(
  name = 'jvm_platform',
  sources = ['jvm_platform.py'],
  dependencies = [
    'src/python/pants/base:revision',
    'src/python/pants/option',
    'src/python/pants/subsystem',
    'src/python/pants/util:memo',
    'src/python/pants/java/distribution',
  ],
)

python_library(
  name = 'scala_platform',
  sources = ['scala_platform.py'],
  dependencies = [
    ':jvm_tool_mixin',
    'src/python/pants/option',
    'src/python/pants/subsystem',
  ],
)

python_library(
  name = 'shader',
  sources = ['shader.py'],
  dependencies = [
    'src/python/pants/backend/jvm/targets:jvm',
    'src/python/pants/backend/jvm/tasks:jvm_tool_task_mixin',
    'src/python/pants/java/distribution',
    'src/python/pants/java:executor',
    'src/python/pants/subsystem',
    'src/python/pants/util:contextutil',
  ]
)
