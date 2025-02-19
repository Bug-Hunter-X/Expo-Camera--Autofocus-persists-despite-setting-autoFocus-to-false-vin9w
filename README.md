# Expo Camera Autofocus Issue

This repository demonstrates a bug in Expo's Camera API where the autofocus functionality persists even when the `autoFocus` prop is set to `false`. This leads to unpredictable image quality and behavior, particularly in low-light conditions.

## Bug Description
The `autoFocus` prop in Expo's Camera component doesn't always behave as expected.  Even when explicitly set to `false`, the camera may still attempt to autofocus, resulting in inconsistent image capture. This is especially problematic in dynamic environments or low-light situations.

## Reproduction Steps
1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Observe the camera behavior.  Note the inconsistent focus.

## Solution
The provided solution uses a workaround by manually managing the focus distance using the `Camera.setCameraFocus` method. While not ideal, it mitigates the issue of unexpected autofocus behavior.  A better solution would be a fix within the Expo Camera API itself.