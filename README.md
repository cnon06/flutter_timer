# timer

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

Timer class Null safety
A countdown timer that can be configured to fire once or repeatedly.

The timer counts down from the specified duration to 0. When the timer reaches 0, the timer invokes the specified callback function. Use a periodic timer to repeatedly count down the same interval.

A negative duration is treated the same as a duration of 0. If the duration is statically known to be 0, consider using run.

Frequently the duration is either a constant or computed as in the following example (taking advantage of the multiplication operator of the Duration class):

void main() {
  scheduleTimeout(5 * 1000); // 5 seconds.
}

Timer scheduleTimeout([int milliseconds = 10000]) =>
    Timer(Duration(milliseconds: milliseconds), handleTimeout);

void handleTimeout() {  // callback function
  // Do some work.
}
Note: If Dart code using Timer is compiled to JavaScript, the finest granularity available in the browser is 4 milliseconds.

See also:

Stopwatch for measuring elapsed time.
Implementers
FakeTimerRestartableTimer
Constructors
Timer(Duration duration, void callback())
Creates a new timer. [...]
factory
Timer.periodic(Duration duration, void callback(Timer timer))
Creates a new repeating timer. [...]
factory
Properties
hashCode → int
The hash code for this object. [...]
read-only, inherited
isActive → bool
Returns whether the timer is still active. [...]
read-only
runtimeType → Type
A representation of the runtime type of the object.
read-only, inherited
tick → int
The number of durations preceding the most recent timer event. [...]
read-only
Methods
cancel() → void
Cancels the timer. [...]
noSuchMethod(Invocation invocation) → dynamic
Invoked when a non-existent method or property is accessed. [...]
inherited
toString() → String
A string representation of this object. [...]
inherited
Operators
operator ==(Object other) → bool
The equality operator. [...]
inherited
Static Methods
run(void callback()) → void
Runs the given callback asynchronously as soon as possible. [...]
