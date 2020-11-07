---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658090"
---
# Get-AzAttestation

## Synopsis
Ruft eine Bescheinigung ab.

## Syntax

### NameParameterSet (Standard)
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupParameterSet
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Get-AzAttestation-Cmdlet erhält Informationen zur Bescheinigung in einem Abonnement.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
Besorgen Sie sich die Bescheinigung "Beispiel" in der Ressourcengruppe "RG1". 

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name der Bescheinigung.

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die der abgefragten Bescheinigung zugeordnet ist.

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Gibt den Namen der Resourcen-Nr. an, die der Befragten Bescheinigung zugeordnet ist.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Testat. Models. PSAttestation

## Notizen

## Verwandte Links
