<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@kumodao/lib-base](./lib-base.md) &gt; [SendableKumo](./lib-base.sendablekumo.md) &gt; [repayKUSD](./lib-base.sendablekumo.repaykusd.md)

## SendableKumo.repayKUSD() method

Adjust existing Trove by repaying some of its debt.

<b>Signature:</b>

```typescript
repayKUSD(amount: Decimalish): Promise<SentKumoTransaction<S, KumoReceipt<R, TroveAdjustmentDetails>>>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  amount | [Decimalish](./lib-base.decimalish.md) | The amount of KUSD to repay. |

<b>Returns:</b>

Promise&lt;[SentKumoTransaction](./lib-base.sentkumotransaction.md)<!-- -->&lt;S, [KumoReceipt](./lib-base.kumoreceipt.md)<!-- -->&lt;R, [TroveAdjustmentDetails](./lib-base.troveadjustmentdetails.md)<!-- -->&gt;&gt;&gt;

## Remarks

Equivalent to:

```typescript
adjustTrove({ repayKUSD: amount })

```

