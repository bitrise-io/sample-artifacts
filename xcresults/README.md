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

## xcresult3-flaky-ui-configuration.xcresult

`xcresult3` format, Xcode 27.2.

Has one UI test, `BullsEyeLaunchTests/testLaunch()` from
[sample-swift-project-with-parallel-ui-test](https://github.com/bitrise-io/sample-swift-project-with-parallel-ui-test),
run with `-retry-tests-on-failure -test-iterations 3`. It runs once for each UI configuration, and each
configuration is an `Arguments` node with its own repetitions.

`Light Appearance, Portrait` failed on the first run and passed on `Retry 1`. The other three
configurations passed first time. The test case still has a `Failed` result.

Recorded without attachments and test diagnostics, to keep it small.
