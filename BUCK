#include_defs('//BUCKAROO_DEPS')

cxx_library(
  name = 'capnproto',
  header_namespace = 'capnp',
  exported_headers = subdir_glob([
    ('c++/src/capnp', '**/*.h'),
  ],
  excludes = glob([
    'c++/src/capnp/**/test*.h',
  ])),
  srcs = glob([
    'c++/src/capnp/**/*.c++',
  ],
  excludes = glob([
    'c++/src/capnp/compiler/capnp.c++',
    'c++/src/capnp/compiler/capnpc-c++.c++',
    'c++/src/capnp/compiler/capnpc-capnp.c++',
    'c++/src/capnp/benchmark/**/*.c++',
    'c++/src/capnp/**/*test*.c++',
  ])),
  compiler_flags = [
    '-std=c++14',
    '-Wno-inconsistent-missing-override',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = [
    ':kj',
  ],
)

cxx_library(
  name = 'kj',
  header_namespace = 'kj',
  exported_headers = subdir_glob([
    ('c++/src/kj', '**/*.h'),
  ]),
  srcs = glob([
    'c++/src/kj/**/*.c++',
  ],
  excludes = glob([
    'c++/src/kj/compat/**/*.c++',
    'c++/src/kj/**/*test.c++',
  ])),
  compiler_flags = [
    '-std=c++14',
  ],
  visibility = [
    'PUBLIC',
  ],
)

cxx_binary(
  name = 'capnproto_bin',
  srcs = [
    'c++/src/capnp/compiler/capnp.c++',
    #'buckaroo/official/sandstorm/capnproto/c++/src/capnp/compiler/capnpc-c++.c++',
    #'buckaroo/official/sandstorm/capnproto/c++/src/capnp/compiler/capnpc-capnp.c++',
    #'buckaroo/official/sandstorm/capnproto/c++/src/capnp/benchmark/**/*.c++',
    #'buckaroo/official/sandstorm/capnproto/c++/src/capnp/**/*test*.c++',
  ],
  compiler_flags = [
    '-std=c++14',
    '-Wno-inconsistent-missing-override',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = [":capnproto"]
)

cxx_binary(
  name = 'capnproto_c++_bin',
  srcs = [
    'c++/src/capnp/compiler/capnpc-c++.c++',
    #'buckaroo/official/sandstorm/capnproto/c++/src/capnp/compiler/capnpc-capnp.c++',
    #'buckaroo/official/sandstorm/capnproto/c++/src/capnp/benchmark/**/*.c++',
    #'buckaroo/official/sandstorm/capnproto/c++/src/capnp/**/*test*.c++',
  ],
  compiler_flags = [
    '-std=c++14',
    '-Wno-inconsistent-missing-override',
  ],
  visibility = [
    'PUBLIC',
  ],
  deps = [":capnproto"]
)

