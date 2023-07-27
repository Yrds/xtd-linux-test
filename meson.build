project('xtd_test', 'cpp', version: '0.0.1', default_options : ['cpp_std=c++20'])

cmake = import('cmake')

xtd_opt_var = cmake.subproject_options()

xtd_opt_var.add_cmake_defines( {
  'XTD_BUILD_TOOL_XTDC_COMMAND_LINE': 'OFF',
  'XTD_BUILD_TOOL_XTDC_GUI': 'OFF',
  'CMAKE_CXX_STANDARD': '20',
  'CMAKE_CXX_STANDARD_REQUIRED': 'ON'
  })

xtd_subproj = cmake.subproject('xtd-0.1.1-beta', options: xtd_opt_var)

xtd_dep = xtd_subproj.dependency('xtd')
#xtd_dep = dependency('xtd')

wx_dep = dependency(
  'wxwidgets', version : '>=3.0.0', modules : ['std', 'stc'],
)

deps = []

deps += wx_dep
deps += xtd_dep


executable('xtd_test', 'main.cpp', dependencies: deps)
