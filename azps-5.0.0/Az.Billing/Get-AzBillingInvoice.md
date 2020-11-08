---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178635"
---
# Get-AzBillingInvoice

## Synopsis
Abrechnungs Rechnungen des Abonnements abrufen.
Abrufen von Abrechnungs Rechnungen eines Abrechnungskontos und eines Abrechnungs Profils

## Syntax

### Liste (Standard)
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### Neueste
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### Einzel
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzBillingInvoice** " ruft Rechnungs Rechnungen des Abonnements ab. 

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzBillingInvoice -Latest
```

Besorgen Sie sich die aktuelle Rechnung des Abonnements.

### Beispiel 2
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

Besorgen Sie sich die Rechnung des Abonnements mit dem angegebenen Namen.

### Beispiel 3
```
PS C:\> Get-AzBillingInvoice
```

Abrufen aller verfügbaren Rechnungen des Abonnements in umgekehrter chronologischer Reihenfolge, beginnend mit der letzten Rechnung ohne Download-URL. 

### Beispiel 4
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Holen Sie sich die letzten 10 Rechnungen des Abonnements, und fügen Sie die Download-URL in das Ergebnis ein.

### Beispiel 5
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

Beziehen Sie die spezifische Rechnung nach Namen, und fügen Sie die Download-URL in das Ergebnis ein.

### Beispiel 6
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Sie erhalten Rechnungen nach Rechnungskonto Name und fügen die Download-URL für jede Rechnung in das Ergebnis ein.

### Beispiel 7
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Erhalten Sie eine bestimmte Rechnung nach Rechnungsname und Rechnungskonto Namen, und fügen Sie die Download-URL für jede Rechnung in das Ergebnis ein.

### Beispiel 8
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Aktuelle Rechnung nach Rechnungskonto Namen abrufen und die Download-URL für Rechnung in das Ergebnis einbeziehen.

### Beispiel 9
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

Holen Sie sich die letzten 10 Rechnungen des jeweiligen Abrechnungskontos und des bestimmten Abrechnungs Profils, und fügen Sie die Download-URL in das Ergebnis ein.

### Beispiel 10
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

Aktuelle Rechnung nach Rechnungskonto Name und Rechnungsprofil Namen abrufen und die Download-URL für Rechnung in das Ergebnis einbeziehen.

### Beispiel 10
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

Sie erhalten Rechnungen nach Rechnungskonto Name und Rechnungsprofil Name für einen Abrechnungszeitraum, der durch perioStart Datum und periodEnd Datum angegeben ist.


## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Neueste
Besorgen Sie sich die neueste Rechnung.

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
Bestimmt die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.

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
Der Name einer bestimmten Rechnung, die abgerufen werden soll, oder der letzte, wenn nicht angegeben.

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
Der Name eines bestimmten Abrechnungskontos, für das Rechnungen abgerufen werden sollen.

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
Der Name eines bestimmten Abrechnungs Profils, für das Rechnungen abgerufen werden sollen.

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
Anfangstermin für Rechnung.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Billing. Models. PSInvoice

## Notizen

## Verwandte Links
