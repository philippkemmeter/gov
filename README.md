# gov

Simple command line tool to manage the cpu scaling govenors of your system.
Well suited to be used in other scripts e.g. for acpi button binding.

## Synopsis

    Usage: gov [OPTIONS] [GOVERNOR]

    Changes the scaling governor of the cpus.

    Available Options:
      -c,--cpu CPUID If this option is set, the scaling of the
                     cpu of this ID will be changed. Possible values are {0,..n-1}
                     where n is the amount of the CPUs of your machine. Omit this
                     option to affect all CPUs.
      -h,--help      Shows this help


## Examples

    # Switch to powersave for CPU 0
    gov -c 0 powersave

    # Echos the current active governor for CPU 1
    gov --cpu 1

    # Switch to performance for all CPUs
    gov performance

    # Echos the current active governor for all CPUs
    gov --cpu 1

## Requirements

This tools read its information from `/sys`, so this feature has to be enabled
in kernel.
