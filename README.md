# Supplementary Material

Supplementary artifacts for the paper:

**Urban Anomaly Detection from UE Geo-Signaling Data**

Nguyen-Dung Ha, Minh-Hoang Nguyen, and Vu-Duc Ngo.

## Quick access

| Artifact | Description |
| --- | --- |
| [Supplementary report](./docs/1571313031_Supplementary_Material.pdf) | GEO-system characterization, validation protocol, baseline comparisons, sensitivity analysis, quality control, and privacy notes. |
| [Public GEO-signaling sample](./data/sample/geo_signaling_public_sample.xlsx) | Small anonymized sample provided only to illustrate the public schema and field semantics. |
| [Top-10 area validation map](./validation/maps/top10_area_user_count_with_ue_points.kml) | H3 area candidates, event context, and anonymized representative UE points used for geographic inspection. |
| [Top-10 user spatial-audit map](./validation/maps/top10_user_spatial_audit.kmz) | Same-block reference locations and anomalous locations for the ten highest-ranked user candidates. |

## Repository structure

```text
.
|-- README.md
|-- docs/
|   `-- 1571313031_Supplementary_Material.pdf
|-- data/
|   |-- README.md
|   `-- sample/
|       `-- geo_signaling_public_sample.xlsx
`-- validation/
    |-- README.md
    `-- maps/
        |-- top10_area_user_count_with_ue_points.kml
        `-- top10_user_spatial_audit.kmz
```

## Scope of the supplementary material

The supplementary report provides:

- Top-10 area-event and user-movement validation;
- shared-baseline versus leave-one-date-out benchmarking;
- Top-k comparisons with statistical and machine-learning baselines;
- LTE CellTrace and GEO-location system characterization;
- observation-frequency and location-quality metadata distributions; and
- implementation, quality-control, and privacy details.

The area-validation map contains H3 polygons and representative UE point summaries for the detected event block. Each point uses a display-only anonymous label, and its coordinate is the mean coordinate of that UE's records inside the relevant H3 cell and time block. Original subscriber identifiers are not exported.

The user spatial-audit map compares each detected location with same-block reference locations. It supports verification of non-routine spatial displacement; it does not by itself attribute the movement to a specific external event.

## Viewing the map files

The KML and KMZ files can be opened in Google Earth Pro:

1. Download the selected file from the table above.
2. In Google Earth Pro, select **File > Open**.
3. Expand the folders in the **Places** panel and select a polygon or point to inspect its context.

For the area map, the H3 polygons identify candidate hotspot areas and the point layer provides the corresponding anonymized, event-block UE summaries. For the user map, the reference and anomaly layers show the normal and detected locations used to calculate the reported spatial shift.

## Data availability and privacy

This public repository contains only a small anonymized schema sample and derived validation artifacts. It does not contain original subscriber identifiers or the private operator feed.

The original private feed, `datafeed.20251221-0300.csv.gz`, is not stored in this repository because of operator confidentiality and mobility-privacy requirements. Access may be considered for IEEE reviewers following a formal request, operator approval, and appropriate secure-access controls.

The public validation maps contain derived coordinates and display-only anonymous labels. They must not be used to infer subscriber identity or individual behavior beyond the validation scope described in the paper.

## Citation

Please cite the paper when using or referring to these supplementary artifacts:

> Nguyen-Dung Ha, Minh-Hoang Nguyen, and Vu-Duc Ngo, "Urban Anomaly Detection from UE Geo-Signaling Data," 2026.

## Version

Version 1.1, September 2026.
