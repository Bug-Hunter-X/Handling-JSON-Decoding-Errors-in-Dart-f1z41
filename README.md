# Dart JSON Decoding Error Handling

This repository demonstrates a common error in Dart when handling JSON responses from APIs:  inadequate handling of JSON decoding failures.  The original code lacks robust error handling for cases where the JSON response is malformed or invalid.

The `bug.dart` file shows the problematic code. The `bugSolution.dart` file provides an improved version with more comprehensive error handling.

## How to Reproduce

1. Clone this repository.
2. Run `bug.dart`.  Observe the behavior when the API returns valid JSON and when it returns invalid JSON.
3. Run `bugSolution.dart` to see how the issue is addressed.

## Solution

The solution involves using a `try-catch` block specifically around the `json.decode()` call to catch `FormatException` errors, which are thrown when the JSON is malformed.
