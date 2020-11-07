---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662450"
---
# Set-AzureRmMarketplaceTerms

## Synopsis
Akzeptieren oder ablehnen von Ausdrücken für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name). Bitte verwenden Sie Get-AzureRmMarketplaceTerms, um die Vertragsbedingungen zu erhalten.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### AgreementAcceptParameterSet (Standard)
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AgreementRejectParameterSet
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectAcceptParameterSet
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectRejectParameterSet
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmMarketplaceTerms** " speichert das Ausdrücke-Objekt für die angegebene Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name)-Tupel.

## Beispiele

### Beispiel 1
Abrufen des Marketplace Publisher-Vertrags
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### Beispiel 2
Stellen Sie die Publisher-Vereinbarung auf "akzeptieren" ein. Abrufen des Werts für den "Termes"-Parameter aus dem Cmdlet "Get-AzureRmMarketplaceTerms"
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## Parameter

### – Akzeptieren
Geben Sie diese an, um die rechtlichen Best imbegriffe zu akzeptieren.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
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

### -Inputobject
In Get-AzureRmMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt. Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Plan-Identifier-Zeichenfolge des bereitzustellenden Bilds

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Product
Angebots Kennungszeichenfolge des bereitzustellenden Bilds.

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publisher
Herausgeber Kennungszeichenfolge des bereitzustellenden Bilds.

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ablehnen
Übergeben Sie diese, um die rechtlichen Best imbegriffe abzulehnen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AGB
In Get-AzureRmMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt. Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms
Parameter: Inputobject (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms

## Notizen

## Verwandte Links
