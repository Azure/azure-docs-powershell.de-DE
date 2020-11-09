---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302122"
---
# Get-AzBillingAccount

## Synopsis
Besorgen Sie sich Abrechnungskonten.

## Syntax

### Liste (Standard)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Einzel
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzBillingAccount** " erhält Abrechnungskonten, auf die der Benutzer zugreifen kann. 

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzBillingAccount
```

Alle Abrechnungskonten abrufen, auf die der Benutzer zugreifen kann.

### Beispiel 2
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

Besorgen Sie sich das Abrechnungskonto mit dem angegebenen Namen.

### Beispiel 3
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Rufen Sie alle Abrechnungskonten ab, auf die der Benutzer Zugriff hat, und fügen Sie die Adresse in das Ergebnis ein.

### Beispiel 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Rufen Sie alle Abrechnungskonten ab, auf die der Benutzer Zugriff hat, und fügen Sie die Abrechnungsprofile in das Ergebnis ein.

### Beispiel 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Besorgen Sie sich alle Abrechnungskonten, auf die der Benutzer Zugriff hat, und fügen Sie die Abrechnungsprofile und die Rechnungs Abschnitte in das Ergebnis ein.

### Beispiel 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Rufen Sie das Abrechnungskonto mit dem angegebenen Namen ab, und schließen Sie die Adresse, die Abrechnungsprofile und die Rechnungs Abschnitte in das Ergebnis ein.

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

### -IncludeAddress
Geben Sie die Adresse des Abrechnungskontos ein.

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

### -ExpandBillingProfile
Fügen Sie die Abrechnungsprofile unter das Abrechnungskonto ein.

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

### -ExpandInvoiceSection
Fügen Sie die Abrechnungsprofile unter den Abschnitten Abrechnungskonto und Rechnungen darunter ein.

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

### -Name
Der Name eines bestimmten Abrechnungskontos.

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

### -ListEntitiesToCreateSubscription
Listen Sie die Abrechnungs Entitäten unter Abrechnungskonto auf, die als Eingabe zum Erstellen eines Abonnements verwendet werden können.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
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

### Microsoft. Azure. Commands. Billing. Models. PSBillingAccount

## Notizen

## Verwandte Links
