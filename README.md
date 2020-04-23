# About <a href="https://en.wikipedia.org/wiki/C%2B%2B11"><img align="right" src="https://img.shields.io/badge/C%2B%2B-17-00599C?logo=C%2B%2B" alt="C++ 17" /></a>
TimerH is a compact C++ library used for timing code and formatting time. It supports precision up to a nanosecond.

# License <a href="https://github.com/UnexomWid/timerh/blob/master/LICENSE"><img align="right" src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT" /></a>
TimerH was created by [UnexomWid](https://uw.exom.dev).
It is licensed under the [MIT](https://github.com/UnexomWid/timerh/blob/master/LICENSE) license.

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

| Name        | Value                                          |
|-------------|------------------------------------------------|
| CHRONOMETER | std::chrono::high_resolution_clock::time_point |

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
| format_time_ns(uint64_t)        | Formats a number representing nanoseconds as a string                  |
| format_time_mis(uint64_t)       | Formats a number representing microseconds as a string                 |
| format_time_ms(uint64_t)        | Formats a number representing milliseconds as a string                 |
| getf_exec_time_ns(CHRONOMETER)  | Gets the formatted execution time with the precision of a nanosecond   |
| getf_exec_time_mis(CHRONOMETER) | Gets the formatted execution time with the precision of a microsecond  |
| getf_exec_time_ms(CHRONOMETER)  | Gets the formatted execution time with the precision of a millisecond  |

