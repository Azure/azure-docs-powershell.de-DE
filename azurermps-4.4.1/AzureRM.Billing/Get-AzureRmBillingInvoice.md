---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 38b1c4e29ed82ac3bddcff9565a216bd6db23411
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500094"
---
# Get-AzureRmBillingInvoice

## Synopsis
Abrechnungs Rechnungen des Abonnements abrufen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Liste (Standard)
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Neueste
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Einzel
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmBillingInvoice** " ruft Rechnungs Rechnungen des Abonnements ab. 

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

Besorgen Sie sich die aktuelle Rechnung des Abonnements.

### Beispiel 2
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

Besorgen Sie sich die Rechnung des Abonnements mit dem angegebenen Namen.

### Beispiel 3
```
PS C:\> Get-AzureRmBillingInvoice
```

Abrufen aller verfügbaren Rechnungen des Abonnements in umgekehrter chronologischer Reihenfolge, beginnend mit der letzten Rechnung ohne Download-URL. 

### Beispiel 4
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Holen Sie sich die letzten 10 Rechnungen des Abonnements, und fügen Sie die Download-URL in das Ergebnis ein.

## Parameter

### -GenerateDownloadUrl
Generieren Sie die Download-URL der Rechnungen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Billing. Models. Rechnung, Microsoft. Azure. Commands. Billing, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Management. Billing. Models. Rechnung

## Notizen

## Verwandte Links

