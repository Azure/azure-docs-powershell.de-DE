---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: fa8681a8dab5aaba6d82b03a8b3885fd453e1faa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500881"
---
# Get-AzureRmVmss

## Synopsis
Ruft die Eigenschaften eines VMSS ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Defaultparameter (Standard)
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
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

### -InstanceView
Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des VMSS an.

```yaml
Type: System.String
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
Type: System.String
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


