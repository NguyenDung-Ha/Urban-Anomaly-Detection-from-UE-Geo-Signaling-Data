# Validation Artifacts

This directory contains the map artifacts used to inspect the highest-ranked area and user anomalies.

| File | Validation role |
| --- | --- |
| [`maps/top10_area_user_count_with_ue_points.kml`](./maps/top10_area_user_count_with_ue_points.kml) | Displays Top-10 area candidates as H3 polygons together with event context and anonymized representative UE points. |
| [`maps/top10_user_spatial_audit.kmz`](./maps/top10_user_spatial_audit.kmz) | Displays same-block reference locations and detected anomalous locations for the Top-10 user candidates. |

## Interpretation

Area candidates were checked against geographic context and publicly documented real-world events. Repeated H3/date candidates may correspond to the same underlying event and should not be interpreted as independent events.

User candidates were checked for consistency with a non-routine spatial shift relative to their same-block reference locations. This map validation confirms the displacement represented in the detector output but does not establish an external cause for every movement.

## Privacy

Original subscriber identifiers are not exported. The area map uses display-only anonymous point labels and one representative mean coordinate per UE within the relevant event H3 cell and time block. The artifacts are provided only for validation of the results reported in the paper.
