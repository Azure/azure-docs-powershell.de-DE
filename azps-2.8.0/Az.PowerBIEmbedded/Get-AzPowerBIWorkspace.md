---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 0bba0651d8b1125673b97aea625a11e598db6c85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823939"
---
# Get-AzPowerBIWorkspace

## Synopsis
Ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichs Sammlung ab.

## Syntax

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzPowerBIWorkspace** " Ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichs Sammlung ab.

## Beispiele

### Beispiel 1: Abrufen von Arbeitsbereichen einer Arbeitsbereichs Sammlung
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

Dieser Befehl ruft die Arbeitsbereiche ab, die der Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe angehören.

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
Gibt den Namen der Ressourcengruppe an, zu der die Arbeitsbereichs Sammlung gehört.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceCollectionName
Gibt den Namen der Arbeitsbereichs Sammlung an, für die dieses Cmdlet Arbeitsbereiche abruft.

```yaml
Type: System.String
Parameter Sets: (All)
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

### Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace

## Notizen

## Verwandte Links

[Get-AzPowerBIWorkspaceCollection](./Get-AzPowerBIWorkspaceCollection.md)


