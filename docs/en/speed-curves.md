[🇩🇪 Deutsch](../gaskurven.md) | [🇬🇧 English](../en/speed-curves.md)
# What are throttle curves and what can I do with them?

A user experience report by [go-digital-132](https://www.carrera-go.info/index.php?user/8085-go-digital-132/) from the carrera-go forum. Many thanks for sharing this!

---

## 1. What do throttle curves do?

Throttle curves allow you to control how much throttle (= voltage) is delivered by the decoder to the car.

Technically, this works as follows: Depending on the position of the controller trigger, the controller sends one of fifteen throttle values to the CU (Control Unit). From there, the command is forwarded to the decoder of the respective car, instructing it to increase or decrease the voltage supplied to the motor. This makes the car go faster or slower.

Throttle curves allow you to define exactly how much throttle (= voltage) should reach the car.

There are fifteen throttle points in total, which together form the curve. A value of 0 means "motor off", while a value of 255 means "full throttle". Values in between represent corresponding throttle levels.

## 2. Why is this important?

Throttle curves allow you to achieve many things according to your personal preferences:

- **Unlocking the technically possible maximum speed of a D143 car.** This is not possible with the original Carrera decoder firmware, which limits the cars to approximately 80% of their maximum possible performance, even though the cars can handle full throttle.

- **Conversely, full throttle can also be limited.** This is useful, for example, when using cars that become difficult to control at high speeds due to their design (cars with a high center of gravity or cars without magnets). It is also useful when racing with children who have not yet developed the feel for controlling a car at the limits of physics.

- **Improved throttle control according to personal preferences.** Some drivers prefer a controller that initially increases the throttle only slightly, but then reaches full throttle more quickly towards the end. Others prefer the opposite: reaching a medium speed quickly and then being able to adjust the throttle very precisely at the upper end of the range. Some drivers set the lower throttle points to relatively high values right from the start. After all, what is the point of having power delivered to the car at the lowest controller setting if the car is moving so slowly that it cannot even make it through the next lane changer?

- **Influencing how much the car slows down when using a Carrera D132 CU with one of the two fuel modes enabled.** Carrera has implemented this very elegantly: When the CU detects that a car has run out of fuel, the maximum speed of that car is limited to the tenth of the fifteen throttle points. Even if the controller trigger is pulled all the way, the car will never receive more throttle than it would at the tenth controller position.

  You can therefore design a throttle curve so that the reduction in speed is barely noticeable (higher values close to 255), or so that the car slows down very noticeably (values around 130).

  The latter is particularly interesting for drivers who cannot or do not want to keep an eye on Driver Displays, screens, tablets or smartphones all the time. The reduced speed immediately indicates that the car has run out of fuel.

## 3. How can I use throttle curves with flash143plus?

By default, flash143plus comes with five predefined throttle curves, which are available after installation:

- Kind 1
- Kind 2
- Kind 3
- Full Throttle 1
- Full Throttle 2

Each curve contains its own set of throttle values:

- The "Kind 3" curve, for example, ranges from a throttle value of 38 to 179. This is a throttle curve that deliberately limits full throttle, restricting the cars to approximately 70% of their technically possible maximum speed. "Kind 2" and "Kind 1" limit the maximum speed even further, making them perfect for the very first driving experiences of younger children.

- The "Full Throttle 1" curve unlocks full speed in such a way that relatively little additional throttle is applied at low and medium controller positions. Towards the end, when you pull the controller trigger all the way, a substantial extra "boost" kicks in. It's a bit like turbo lag at first, followed by a powerful burst of acceleration once the turbo has enough air to breathe! 😊

- The "Full Throttle 2" curve also unlocks full speed, but increases the throttle linearly with every additional movement of the controller trigger. It's more like an electric car, where a constant amount of torque accelerates the car smoothly, almost as if it were being pulled along by a rubber band.

- As mentioned above, the tenth point of the throttle curve (called P10) is particularly important. This is the maximum speed available when using one of the two fuel modes of the D132 CU and the fuel tank has run empty.

  You can therefore design the curve to provide exactly the maximum speed you consider appropriate when the tank is empty. For example, you can make it very clear that an empty car needs to return to the pits, without immediately turning it into a potential cause of accidents because it has become too slow.

The buttons are clearly labelled and do exactly what their names suggest. Not all buttons are active in the demo version.

**Draw Curve.** To draw a curve, first select the desired curve by clicking on one of the coloured curve fields. Then move the mouse pointer into the graph window and click the left mouse button to set the corresponding position. Repeat this for each of the 15 speed values. The mouse wheel can be used to fine-tune the values.

**Save Curve.** This saves the currently active curve to the Motor Curve Database after you have entered a name.

**Assign Curve.** In the Motor Curve Database, saved curves can be assigned to a curve slot or deleted using the right mouse button.

**Flash Curves.** Clicking "Flash Curves" transfers all curves currently displayed in the graph window to the controller.

## 4. What might the future bring?

Future flash143plus updates might introduce new features that make use of the throttle curve functionality, for example:

- An option that gradually slows a car down even before the tank is completely empty, warning the driver that fuel is running low and giving them enough time to reach the pits before laps are no longer counted.

- A hardcore mode in which the car stops abruptly when the tank is empty, immediately eliminating the affected driver from the race, just like in real racing.

- Randomly simulated car damage, for example through irregular engine sputtering, forcing the driver to return to the pits for repairs.

But even without any future features, throttle curves are already extremely powerful and allow every D143 driver to influence the driving behaviour of their cars.

**Would you like to see an example?**

The screenshot below shows the five included throttle curves in the Motor Curve Database, plus an additional curve ("Full Throttle 3") optimized for use with one of the fuel modes of the D132 CU.

When an empty tank is detected, the cars are limited to approximately half their maximum performance. This is fast enough to avoid immediate accidents caused by the sudden reduction in speed and to allow cars to pass lane changers reliably while running on an empty tank.

However, it is also slow enough to provide the driver with some wonderful moments of frustration until they finally make it back to the pit lane!

This curve also starts at a throttle value of 56, since lower values are not really practical on the corresponding track, "Bitzenheimer Berg".

![The five included throttle curves and the additional "Full Throttle 3" curve](../images/godigital132_bild1.png)

<!-- Note: The original image must be stored in the repository under docs/images/godigital132_bild1.png. -->
