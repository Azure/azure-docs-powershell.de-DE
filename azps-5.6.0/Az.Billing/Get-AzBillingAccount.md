---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922507"
---
# Get-AzBillingAccount

## SYNOPSIS
Abrechnungskonten erhalten.

## SYNTAX

### Liste (Standard)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Single
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzBillingAccount-Cmdlet** erhält Abrechnungskonten, auf die benutzer zugreifen können. 

## BEISPIELE

### Beispiel 1
```
PS C:\> Get-AzBillingAccount
```

Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben.

### Beispiel 2
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

Holen Sie sich das Abrechnungskonto mit dem angegebenen Namen.

### Beispiel 3
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und fügen Sie die Adresse in das Ergebnis ein.

### Beispiel 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und fügen Sie die Abrechnungsprofile in das Ergebnis ein.

### Beispiel 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und fügen Sie die darunter gegliederten Abrechnungsprofile und Rechnungsabschnitte in das Ergebnis ein.

### Beispiel 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Holen Sie sich das Abrechnungskonto mit dem angegebenen Namen, und fügen Sie die darunter gegliederten Abschnitte Adresse, Abrechnungsprofile und Rechnungen in das Ergebnis ein.

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

### -IncludeAddress
Geben Sie die Adresse des Abrechnungskontos an.

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
Fügen Sie die Abrechnungsprofile unter dem Abrechnungskonto ein.

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
Fügen Sie die Abrechnungsprofile unter abrechnungskonto und rechnungsabschnitte darunter ein.

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
Name eines bestimmten Abrechnungskontos.

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
Listen Sie die Abrechnungsentitäten unter Abrechnungskonto auf, die als Eingabe zum Erstellen eines Abonnements verwendet werden können.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Billing.Models.PSBillingAccount

## NOTIZEN

## VERWANDTE LINKS
