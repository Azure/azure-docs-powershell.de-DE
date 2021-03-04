---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 604109a80171ff4bb294dc1643081cd8e933d728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922491"
---
# Get-AzBillingInvoice

## SYNOPSIS
Abrechnungsrechnungen des Abonnements erhalten.
Abrechnungsrechnungen eines Abrechnungskontos und Eines Abrechnungsprofils erhalten

## SYNTAX

### Liste (Standard)
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### Neueste Version
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### Single
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzBillingInvoice-Cmdlet** erhält Abrechnungsrechnungen des Abonnements. 

## BEISPIELE

### Beispiel 1
```
PS C:\> Get-AzBillingInvoice -Latest
```

Erhalten Sie die neueste Rechnung des Abonnements.

### Beispiel 2
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

Erhalten Sie die Rechnung des Abonnements mit dem angegebenen Namen.

### Beispiel 3
```
PS C:\> Get-AzBillingInvoice
```

Holen Sie sich alle verfügbaren Rechnungen des Abonnements in umgekehrter chronologischer Reihenfolge ab der neuesten Rechnung ohne Download-URL. 

### Beispiel 4
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Holen Sie sich die letzten 10 Rechnungen des Abonnements, und fügen Sie die Download-URL in das Ergebnis ein.

### Beispiel 5
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

Holen Sie sich die spezifische Rechnung nach Name, und fügen Sie die Download-URL in das Ergebnis ein.

### Beispiel 6
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Holen Sie sich Rechnungen über den Namen des Abrechnungskontos, und fügen Sie die Download-URL für jede Rechnung in das Ergebnis ein.

### Beispiel 7
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Erhalten Sie eine bestimmte Rechnung nach Rechnungsname und Rechnungskontoname, und fügen Sie die Download-URL für jede Rechnung in das Ergebnis ein.

### Beispiel 8
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Holen Sie sich den Namen des aktuellen Rechnungskontos, und fügen Sie die Download-URL für rechnung in das Ergebnis ein.

### Beispiel 9
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

Holen Sie sich die neuesten 10 Rechnungen des jeweiligen Abrechnungskontos und eines bestimmten Abrechnungsprofils, und fügen Sie die Download-URL in das Ergebnis ein.

### Beispiel 10
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

Holen Sie sich die neueste Rechnung über den Namen des Abrechnungskontos und den Namen des Abrechnungsprofils, und fügen Sie die Download-URL für rechnung in das Ergebnis ein.

### Beispiel 10
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

Erhalten Sie Rechnungen nach Dem Namen des Abrechnungskontos und dem Namen des Abrechnungsprofils für einen Abrechnungszeitraum, der durch perioStart-Datum und PeriodEnd-Datum angegeben ist.


## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GenerateDownloadUrl
Generieren Sie die Download-URL der Rechnungen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Latest
Erhalten Sie die neueste Rechnung.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Bestimmt die maximale Anzahl von Datensätzen, die zurückzukehren sind.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name einer bestimmten Rechnung, die sie erhalten soll, oder der aktuellste, wenn nicht angegeben.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BillingAccountName
Name eines bestimmten Abrechnungskontos, für das Rechnungen erhalten werden.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BillingProfileName
Name eines bestimmten Abrechnungsprofils zum Erhalten von Rechnungen.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeriodStartDate
Startdatum für Rechnung.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeriodEndDate
Enddatum für Rechnung.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Billing.Models.PSInvoice

## NOTIZEN

## VERWANDTE LINKS
