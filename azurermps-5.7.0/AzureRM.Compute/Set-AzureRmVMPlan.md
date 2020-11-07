---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662364"
---
# Set-AzureRmVMPlan

## Synopsis
Legt die Informationen zum Marktplatz Plan auf einem virtuellen Computer fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRmVMPlan** " legt die Azure Marketplace-Planinformationen für einen virtuellen Computer fest.

Bevor Sie ein Marketplace-Abbild über die Befehlszeile bereitstellen können, muss der programmgesteuerte Zugriff aktiviert sein, oder der virtuelle Computer muss mithilfe des Azure-Portals bereitgestellt werden.

## Beispiele

## Parameter

### -Name
Gibt den Namen des Bilds vom Marketplace an.
Dies ist derselbe Wert, der vom Get-AzureRmVMImageSku-Cmdlet zurückgegeben wird.
Weitere Informationen zum Auffinden von Bildinformationen finden Sie unter [navigieren und Auswählen von Bildern für Azure Virtual Machine mit PowerShell und der Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in der Microsoft Azure-Dokumentation.

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

### -Product
Gibt das Produkt des Bilds vom Marktplatz an.
Hierbei handelt es sich um dieselben Informationen wie der **Angebots** Wert des **imagereference** -Elements.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PromotionCode
Gibt einen Promotionscode an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
Gibt den Herausgeber des Bilds an.
Sie finden diese Informationen unter Verwendung des Get-AzureRmVMImagePublisher-Cmdlets.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des virtuellen Computers an, für das ein Marktplatz Plan festgelegt werden soll.
Sie können das Get-AzureRmVM-Cmdlet verwenden, um ein Objekt eines virtuellen Computers abzurufen.
Sie können das New-AzureRmVMConfig-Cmdlet verwenden, um ein Objekt eines virtuellen Computers zu erstellen.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Neu – AzureRmVMConfig](./New-AzureRmVMConfig.md)
