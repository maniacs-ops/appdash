# Changelog

- Apr 26, 2016
  - [#153](https://github.com/sourcegraph/appdash/pull/136) Added a Recorder.Logger field which, when non-nil, causes errors to be logged instead of checked explicitly via the Errors method.
- Apr 15, 2016 - **Breaking Changes!**
  - [#136](https://github.com/sourcegraph/appdash/pull/136) Users must now call `Recorder.Finish` when finished recording, or else data    will not be collected.
  - [#136](https://github.com/sourcegraph/appdash/pull/136) AggregateStore is removed in favor of InfluxDBStore, which is also embeddable, and is generally faster and more reliable. Refer to the [cmd/webapp-influxdb](https://github.com/sourcegraph/appdash/blob/master/examples/cmd/webapp-influxdb/main.go#L50) for further information on how to migrate to `InfluxDBStore`, or [read more about why this change was made](https://github.com/sourcegraph/appdash/issues/137).
  - [#136](https://github.com/sourcegraph/appdash/issues/136) `AggregateEvent`, `Trace.IsAggregate` and `Trace.Aggregated` are removed.
- Mar 28, 2016
  - [#110](https://github.com/sourcegraph/appdash/pull/110) Added support for the [OpenTracing API](http://opentracing.io/).
- Mar 9 2016
  - [#99](https://github.com/sourcegraph/appdash/pull/99) Added an embeddable InfluxDB storage engine.