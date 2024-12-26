# React Native Dimensions API Returns Undefined or 0

This repository demonstrates a common issue in React Native where the `Dimensions` API returns `undefined` or `0` for width and height, especially during the initial app load. The problem arises because the dimensions are not immediately available and accessing them prematurely leads to incorrect values.

## Problem

The `Dimensions` API in React Native provides screen dimensions. However, if accessed too early in the app lifecycle, before the layout is calculated, it might return `undefined` or `0`.

## Solution

The solution involves ensuring the dimensions are available before accessing them.  This can be achieved using `useEffect` and checking if dimensions are 0.  A fallback value is used initially to prevent errors.