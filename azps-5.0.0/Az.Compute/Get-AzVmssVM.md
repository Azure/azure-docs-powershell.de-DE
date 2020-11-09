---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303194"
---
# Get-AzVmssVM

## Synopsis
Ruft die Eigenschaften eines virtuellen VMSS-Computers ab.

## Syntax

### Defaultparameter (Standard)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzVmssVM** " Ruft die Modellansicht und die Instanzen Ansicht einer virtuellen Maschine für einen virtuellen Computer-Skalierungs Satz (VMSS) ab.
Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.
Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.
Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.

## Beispiele

### Beispiel 1: Abrufen der Eigenschaften eines virtuellen VMSS-Computers
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers mit dem Namen VMSS001 ab, der zur Ressourcengruppe mit dem Namen Group001 gehört.
Da der Befehl den *InstanceView* -Schalterparameter nicht angibt, ruft das Cmdlet die Modellansicht des virtuellen Computers ab.

### Beispiel 2: Abrufen der Modell Ansichtseigenschaften eines virtuellen VMSS-Computers
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers mit dem Namen VMSS004 ab, der zur Ressourcengruppe mit dem Namen Group002 gehört.
Der Befehl ruft die in der Variablen $ID gespeicherte Instanz-ID ab, für die die Modellansicht abgerufen werden soll.

### Beispiel 3: Abrufen der Eigenschaften der Instanzen Ansicht eines virtuellen VMSS-Computers
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers mit dem Namen VMSS004 ab, der zur Ressourcengruppe mit dem Namen Group002 gehört.
Da der Befehl den *InstanceView* -Switch-Parameter angibt, ruft das Cmdlet die Instanzen Ansicht des virtuellen Computers ab.
Der Befehl ruft die in der Variablen $ID gespeicherte Instanz-ID ab, für die die Instanzen Ansicht abgerufen werden soll.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -InstanceId
Gibt die Instanz-ID an, für die die Modellansicht abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Position: 0
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
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM

## Notizen

## Verwandte Links

[Satz-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


