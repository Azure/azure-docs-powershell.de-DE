---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305280"
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
Das **Get-AzBillingAccount-Cmdlet** erhält Abrechnungskonten, auf die der Benutzer zugreifen kann. 

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

Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und geben Sie die Adresse in das Ergebnis ein.

### Beispiel 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und schließen Sie die Abrechnungsprofile in das Ergebnis ein.

### Beispiel 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Holen Sie sich alle Abrechnungskonten, auf die Benutzer Zugriff haben, und schließen Sie die Abrechnungsprofile und Rechnungsabschnitte darunter in das Ergebnis ein.

### Beispiel 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Holen Sie sich das Abrechnungskonto mit dem angegebenen Namen, und fügen Sie die Adresse, die Abrechnungsprofile und die Rechnungsabschnitte darunter in das Ergebnis ein.

## PARAMETERS

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
Schließen Sie die Abrechnungsprofile unter dem Abrechnungskonto ein.

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
Fügen Sie die Abrechnungsprofile in den Abschnitten "Abrechnungskonto" und "Rechnungen" darunter ein.

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
Listen Sie die Abrechnungsentitäten unter "Abrechnungskonto" auf, die als Eingabe zum Erstellen eines Abonnements verwendet werden können.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Billing.Models.PSBillingAccount

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
