---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 19b1d1b0da719167d53739a8c92a97121656aa9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823936"
---
# Get-AzPowerBIWorkspaceCollection

## Synopsis
Ruft Power BI-Arbeitsbereichs Sammlungen ab.

## Syntax

### ResourceGroupParameterSet
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WorkspaceCollectionNameParameterSet
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzPowerBIWorkspaceCollection** " ruft Power BI-Arbeitsbereichs Auflistungen in Ihrem Azure-Abonnement und ihrer Ressourcengruppe oder nach dem Sammlungsnamen ab.

## Beispiele

### Beispiel 1: Abrufen aller Arbeitsbereichs Auflistungen in einer Ressourcengruppe
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

Dieser Befehl ruft die Arbeitsbereichs Auflistungen ab, die zur Ressourcengruppe mit dem Namen ResourceGroup17 gehören.

### Beispiel 2: Abrufen einer Arbeitsbereichs Sammlung unter Verwendung des Namens
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

Dieser Befehl ruft die Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe ab.

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet Arbeitsbereichs Sammlungen erhält.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceCollectionName
Gibt den Namen der Power BI-Arbeitsbereichs Sammlung an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection

## Notizen

## Verwandte Links

[Neu – AzPowerBIWorkspaceCollection](./New-AzPowerBIWorkspaceCollection.md)

[Remove-AzPowerBIWorkspaceCollection](./Remove-AzPowerBIWorkspaceCollection.md)


