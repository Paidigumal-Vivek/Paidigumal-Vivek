# DAX / Calculated-Column Reference

The Power BI model uses calculated columns for row-level transformations needed for grouping, filtering, sorting, and response-time analysis.

> The formulas below document the analytical intent. The authoritative implementation is the `.pbix` model.

## Temporal fields

### Hour
```DAX
Hour = HOUR('RAW DATA'[Incident Date / Time])
```

### Month
```DAX
Month = MONTH('RAW DATA'[Incident Date / Time])
```

### Month Number
```DAX
Month Number = MONTH('RAW DATA'[Incident Date / Time])
```

### Day Name
```DAX
Day Name = FORMAT('RAW DATA'[Incident Date / Time], "dddd")
```

### Day Number
```DAX
Day Number = WEEKDAY('RAW DATA'[Incident Date / Time], 2)
```

### Week Type
```DAX
Week Type =
IF(
    WEEKDAY('RAW DATA'[Incident Date / Time], 2) >= 6,
    "Weekend",
    "Weekday"
)
```

## Response metrics

The model includes calculated fields for dispatch delay, travel time, and total response time based on the available CAD timestamps. The implementation should preserve blank timestamps rather than converting missing operational events into artificial zero-duration responses.

## Response-time grouping

The dashboard groups total response time into operationally interpretable bands:

- 0–30 minutes
- 31–60 minutes
- 1–4 hours
- 4–24 hours
- >24 hours
- Missing

## Unit deployment fields

`Units Assigned Count` provides a row-level count of assigned resources. `Units Assigned Group` converts the count into categories that make deployment intensity easier to compare visually.

## Modeling note

Calculated **columns** were used deliberately for row-level attributes. These fields need to exist at the record level so they can be used in visual axes, slicers, sorting, and categorical groupings. Measures remain appropriate for aggregate KPIs and summary calculations.
