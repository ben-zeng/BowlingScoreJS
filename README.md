
# TDD Bowling Scorecard Kata in JavaScript


### To run bowling scorecard

- Clone this repo
- `$ cd BowlingScoreJS`
- `$ open index.html`
- Populate bowls in text fields
- Click calculate!

![Run_1](./readme_images/demo_run_1.png) 

#### Notes
- If clicking calculate does nothing, it's very likely an error has occurred which has not been caught, such as:
    - If invalid bowl entered, i.e. number not between 0 - 10, clicking calculate will do nothing.
    - If entering a value for the 3rd bowl in frame 10 when first two bowls are not a strike or spare, clicking calculate will do nothing.
    - All text fields need to be filled with a number between 0 - 10 otherwise clicking calculate will do nothing.

### Future Improvements

- Adding buttons to populate text fields with scores instead of needing them to be typed
- Tidy up HTML files by generating HTML using JS
- Take JS out of html file
- Alert on error instead of writing to console log


### To Run Tests
- Clone this repo
- `$ cd BowlingScoreJS`
- Then either:
    - `$ open SpecRunner.html` OR
    - `$ npm install`
    - `$ karma start`

![Test_1](./readme_images/demo_test_1.png) 


### Rules


#### Strikes

The player receives a strike if they knock down all 10 pins with the first roll in a frame. The frame ends immediately (since there are no pins left for a second roll). The bonus for that frame is the number of pins knocked down by the next two rolls. That would be the next frame, unless the player rolls another strike.

#### Spares

The player receives a spare if they knock down all 10 pins with the two rolls of a frame. The bonus for that frame is the number of pins knocked down by the next roll (first roll of next frame).

#### 10th frame

If the player rolls a strike or spare in the 10th frame they can roll the additional balls for the bonus. But they can never roll more than 3 balls in the 10th frame. The additional rolls only count for the bonus not for the regular frame count.

    10, 10, 10 in the 10th frame gives 30 points (10 points for the regular first strike and 20 points for the bonus).
    1, 9, 10 in the 10th frame gives 20 points (10 points for the regular spare and 10 points for the bonus).

#### Gutter Game

A Gutter Game is when the player never hits a pin (20 zero scores).

#### Perfect Game

A Perfect Game is when the player rolls 12 strikes (10 regular strikes and 2 strikes for the bonus in the 10th frame). The Perfect Game scores 300 points.

In the image below you can find some score examples.

More about ten pin bowling here: http://en.wikipedia.org/wiki/Ten-pin_bowling

![Ten Pin Score Example](images/example_ten_pin_scoring.png)
