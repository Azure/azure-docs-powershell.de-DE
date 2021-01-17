---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473090"
---
# Get-AzVmssVM

## SYNOPSIS
Ruft die Eigenschaften eines virtuellen VMSS-Computers ab.

## SYNTAX

### Standardparameter (Standard)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzVmssVM-Cmdlet** ruft die Modellansicht und Instanzansicht eines virtuellen VMSS (Virtual Machine Scale Set) ab.
Die Modellansicht ist die vom Benutzer angegebenen Eigenschaften des virtuellen Computers.
Die Instanzansicht ist der Status der Instanzebene des virtuellen Computers.
Geben Sie den *Parameter "Status"* an, um nur die Instanzansicht eines virtuellen Computers zu erhalten.

## BEISPIELE

### Beispiel 1: Erhalten der Eigenschaften eines virtuellen VMSS-Computers
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers namens VMSS001 ab, der zur Ressourcengruppe "Group001" gehört.
Da der Befehl den Parameter des *InstanceView-Schalters* nicht anfordert, ruft das Cmdlet die Modellansicht des virtuellen Computers ab.

### Beispiel 2: Erhalten der Modellansichtseigenschaften eines virtuellen VMSS-Computers
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers namens VMSS004 ab, der zur Ressourcengruppe "Group002" gehört.
Der Befehl ruft die Instanz-ID ab, die in der Variablen gespeichert $ID, für die die Modellansicht angezeigt werden soll.

### Beispiel 3: Erhalten der Instanzansichtseigenschaften eines virtuellen VMSS-Computers
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

Dieser Befehl ruft die Eigenschaften des virtuellen VMSS-Computers namens VMSS004 ab, der zur Ressourcengruppe "Group002" gehört.
Da der Befehl den *Parameter "InstanceView-Switch"* angibt, ruft das Cmdlet die Instanzansicht des virtuellen Computers ab.
Der Befehl ruft die Instanz-ID ab, die in der Variablen gespeichert $ID, für die die Instanzansicht angezeigt werden soll.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt die Instanz-ID an, für die die Modellansicht angezeigt werden soll.

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
Gibt an, dass dieses Cmdlet nur die Instanzansicht des virtuellen Computers erhält.

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
Gibt den Namen der Ressourcengruppe der VMSS an.

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
Arten des Namens der VMSS.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


