# ISO8601
Parse ISO8601 duration strings, and use to shift dates/times.

### Basic Example

	package main

	import (
		"fmt"
		"time"

		"github.com/senseyeio/iso8601"
	)

	func main() {
		d, _ := iso8601.ParseDuration("P1D")
		today := time.Now()
		tomorrow := d.Shift(today)
		fmt.Println(today.Format("Jan _2"))
		fmt.Println(tomorrow.Format("Jan _2"))
	}

