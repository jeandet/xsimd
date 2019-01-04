project('xsimd', 'cpp', version:'7.1.2', license:'BSD-3-Clause', default_options : ['warning_level=3', 'cpp_std=c++14'])

xsim_dependencies = []
xsimd_cpp_arg = []

if get_option('ENABLE_XTL_COMPLEX')
  xsim_dependencies+=[dependency('xtl', version:'>=0.4.11')]
  xsimd_cpp_arg = ['-DXSIMD_ENABLE_XTL_COMPLEX']
endif

xsimd_dep = declare_dependency(include_directories:include_directories('include'), dependencies:xsim_dependencies, compile_args:xsimd_cpp_arg)

install_headers([
 'include/xsimd/config/xsimd_config.hpp',
 'include/xsimd/config/xsimd_include.hpp',
 'include/xsimd/config/xsimd_instruction_set.hpp',
 'include/xsimd/config/xsimd_align.hpp',
 'include/xsimd/math/xsimd_fp_sign.hpp',
 'include/xsimd/math/xsimd_invtrigo.hpp',
 'include/xsimd/math/xsimd_rem_pio2.hpp',
 'include/xsimd/math/xsimd_horner.hpp',
 'include/xsimd/math/xsimd_numerical_constant.hpp',
 'include/xsimd/math/xsimd_fp_manipulation.hpp',
 'include/xsimd/math/xsimd_power.hpp',
 'include/xsimd/math/xsimd_hyperbolic.hpp',
 'include/xsimd/math/xsimd_scalar.hpp',
 'include/xsimd/math/xsimd_basic_math.hpp',
 'include/xsimd/math/xsimd_math_complex.hpp',
 'include/xsimd/math/xsimd_rounding.hpp',
 'include/xsimd/math/xsimd_logarithm.hpp',
 'include/xsimd/math/xsimd_trigo_reduction.hpp',
 'include/xsimd/math/xsimd_trigonometric.hpp',
 'include/xsimd/math/xsimd_error.hpp',
 'include/xsimd/math/xsimd_exponential.hpp',
 'include/xsimd/math/xsimd_math.hpp',
 'include/xsimd/math/xsimd_gamma.hpp',
 'include/xsimd/math/xsimd_exp_reduction.hpp',
 'include/xsimd/memory/xsimd_aligned_stack_buffer.hpp',
 'include/xsimd/memory/xsimd_load_store.hpp',
 'include/xsimd/memory/xsimd_aligned_allocator.hpp',
 'include/xsimd/memory/xsimd_alignment.hpp',
 'include/xsimd/stl/algorithms.hpp',
 'include/xsimd/xsimd.hpp',
 'include/xsimd/types/xsimd_neon_uint32.hpp',
 'include/xsimd/types/xsimd_avx512_int_base.hpp',
 'include/xsimd/types/xsimd_neon_bool.hpp',
 'include/xsimd/types/xsimd_avx_int64.hpp',
 'include/xsimd/types/xsimd_neon_int32.hpp',
 'include/xsimd/types/xsimd_neon_int8.hpp',
 'include/xsimd/types/xsimd_sse_int16.hpp',
 'include/xsimd/types/xsimd_neon_int64.hpp',
 'include/xsimd/types/xsimd_sse_int32.hpp',
 'include/xsimd/types/xsimd_neon_uint8.hpp',
 'include/xsimd/types/xsimd_avx512_int8.hpp',
 'include/xsimd/types/xsimd_avx512_float.hpp',
 'include/xsimd/types/xsimd_int_conversion.hpp',
 'include/xsimd/types/xsimd_neon_uint64.hpp',
 'include/xsimd/types/xsimd_sse_int64.hpp',
 'include/xsimd/types/xsimd_neon_complex.hpp',
 'include/xsimd/types/xsimd_neon_uint16.hpp',
 'include/xsimd/types/xsimd_traits.hpp',
 'include/xsimd/types/xsimd_sse_float.hpp',
 'include/xsimd/types/xsimd_neon_conversion.hpp',
 'include/xsimd/types/xsimd_fallback.hpp',
 'include/xsimd/types/xsimd_avx512_complex.hpp',
 'include/xsimd/types/xsimd_avx_double.hpp',
 'include/xsimd/types/xsimd_avx_float.hpp',
 'include/xsimd/types/xsimd_complex_base.hpp',
 'include/xsimd/types/xsimd_utils.hpp',
 'include/xsimd/types/xsimd_avx512_int32.hpp',
 'include/xsimd/types/xsimd_avx512_int64.hpp',
 'include/xsimd/types/xsimd_avx512_conversion.hpp',
 'include/xsimd/types/xsimd_sse_double.hpp',
 'include/xsimd/types/xsimd_sse_complex.hpp',
 'include/xsimd/types/xsimd_neon_utils.hpp',
 'include/xsimd/types/xsimd_avx512_bool.hpp',
 'include/xsimd/types/xsimd_avx_int8.hpp',
 'include/xsimd/types/xsimd_avx_conversion.hpp',
 'include/xsimd/types/xsimd_sse_int8.hpp',
 'include/xsimd/types/xsimd_neon_float.hpp',
 'include/xsimd/types/xsimd_neon_double.hpp',
 'include/xsimd/types/xsimd_base.hpp',
 'include/xsimd/types/xsimd_avx512_int16.hpp',
 'include/xsimd/types/xsimd_avx_int32.hpp',
 'include/xsimd/types/xsimd_avx_int_base.hpp',
 'include/xsimd/types/xsimd_avx_int16.hpp',
 'include/xsimd/types/xsimd_sse_conversion.hpp',
 'include/xsimd/types/xsimd_avx_complex.hpp',
 'include/xsimd/types/xsimd_neon_int16.hpp',
 'include/xsimd/types/xsimd_sse_int_base.hpp',
 'include/xsimd/types/xsimd_avx512_double.hpp',
 'include/xsimd/types/xsimd_types_include.hpp'],
 subdir:'xsimd'
)


tests_sources = [
 'test/main.cpp',
 'test/xsimd_algorithms.cpp',
 'test/xsimd_api_test.cpp',
 'test/xsimd_basic_math_test.cpp',
 'test/xsimd_basic_test.cpp',
 'test/xsimd_cexponential_test.cpp',
 'test/xsimd_chyperbolic_test.cpp',
 'test/xsimd_cpower_test.cpp',
 'test/xsimd_ctrigonometric_test.cpp',
 'test/xsimd_error_gamma_test.cpp',
 'test/xsimd_exponential_test.cpp',
 'test/xsimd_fp_manipulation_test.cpp',
 'test/xsimd_hyperbolic_test.cpp',
 'test/xsimd_interface_test.cpp',
 'test/xsimd_memory_test.cpp',
 'test/xsimd_power_test.cpp',
 'test/xsimd_rounding_test.cpp',
 'test/xsimd_trigonometric_test.cpp'
 ]

if get_option('BUILD_TESTS')
  cpp_args = []
  if get_option('ENABLE_FALLBACK')
     cpp_args+=['-DXSIMD_ENABLE_FALLBACK=1']
  endif
  gtest_dep = dependency('gtest', main : true, fallback : ['gtest', 'gtest_dep'])
  test_exe = executable('xsimd-test', tests_sources, dependencies:[xsimd_dep, gtest_dep], cpp_args:cpp_args)
  test('xsimd-test', test_exe)

  benchmark_exe = executable('xsimd-benchmark', 'benchmark/main.cpp', dependencies:[xsimd_dep], cpp_args:cpp_args)
  benchmark('xsimd-benchmark', benchmark_exe, timeout:3600)
endif
