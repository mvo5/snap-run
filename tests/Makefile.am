TESTS =

all_tests = \
    test_bad_seccomp_filter_args \
    test_bad_seccomp_filter_args_null \
    test_bad_seccomp_filter_args_prctl \
    test_bad_seccomp_filter_args_prio \
    test_bad_seccomp_filter_args_socket \
    test_bad_seccomp_filter_length \
    test_bad_seccomp_filter_missing_trailing_newline \
    test_complain \
    test_complain_missed \
    test_noprofile \
    test_restrictions \
    test_restrictions_working \
    test_restrictions_working_args \
    test_restrictions_working_args_prctl \
    test_restrictions_working_args_prio \
    test_restrictions_working_args_socket \
    test_unrestricted \
    test_unrestricted_missed \
    test_whitelist

EXTRA_DIST = $(all_tests) common.sh

if SECCOMP
if CONFINEMENT_TESTS
TESTS += $(all_tests)
endif
endif

check: ../src/snap-confine

.PHONY: check-syntax
check-syntax:
	shellcheck --format=gcc $(wildcard test_*) common.sh
