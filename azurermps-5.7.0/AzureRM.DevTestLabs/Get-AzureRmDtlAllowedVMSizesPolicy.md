---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 25b3f15b6a71b54cbcab1a53f793a32da8b2173a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662740"
---
# Get-AzureRmDtlAllowedVMSizesPolicy

## Synopsis
Ruft die zulässige Größen Richtlinie für virtuelle Maschinen einer Übungseinheit in DevTest Labs ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDtlAllowedVMSizesPolicy** " Ruft die zulässige Größen Richtlinie für virtuelle Maschinen ab, mit der Sie eine Liste der in der Übungseinheit zulässigen virtuellen Computer Größen angeben können.
Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und eine Liste aller zulässigen virtuellen Computer Größen zurück, die Sie in der angegebenen Richtlinie festgelegt haben.

## Beispiele

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LabName
Gibt den Namen der Übungseinheit an, für die dieses Cmdlet eine Größen Richtlinie für virtuelle Maschinen erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy
Dieses Cmdlet gibt die Richtlinie zurück, die die Liste der in der Übungseinheit zulässigen virtuellen Computer Größen angibt.

## Notizen

## Verwandte Links

[Satz-AzureRmDtlAllowedVMSizesPolicy](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[Azure-Entwicklungs Test Lab-Cmdlets](./AzureRM.DevTestLabs.md)


