---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: 84b54353b1f36dbfbb3cef068987c50a4b60923e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947939"
---
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
Erstellen eines Speicherobjekts für QueryFilter

## SYNTAX

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## BESCHREIBUNG
Erstellen eines Speicherobjekts für QueryFilter

## BEISPIELE

### Beispiel 1: Erstellen eines Filterobjekts der Abfrage für den Kostenverwaltungsexport
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

Mit diesem Befehl wird ein Filterobjekt der Abfrage für den Kostenverwaltungsexport erstellt.

## PARAMETER

### -Und
Der logische Ausdruck "UND".
Muss mindestens zwei Elemente enthalten.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für UND-Eigenschaften, und erstellen Sie eine Hashtabelle.

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
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu DIMENSIONS-Eigenschaften, und erstellen Sie eine Hashtabelle.

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
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für #A0 und Erstellen einer Hashtabelle.

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
Muss mindestens zwei Elemente enthalten.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für #A0 und Erstellen einer Hashtabelle.

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
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu #A0 und Erstellen einer Hashtabelle.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


UND <IQueryFilter[]>: Der logische Ausdruck "UND". Muss mindestens zwei Elemente enthalten.
  - `[And <IQueryFilter[]>]`: Der logische Ausdruck "UND". Muss mindestens zwei Elemente enthalten.
  - `[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension
    - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
    - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden
  - `[Not <IQueryFilter>]`: Der logische Ausdruck "NOT".
  - `[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER". Muss mindestens zwei Elemente enthalten.
  - `[Tag <IQueryComparisonExpression>]`: Verfügt über Vergleichsausdruck für ein Tag

DIMENSIONEN <IQueryComparisonExpression> : Verfügt über einen Vergleichsausdruck für eine Dimension.
  - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
  - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden

NICHT: <IQueryFilter> Der logische Ausdruck "NOT".
  - `[And <IQueryFilter[]>]`: Der logische Ausdruck "UND". Muss mindestens zwei Elemente enthalten.
  - `[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension
    - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
    - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden
  - `[Not <IQueryFilter>]`: Der logische Ausdruck "NOT".
  - `[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER". Muss mindestens zwei Elemente enthalten.
  - `[Tag <IQueryComparisonExpression>]`: Verfügt über Vergleichsausdruck für ein Tag

ODER <IQueryFilter[]>: Der logische Ausdruck "ODER". Muss mindestens zwei Elemente enthalten.
  - `[And <IQueryFilter[]>]`: Der logische Ausdruck "UND". Muss mindestens zwei Elemente enthalten.
  - `[Dimensions <IQueryComparisonExpression>]`: Verfügt über einen Vergleichsausdruck für eine Dimension
    - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
    - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden
  - `[Not <IQueryFilter>]`: Der logische Ausdruck "NOT".
  - `[Or <IQueryFilter[]>]`: Der logische Ausdruck "ODER". Muss mindestens zwei Elemente enthalten.
  - `[Tag <IQueryComparisonExpression>]`: Verfügt über Vergleichsausdruck für ein Tag

TAG <IQueryComparisonExpression> : Verfügt über einen Vergleichsausdruck für ein Tag.
  - `Name <String>`: Der Name der Spalte, die im Vergleich verwendet werden soll.
  - `Value <String[]>`: Array von Werten, die zum Vergleich verwendet werden

## VERWANDTE LINKS

