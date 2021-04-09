## CircuitPython Schedule

The CircuitPython_Schedule module is based on the excellent [schedule](https://pypi.org/project/schedule/) CPython module by [Dan Bader](https://pypi.org/user/dbader/), modified for CircuitPython by [Nathan Byrd](https://github.com/cognitivegears).  This open-source module facilitates the execution of functions on fixed time schedules. This is particularly useful in CircuitPython for use cases involving time-based activities; some activities could include watering plants, turning on/off lights, periodically logging data or sending reminders, among many others. The library uses a Domain Specific Language (DSL) to allow for flexible scheduling options at execution time.

### Example

```python
import time
import circuitpython_schedule as schedule


def greet():
    print("Hello, world!")


# Note: pass functions, not function calls - i.e. "greet", not "greet()"

# schedule every 10 seconds
schedule.every(10).seconds.do(greet)

# schedule every 10 minutes
schedule.every(10).minutes.do(greet)

# schedule once a day
schedule.every().day.at("10:30").do(greet)

# schedule from 5 to 10 minutes
schedule.every(5).to(10).minutes.do(greet)

# schedule on a particular day
schedule.every().monday.do(greet)

# schedule day and time
schedule.every().wednesday.at("13:15").do(greet)

# schedule once a minute at seventeen seconds
schedule.every().minute.at(":17").do(greet)


while True:
    # Run any pending jobs
    schedule.run_pending()
    time.sleep(1)
````

### Installation

CircuitPython_Schedule is part of the [Adafruit CircuitPython Community Bundle](https://github.com/adafruit/CircuitPython_Community_Bundle). It is located in the bundle at `libraries/helpers/schedule`. For instructions on how to install a library in CircuitPython, see [CircuitPython Libraries](https://learn.adafruit.com/welcome-to-circuitpython/circuitpython-libraries)



### More Information

* [CircuitPython-Schedule on PyPi](https://pypi.org/project/circuitpython-schedule/)
* [CircuitPython-Schedule GitHub page](https://github.com/cognitivegears/CircuitPython_Schedule)

### Documentation

For full information on using the library, see the [Documentation at ReadTheDocs](https://circuitpython-schedule.readthedocs.io/en/latest/)

### Contributing

Contributions are always welcome. Feel free to open an [Issue](https://github.com/cognitivegears/CircuitPython_Schedule/issues) or create a [Pull Request](https://github.com/cognitivegears/CircuitPython_Schedule/pulls) with any changes. All code (original and CircuitPython version) are under the [MIT license](https://github.com/cognitivegears/CircuitPython_Schedule/blob/main/LICENSE).
