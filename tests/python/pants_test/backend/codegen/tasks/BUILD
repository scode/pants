# Copyright 2014 Pants project contributors (see CONTRIBUTORS.md).
# Licensed under the Apache License, Version 2.0 (see LICENSE).

target(
  name = 'tasks',
  dependencies = [
    ':antlr_gen',
    ':apache_thrift_gen',
    ':jaxb_gen',
    ':protobuf_gen',
    ':protobuf_parse',
    ':ragel_gen',
    ':simple_codegen_task',
    ':wire_gen',
  ],
)

python_tests(
  name = 'apache_thrift_gen',
  sources = ['test_apache_thrift_gen.py'],
  dependencies = [
    'src/python/pants/backend/codegen/targets:java',
    'src/python/pants/backend/codegen/tasks:apache_thrift_gen',
    'src/python/pants/backend/jvm/targets:java',
    'src/python/pants/base:source_root',
    'tests/python/pants_test/tasks:task_test_base',
  ],
)

python_tests(
  name = 'antlr_gen',
  sources = ['test_antlr_gen.py'],
  dependencies = [
    '3rdparty/python/twitter/commons:twitter.common.dirutil',
    'src/python/pants/backend/codegen/targets:java',
    'src/python/pants/backend/codegen/tasks:antlr_gen',
    'src/python/pants/base:build_file_aliases',
    'src/python/pants/base:exceptions',
    'src/python/pants/base:source_root',
    'tests/python/pants_test/jvm:nailgun_task_test_base',
  ],
)

python_tests(
  name = 'jaxb_gen',
  sources = ['test_jaxb_gen.py'],
  dependencies = [
    'src/python/pants/backend/codegen/tasks:jaxb_gen',
    'src/python/pants/backend/codegen/targets:java',
    'src/python/pants/backend/core:plugin',
    'src/python/pants/util:contextutil',
    'tests/python/pants_test/tasks:task_test_base',
  ],
)

python_tests(
  name = 'protobuf_gen',
  sources = ['test_protobuf_gen.py'],
  dependencies = [
    'src/python/pants/backend/codegen/tasks:protobuf_gen',
    'src/python/pants/backend/codegen:plugin',
    'src/python/pants/backend/core:plugin',
    'src/python/pants/util:contextutil',
    'tests/python/pants_test/tasks:task_test_base',
  ],
)

python_tests(
  name = 'protobuf_parse',
  sources = ['test_protobuf_parse.py'],
  dependencies = [
    'src/python/pants/backend/codegen/tasks:protobuf_parse',
    'src/python/pants/util:contextutil',
  ],
)

python_tests(
  name = 'ragel_gen',
  sources = ['test_ragel_gen.py'],
  dependencies = [
    'src/python/pants/backend/codegen/targets:java',
    'src/python/pants/backend/codegen/tasks:ragel_gen',
    'src/python/pants/util:contextutil',
    'tests/python/pants_test/tasks:task_test_base',
  ],
)

python_tests(
  name = 'simple_codegen_task',
  sources = ['test_simple_codegen_task.py'],
  dependencies = [
    'src/python/pants/backend/codegen/targets:java',
    'src/python/pants/backend/codegen/tasks:simple_codegen_task',
    'src/python/pants/backend/codegen:plugin',
    'src/python/pants/backend/core:plugin',
    'src/python/pants/util:contextutil',
    'tests/python/pants_test/tasks:task_test_base',
  ],
)

python_tests(
  name = 'wire_gen',
  sources = ['test_wire_gen.py'],
  dependencies = [
    '3rdparty/python/twitter/commons:twitter.common.collections',
    'src/python/pants/backend/codegen/tasks:wire_gen',
    'src/python/pants/backend/codegen:plugin',
    'src/python/pants/backend/core:plugin',
    'src/python/pants/backend/jvm/targets:jvm',
    'src/python/pants/base:exceptions',
    'src/python/pants/base:revision',
    'src/python/pants/base:source_root',
    'src/python/pants/base:target',
    'src/python/pants/base:validation',
    'src/python/pants/util:contextutil',
    'tests/python/pants_test/tasks:task_test_base',
  ],
)

python_tests(
  name = 'wire_integration',
  sources = ['test_wire_integration.py'],
  dependencies = [
    'src/python/pants/base:build_environment',
    'tests/python/pants_test:int-test',
  ],
)
