# JDCM data

What the JDCM web app (https://makensi.es/jdcm) reads: the public JSON of
juegosdeportivos.ecmadrid.org for every group of the competition, read by a small device at home
(`pwa/pi/jdcm-fetch.sh` in https://github.com/olemoudi/jdcm) and force-pushed here as one commit
every run. Never edit it by hand.

- `v1/index.json`: when it was published, groups per sport, when each group last changed, the last run.
- `v1/state/sched-<sport>.json`: every group's matches from the grouped calendars (dates, venues,
  states; no scores), when each round number was read, refusals.
- `v1/groups/<id>/r<round>.json`: one round as the group's own page sent it (with scores).
- `v1/groups/<id>/meta.json`: that group's round list, when each round was read, its final results.
- `v1/groups/<id>/all.json`: all of the above for one group (what the app downloads).
- `v1/catalog/<sport>.json`: every competition, category, group and team of a sport.
