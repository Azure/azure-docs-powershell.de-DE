---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163908"
---
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
Erstellen eines Speicherobjekts für "QueryFilter"

## SYNTAX

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## BESCHREIBUNG
Erstellen eines Speicherobjekts für "QueryFilter"

## BEISPIELE

### Beispiel 1: Erstellen eines Abfragefilterobjekts für den Kostenmanagementexport
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

Mit diesem Befehl wird ein Filterobjekt der Abfrage für den Kostenmanagementexport erstellt.

## PARAMETERS

### -Und
Der logische Ausdruck "UND".
Mindestens zwei Elemente müssen enthalten sein.
Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dimensionen
Verfügt über einen Vergleichsausdruck für eine Dimension.
Informationen zum Erstellen finden Sie im Abschnitt "NOTIZEN" für #A0 und erstellen eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Not
Der logische Ausdruck "NOT".
Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Oder
Der logische Ausdruck "ODER".
Mindestens zwei Elemente müssen enthalten sein.
Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Verfügt über einen Vergleichsausdruck für ein Tag.
Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


AND <IQueryFilter[]>: Der logische Ausdruck "UND". Mindestens zwei Elemente müssen enthalten sein.
  - `[And <IQueryFilter[]>]`: Der logische Ausdruck "UND". Mindestens zwei Elemente müssen enthalten sein.
  - `[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension
    - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
    - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden
  - `[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".
  - `[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER". Mindestens zwei Elemente müssen enthalten sein.
  - `[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag

DIMENSIONEN: <IQueryComparisonExpression> Verfügt über einen Vergleichsausdruck für eine Bemaßung.
  - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
  - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden

NOT: <IQueryFilter> Der logische Ausdruck "NOT".
  - `[And <IQueryFilter[]>]`: Der logische Ausdruck "UND". Mindestens zwei Elemente müssen enthalten sein.
  - `[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension
    - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
    - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden
  - `[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".
  - `[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER". Mindestens zwei Elemente müssen enthalten sein.
  - `[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag

ODER <IQueryFilter[]>: Der logische Ausdruck "ODER". Mindestens zwei Elemente müssen enthalten sein.
  - `[And <IQueryFilter[]>]`: Der logische Ausdruck "UND". Mindestens zwei Elemente müssen enthalten sein.
  - `[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension
    - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
    - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden
  - `[Not <IQueryFilter>]`: Der logische Ausdruck "NICHT".
  - `[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER". Mindestens zwei Elemente müssen enthalten sein.
  - `[Tag <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für ein Tag

TAG: <IQueryComparisonExpression> Verfügt über einen Vergleichsausdruck für ein Tag.
  - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
  - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden

## LINKS ZU VERWANDTEN THEMEN

