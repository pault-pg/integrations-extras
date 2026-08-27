# CHANGELOG - UPSC

## 1.0.2 / 2026-08-27

***Fixed***:

* Fix `ups.status` reporting a UPS that is on line power as if it were not. `ups.status` holds a space separated set of flags and the on-line flag is not always the first one: `upsd` prepends `FSD` while a forced shutdown is in progress and drivers can prepend `ALARM`, so `FSD OL` and `ALARM OL` were both flattened to 0. The flag is now looked for among all of them ([#PRNUM](https://github.com/DataDog/integrations-extras/pull/PRNUM)).

## 1.0.1 / 2022-07-01

***Fixed***:

* Fix encoding errors when capturing output and improve device handling ([#1354](https://github.com/DataDog/integrations-extras/pull/1354))

## 0.1.0

***Added***:

* adds upsc stats collector integration.
