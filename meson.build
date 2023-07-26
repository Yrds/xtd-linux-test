project('xtd_test', 'cpp', version: '0.0.1', default_options: ['cpp_std=c++20'])

cmake = import('cmake')

xtd_opt_var = cmake.subproject_options()

xtd_opt_var.add_cmake_defines( {
  'XTD_BUILD_TOOL_XTDC_COMMAND_LINE': 'OFF',
  'XTD_BUILD_TOOL_XTDC_GUI': 'OFF'
  })

xtd_subproj = cmake.subproject('xtd-0.1.1-beta', options: xtd_opt_var)
message('CMake targets:\n - ' + '\n - '.join(xtd_subproj.target_list()))


xtd_dep = xtd_subproj.dependency('xtd')
deps = []
deps += xtd_dep

executable('xtd_test', 'main.cpp', dependencies: deps)
