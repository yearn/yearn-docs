# Computation

- [Computation](#Computation)
  - [formatSignificant](#formatSignificant)
    - [Function Signature](#Function-Signature)
    - [Input Parameters](#Input-Parameters)
    - [Example Usage](#Example-Usage)
  - [formatSignificantDecimals](#formatSignificantDecimals)
    - [Function Signature](#Function-Signature-1)
    - [Input Parameters](#Input-Parameters-1)
    - [Example Usage](#Example-Usage-1)
  - [formatFixed](#formatFixed)
    - [Function Signature](#Function-Signature-2)
    - [Input Parameters](#Input-Parameters-2)
    - [Example Usage](#Example-Usage-2)
  - [formatFixedDecimals](#formatFixedDecimals)
    - [Function Signature](#Function-Signature-3)
    - [Input Parameters](#Input-Parameters-3)
    - [Example Usage](#Example-Usage-3)

## formatSignificant

This function formats values to a specified number of significant digits.

### Function Signature

```typescript
export function formatSignificant(bigNumberish: BigNumberish, options?: FormatSignificantOptions): string
```

### Input Parameters

| Parameter    | Type                       | Description                |
| :----------- | :------------------------- | :------------------------- |
| bigNumberish | `BigNumberish`             | The value to be formatted. |
| options?     | `FormatSignificantOptions` | Formatting options.        |

### Example Usage

```typescript
const formatted: string = formatSignificant('123456', { significantDigits: 3 }) // 1.23
```

## formatSignificantDecimals

This function formats token and ethereum values to a specified number of significant digits.

### Function Signature

```typescript
export function formatSignificantDecimals(
  bigNumberish: BigNumberish,
  decimals: number,
  options?: FormatSignificantOptions
): string
```

### Input Parameters

| Parameter    | Type                       | Description                       |
| :----------- | :------------------------- | :-------------------------------- |
| bigNumberish | `BigNumberish`             | The value to be formatted.        |
| decimals     | `number`                   | The decimals of the passed value. |
| options?     | `FormatSignificantOptions` | Formatting options.               |

### Example Usage

```typescript
const formatted: string = formatSignificantDecimals('1234560000000000000', 18, { significantDigits: 3 }) // 1.23
```

## formatFixed

This function formats values to a specified number of decimal places.

### Function Signature

```typescript
export function formatFixed(bigNumberish: BigNumberish, options?: FormatFixedOptions): string
```

### Input Parameters

| Parameter    | Type                 | Description                |
| :----------- | :------------------- | :------------------------- |
| bigNumberish | `BigNumberish`       | The value to be formatted. |
| options?     | `FormatFixedOptions` | Formatting options.        |

### Example Usage

```typescript
const formatted: string = formatFixed('1.2345', { decimalPlaces: 2 }) // 1.23
```

## formatFixedDecimals

This function formats token and ethereum values to a specified number of decimal places.

### Function Signature

```typescript
export function formatFixedDecimals(
  bigNumberish: BigNumberish,
  decimals: number,
  options?: FormatFixedOptions
): string
```

### Input Parameters

| Parameter    | Type                 | Description                       |
| :----------- | :------------------- | :-------------------------------- |
| bigNumberish | `BigNumberish`       | The value to be formatted.        |
| decimals     | `number`             | The decimals of the passed value. |
| options?     | `FormatFixedOptions` | Formatting options.               |

### Example Usage

```typescript
const formatted: string = formatFixedDecimals('1234560000000000000', 18, { decimalPlaces: 2 }) // 1.23
```
