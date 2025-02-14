<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@kumodao/lib-base](./lib-base.md) &gt; [Fees](./lib-base.fees.md) &gt; [redemptionRate](./lib-base.fees.redemptionrate.md)

## Fees.redemptionRate() method

Calculate the current redemption rate.

<b>Signature:</b>

```typescript
redemptionRate(redeemedFractionOfSupply?: Decimalish, when?: Date): Decimal;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  redeemedFractionOfSupply | [Decimalish](./lib-base.decimalish.md) | The amount of KUSD being redeemed divided by the total supply. |
|  when | Date | Optional timestamp that can be used to calculate what the redemption rate would decay to at a point of time in the future. |

<b>Returns:</b>

[Decimal](./lib-base.decimal.md)

## Remarks

By default, the fee is calculated at the time of the latest block. This can be overridden using the `when` parameter.

Unlike the borrowing rate, the redemption rate depends on the amount being redeemed. To be more precise, it depends on the fraction of the redeemed amount compared to the total KUSD supply, which must be passed as a parameter.

To calculate the redemption fee in KUSD, multiply the redeemed KUSD amount with the redemption rate.

## Example


```typescript
const fees = await liquity.getFees();
const total = await liquity.getTotal();

const redeemedKUSDAmount = Decimal.from(100);
const redeemedFractionOfSupply = redeemedKUSDAmount.div(total.debt);
const redemptionRate = fees.redemptionRate(redeemedFractionOfSupply);
const redemptionFeeKUSD = redemptionRate.mul(redeemedKUSDAmount);

```

