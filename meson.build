project('xtd_test', 'cpp', version: '0.0.1', default_options: ['cpp_std=c++20'])

cmake = import('cmake')

xtd_subproj = cmake.subproject('xtd-0.1.1-beta')

xtd_dep = xtd_subproj.dependency('xtd')
deps = []
deps += xtd_dep

executable('xtd_test', 'main.cpp', dependencies: deps)
