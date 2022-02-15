# xcresult samples

## xcresult3-flaky-with-rerun.xcresult

`xcresult3` format.

Has 4 test suites:

- BullsEyeTests
- BullsEyeSlowTests
- BullsEyeUITests
- BullsEyeFlakyTests

The first three are successful, with no failures, no errors, no skipped tests.

The last one `BullsEyeFlakyTests` has a test, `testFlakyFeature()`, where test repetition on failure was turned on, the test failed the first time then passed the second run.

This test suite (`BullsEyeFlakyTests`) also includes a skipped test example called `testFlakySkip()`.
