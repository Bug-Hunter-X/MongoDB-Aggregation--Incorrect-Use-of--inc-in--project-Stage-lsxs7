# MongoDB Aggregation Pipeline Bug: Incorrect $inc Usage

This repository demonstrates a common error when using the `$inc` operator within the `$project` stage of a MongoDB aggregation pipeline. The `$inc` operator is intended for update operations and does not behave as expected when used to create a new field by incrementing an existing one.

## Bug Description
The provided JavaScript code attempts to increment the `count` field using `$inc` within the `$project` stage. This results in the `incrementedCount` field not being correctly incremented. 

## Solution
The solution involves creating the new `incrementedCount` field and using the `$add` operator to perform the increment operation.