---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: 9aca04a3b8bbccccd2950be30f0f13287997bcfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499706"
---
# Get-AzureRmVMSize

## Synopsis
Ruft Verfügbare Größen für virtuelle Maschinen ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ListVirtualMachineSizeParamSet (Standard)
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForAvailabilitySet
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForVirtualMachine
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmVMSize** " ruft Verfügbare Größen für virtuelle Maschinen ab.

## Beispiele

### Beispiel 1: Abrufen von Größen für virtuelle Maschinen für einen Standort
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

Dieser Befehl ruft die verfügbaren Größen für virtuelle Computer an der angegebenen Position ab.

### Beispiel 2: Abrufen von Größen für einen Verfügbarkeits Satz
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

Dieser Befehl ruft Verfügbare Größen für virtuelle Computer ab, die Sie im Verfügbarkeits Satz mit dem Namen AvailabilitySet17 bereitstellen können.

### Beispiel 3: Abrufen von Größen für einen vorhandenen virtuellen Computer
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

Dieser Befehl ruft Verfügbare Größen für den vorhandenen virtuellen Computer mit dem Namen VirtualMachine12 ab.
Sie können die Größe dieses virtuellen Computers auf die Größen ändern, die dieser Befehl erhält.

## Parameter

### -AvailabilitySetName
Gibt den Namen der verfügbarkeitsgruppe an, für die dieses Cmdlet die verfügbaren Größen für virtuelle Maschinen erhält.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Standort
Gibt den Speicherort an, für den dieses Cmdlet die verfügbaren Größen für virtuelle Maschinen erhält.

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des virtuellen Computers an.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt den Namen des virtuellen Computers an, an dem dieses Cmdlet die verfügbaren Größen für virtuelle Maschinen zur Größenänderung erhält.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
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

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineSize

## Notizen

## Verwandte Links

[Get-AzureRmVM](./Get-AzureRmVM.md)


