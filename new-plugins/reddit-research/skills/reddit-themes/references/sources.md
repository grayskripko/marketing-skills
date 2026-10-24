# Sources and scope

Read 2026-10-10. These sources describe fields and coverage, not guaranteed public access. No copied policy rule is needed for offline analysis.

- https://www.reddit.com/dev/api/#GET_comments_article — Reddit's API documentation describes a thread comment tree and parameters that restrict depth and returned comments. This supports preserving thread/reply context and avoiding a completeness claim from a partial response.
- https://www.reddit.com/dev/api/#GET_api_morechildren — Reddit documents retrieval of comments left out of a base tree. This supports treating omitted-comment stubs as missing evidence, not readable records. The package does not invoke that endpoint.
- https://www.reddit.com/dev/api/#listings — Reddit describes listing pagination. An end marker for one listing is not proof that all nested comments were read.

Authored research rules of thumb: deduplicate stable IDs before counting; distinguish comment counts from people; preserve minority experiences; quote short exact excerpts; attach provided source links; use only supplied content; do not fetch or reconstruct missing/deleted material. These are workflow choices, not Reddit policy or statistical claims.
