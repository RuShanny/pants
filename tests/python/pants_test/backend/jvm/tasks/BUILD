# Copyright 2014 Pants project contributors (see CONTRIBUTORS.md).
# Licensed under the Apache License, Version 2.0 (see LICENSE).

target(
  name = 'tasks',
  dependencies = [
    ':checkstyle',
    ':ide_gen',
    ':idea_gen',
    ':ivy_imports',
    ':junit_run',
    ':scalastyle',
    ':unpack_jars',
    'tests/python/pants_test/backend/jvm/tasks/jvm_compile',
  ]
)

python_tests(
  name = 'checkstyle',
  sources = ['test_checkstyle.py'],
  dependencies = [
    'src/python/pants/backend/jvm/tasks:checkstyle',
    'src/python/pants/base:address',
    'src/python/pants/base:exceptions',
    'tests/python/pants_test/jvm:nailgun_task_test_base',
  ]
)

python_tests(
  name = 'ide_gen',
  sources = ['test_ide_gen.py'],
  dependencies = [
    'src/python/pants/backend/jvm/tasks:ide_gen',
    'src/python/pants/backend/jvm/targets:java',
    'src/python/pants/base:source_root',
    'tests/python/pants_test:base_test',
  ]
)

python_tests(
  name = 'idea_gen',
  sources = ['test_idea_gen.py'],
  dependencies = [
    'src/python/pants/backend/core/targets:common',
    'src/python/pants/backend/jvm/tasks:ide_gen',
    'src/python/pants/backend/jvm/tasks:idea_gen',
    'src/python/pants/backend/jvm/targets:java',
    'src/python/pants/base:source_root',
    'tests/python/pants_test:base_test',
  ]
)


python_tests(
  name = 'ivy_imports',
  sources = ['test_ivy_imports.py'],
  dependencies = [
    'src/python/pants/backend/core/targets:common',
    'src/python/pants/backend/jvm/targets:jvm',
    'src/python/pants/backend/jvm/tasks:ivy_imports',
    'src/python/pants/base:build_file_aliases',
    'src/python/pants/util:contextutil',
    'tests/python/pants_test/tasks:base'
  ]
)

python_tests(
  name = 'junit_run',
  sources = ['test_junit_run.py'],
  dependencies = [
    'src/python/pants/backend/core/targets:common',
    'src/python/pants/backend/jvm/tasks:junit_run',
    'src/python/pants/goal:products',
    'src/python/pants/ivy',
    'src/python/pants/java:distribution',
    'src/python/pants/java:executor',
    'tests/python/pants_test/jvm:jvm_tool_task_test_base',
  ]
)

python_tests(
  name = 'scalastyle',
  sources = ['test_scalastyle.py'],
  dependencies = [
    'src/python/pants/backend/jvm/targets:scala',
    'src/python/pants/backend/jvm/tasks:scalastyle',
    'src/python/pants/base:address',
    'src/python/pants/base:config',
    'src/python/pants/base:exceptions',
    'tests/python/pants_test/jvm:nailgun_task_test_base',
  ]
)

python_tests(
  name = 'ivy_resolve',
  sources = ['test_ivy_resolve.py'],
  dependencies = [
    'src/python/pants/backend/jvm/targets:jvm',
    'src/python/pants/backend/jvm/targets:scala',
    'src/python/pants/backend/jvm/tasks:ivy_resolve',
    'tests/python/pants_test/jvm:nailgun_task_test_base',
  ]
)

python_tests(
  name = 'unpack_jars',
  sources = ['test_unpack_jars.py'],
  dependencies = [
    'src/python/pants/backend/core/targets:common',
    'src/python/pants/backend/jvm/targets:jvm',
    'src/python/pants/backend/jvm/tasks:unpack_jars',
    'src/python/pants/base:target',
    'tests/python/pants_test:base_test',
    'tests/python/pants_test/tasks:base'
    ]
)
