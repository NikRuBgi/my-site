# Functions Reference

!!! info "Analytics Plan"
    This feature requires the Analytics Plan.

## Arithmetic Operators

| Operator | Description |
|---|---|
| `+` `-` `*` `/` | Basic arithmetic |
| `^` | Exponentiation |

## Comparison & Logic

| Operator | Description |
|---|---|
| `<` `>` `<=` `>=` `=` `<>` | Comparison operators |
| `AND` `OR` | Boolean logic |

## Mathematical Functions

| Function | Description |
|---|---|
| `sqrt(x)` | Square root |
| `log(x)` | Base-10 logarithm |
| `ln(x)` | Natural logarithm |
| `sin(x)` `cos(x)` `tan(x)` | Trigonometric functions |
| `asin(x)` `acos(x)` `atan(x)` | Inverse trigonometric functions |

## Aggregation Functions

| Function | Description |
|---|---|
| `avg(a, b, ...)` | Average of multiple values |
| `max(a, b, ...)` | Maximum of multiple values |
| `min(a, b, ...)` | Minimum of multiple values |

## Conditional

| Function | Description |
|---|---|
| `if(condition, value_if_true, value_if_false)` | Conditional expression |

**Example:**
```
if(tag.SA_T.avg > 25, 1, 0)
```

## Scheduling

| Function | Description |
|---|---|
| `schedule()` | Returns `1` during occupied hours, `0` otherwise, based on the building's schedule configuration |

## Counting

| Function | Description |
|---|---|
| `count(condition, ...)` | Counts arguments that meet the condition |
| `nb(a, b, ...)` | Counts non-null values |

## Time Shift

| Function | Description |
|---|---|
| `shift(value, n)` | Returns the value of `value` at t ± n hours |

**Example:** `shift(tag.SA_T.avg, -1)` returns last hour's supply air temperature.

## Interpolation

| Function | Description |
|---|---|
| `curve(x, x1, y1, x2, y2, ...)` | Interpolates `y` for a given `x` along a piecewise linear curve |

## Selection

| Function | Description |
|---|---|
| `first(a, b, ...)` | Returns the first non-null value from the list |

## Alias X

**Alias X** is a special mechanism for writing rules that work across equipment families with different topologies. Instead of hardcoding a specific hierarchy path, you assign Alias X (`load.X` or `source.X`) to different entity types depending on the family. This makes the rule generalize cleanly across buildings where the same equipment may be connected differently.
