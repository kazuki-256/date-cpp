# object date (c++)

to handle date by smart object in c++


```cpp
#include "date.hpp"

int main(int argc, char** argv) {
	date_t date("2026-01-21 16:00:00");
	std::cout << date << std::endl;

	date = date_t("2026/01/21 16:00", "%Y/%m/%d %H:%M");	// parse date string by customize format

	date += interval_t("3 year 1 month 4 day 1 hour 5 min 9 sec");	// moving date/time
	std::cout << date << std::endl;

	date += interval_t("2 week");	// just 2*7 = 14 days
	std::cout << date << std::endl;
}
```
