# Invoice Data

## Data Entry Methods

Dybee supports three ways to import consumption data for each energy source.

### Manual Entry

Enter billing period data directly in the interface:

- Start date
- End date
- Consumption value

Suitable for small datasets or one-time corrections.

### Excel Import

Import multiple periods at once using a spreadsheet with three columns:

```
Date Start | Date End | Value
```

Dates must follow the format expected by Dybee (verify in the import dialog). This is the most efficient method for entering historical data.

### Automatic Retrieval

For supported utility providers, Dybee can retrieve invoice data automatically using your utility account credentials. Once configured, new billing data is imported without manual intervention.

## Data Quality

Baseline models and savings calculations are only as accurate as the underlying consumption data. Before creating a baseline:

- Ensure all billing periods are entered without gaps
- Verify that unusual values (e.g., estimated bills, corrections) are flagged or adjusted
- Confirm that the "Include in total consumption" flag is set on all relevant sources
