---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503853"
---
# Get-AzureRmVmss

## Synopsis
Ruft die Eigenschaften eines VMSS ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Defaultparameter (Standard)
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmVmss** " Ruft die Modell-und Instanzen Ansicht eines virtuellen Computer-Skalierungs Satzes (VMSS) ab.
Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.
Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.
Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.

## Beispiele

### Beispiel 1: Abrufen der Eigenschaften eines VMSS
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Dieser Befehl ruft die Eigenschaften des VMSS mit dem Namen VMSS001 ab, das zur Ressourcengruppe mit dem Namen Group001 gehört.
Da der Befehl den *InstanceView* -Schalterparameter nicht angibt, ruft das Cmdlet die Modellansicht des virtuellen Computers ab.

## Parameter

### -InstanceView
Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des VMSS an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Art der Name des VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
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

### Dieses Cmdlet generiert keine Ausgabe.

## Notizen

## Verwandte Links

[Neu – AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Neustart-AzureRmVmss](./Restart-AzureRmVmss.md)

[Satz-AzureRmVmss](./Set-AzureRmVmss.md)

[Anfang-AzureRmVmss](./Start-AzureRmVmss.md)

[Stopp-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


