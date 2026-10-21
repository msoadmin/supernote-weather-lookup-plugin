# Supernote Weather Lookup Plugin

A weather forecast lookup plugin for Supernote. Write or type a location, lasso it, and choose **Weather Lookup** to view a forecast and optionally insert it into your note.

## Features

- Recognizes handwritten locations from the Supernote lasso menu
- Supports U.S. **city + state** input, such as `Stafford, NY` or `Trumbull, CT`
- Supports U.S. **ZIP codes**, such as `06611`
- Supports **international city + country** input, such as `London, UK` or `Nakuru, Kenya`
- Resolves U.S. state abbreviations as state constraints to avoid similarly named cities in the wrong state
- Shows current conditions and a multi-day forecast
- Lets you correct the recognized location in the popup and run the forecast again
- **Insert Forecast** adds the forecast to the current note
- **Dismiss** closes the popup without changing the note
- E-ink-friendly interface designed for Supernote
- Includes the **Supernote Corner Method** for improved handwriting recognition near the lower corners of affected A5X pages

## Installation

1. Download the current `.snplg` file from the repository's **Releases** page.
2. Copy the plugin file to your Supernote using your normal Supernote plugin installation method.
3. Open the `.snplg` file on the Supernote and install it.
4. Open a regular Supernote Note.
5. Write a location such as `Trumbull, CT`, `06611`, or `London, UK`.
6. Lasso the location.
7. Tap **Weather Lookup** in the lasso menu.

An Internet connection is required to retrieve weather information.

## How to Use

Write or type a location in a Supernote note and lasso it. Choose **Weather Lookup** from the lasso menu.

The plugin attempts to recognize and resolve the location automatically. If the location is incorrect, edit it in the popup and run the forecast again.

Use **Insert Forecast** to place the displayed forecast into the note, or **Dismiss** to close the popup without inserting anything.

### Examples

- `Trumbull, CT`
- `Stafford, NY`
- `Buffalo, NY`
- `06611`
- `London, UK`
- `Nakuru, Kenya`
- `Paris, France`

## Location Matching

The plugin distinguishes U.S. state abbreviations from international country codes. For example, `Stafford, NY` is constrained to New York and will not silently fall back to a Stafford in another state.

For international locations, including the country is recommended when a city name could be ambiguous.

## Weather Data

The plugin uses online geocoding and weather services to resolve locations and retrieve forecasts. U.S. forecast support can use National Weather Service data when available, with Open-Meteo services used for worldwide location/forecast support and fallback behavior.

Weather information is provided for convenience and can change. Do not rely on this plugin as the sole source for emergency or safety-critical weather decisions.

## Supernote Corner Method

Some Supernote A5X environments can report a 1404 × 1872 page while selected handwriting strokes use a higher-resolution EMR coordinate space. This mismatch can cause handwriting recognition to fail near the lower corners of the page.

The plugin incorporates the **Supernote Corner Method**: when that affected coordinate pattern is detected, handwriting recognition uses the corrected 1920 × 2560 recognition space. This improves lower-corner OCR while preserving normal lasso behavior elsewhere on the page.

## Compatibility

Developed and tested for the **Supernote A5X**, including firmware **2.26.39**.

The plugin intentionally retains the legacy-compatible Supernote plugin architecture used by the related KJV Lookup and Stock Quote tools rather than depending on newer APIs that may not register correctly in the lasso menu on this firmware.

## Current Version

**v0.1.3**

This version includes worldwide location support, the updated partly-cloudy lasso icon, removal of the unnecessary upcoming-days heading, and stricter U.S. state matching.

## Status

The plugin is an independent community project and is not affiliated with or endorsed by Supernote, the National Weather Service, or Open-Meteo.

## Author

Robert Hammond
