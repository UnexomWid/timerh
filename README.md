# About
TimerH is a compact C++ library used for timing code and formatting time. It supports precision up to a nanosecond.

# License
TimerH was created by [UnexomWid](http://unexomwid.me).
It is licensed under the [GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html) license.

# Usage

```cpp
CHRONOMETER ch;
ch = time_now();
/*
 Code to time.
*/
std::cout << "Execution Time: " << get_exec_time_ms(ch) << " ms";
std::cout << "\nExecution Time (formatted): " << getf_exec_time_ms(ch);
```

Example of output:

```
Execution Time: 1 ms
Execution Time (formatted): 1 millisecond, 14 microseconds, 695 nanoseconds
```

## Definitions

| Name        | Value                                 |
|-------------|---------------------------------------|
| CHRONOMETER | std::chrono::steady_clock::time_point |
| ULL         | unsigned long long                    |

## Functions


| Function                        | Description                                                            |
|---------------------------------|------------------------------------------------------------------------|
| time_now()                      | Gets the current time, as a CHRONOMETER object                         |
| get_exec_time_ns(CHRONOMETER)   | Gets the execution time in nanoseconds                                 |
| get_exec_time_mis(CHRONOMETER)  | Gets the execution time in microseconds                                |
| get_exec_time_ms(CHRONOMETER)   | Gets the execution time in milliseconds                                |
| get_exec_time_s(CHRONOMETER)    | Gets the execution time in seconds                                     |
| get_exec_time_m(CHRONOMETER)    | Gets the execution time in minutes                                     |
| get_exec_time_h(CHRONOMETER)    | Gets the execution time in hours                                       |
| format_time_ns(ULL)             | Formats a number representing nanoseconds as a string                  |
| format_time_mis(ULL)            | Formats a number representing microseconds as a string                 |
| format_time_ms(ULL)             | Formats a number representing milliseconds as a string                 |
| getf_exec_time_ns(CHRONOMETER)  | Gets the formatted execution time with the precision of a nanosecond   |
| getf_exec_time_mis(CHRONOMETER) | Gets the formatted execution time with the precision of a microsecond  |
| getf_exec_time_ms(CHRONOMETER)  | Gets the formatted execution time with the precision of a millisecond  |

