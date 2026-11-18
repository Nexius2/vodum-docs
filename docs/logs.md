# Logs

The Logs page provides paginated operational events, level filters, search and
an anonymized text export. Open event details to inspect multiline exceptions
without treating their continuation lines as unrelated events.

Level counters cover the retained history, not just the visible page. Unfiltered
paging uses an index and reads only the requested event page. Text search may
need broader analysis. Rotation/purge invalidates affected cached analysis;
unchanged archives can be reused within the bounded cache.

Recent dashboard logs are a short operational sample. For a pending action,
check its task/job or delivery history as well as the log timestamp and source.
For latency, see [Performance](performance.md) and its route-timing report.

Anonymization reduces exposure but does not make every support capture harmless.
Review exports and keep logs, backups and authentication-related details private.
