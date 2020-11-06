---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4dbae539d43961d954dba6ea12bd88e08d9616ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497730"
---
# Get-AzureRmVM

## Synopsis
Ruft die Eigenschaften eines virtuellen Azure Resource Manager (Arm)-virtuellen Computers ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ListAllVirtualMachinesParamSet (Standard)
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVirtualMachineInResourceGroupParamSet
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetVirtualMachineInResourceGroupParamSet
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListNextLinkVirtualMachinesParamSet
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmVM** " Ruft die Modellansicht und die Instanzen Ansicht eines Azure Virtual Machine ab.
Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.
Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.
Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.

## Beispiele

### Beispiel 1: Abrufen von Modell-und Instanzen Ansichtseigenschaften
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

Mit diesem Befehl werden die Eigenschaften Modellansicht und Instanzen Ansicht des virtuellen Computers mit dem Namen VirtualMachine07 abgerufen.

### Beispiel 2: Abrufen von Instanzen Ansichtseigenschaften
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

Dieser Befehl ruft Eigenschaften des virtuellen Computers mit dem Namen VirtualMachine07 ab.
Mit diesem Befehl wird der *Status* -Parameter angegeben.
Daher ruft der Befehl nur die Eigenschaften der Instanzen Ansicht ab.

### Beispiel 3: Abrufen von Eigenschaften für alle virtuellen Computer in einer Ressourcengruppe
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

Dieser Befehl ruft Eigenschaften für alle virtuellen Computer in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.

### Beispiel 4: Abrufen aller virtuellen Computer in Ihrem Abonnement
```
PS C:\> Get-AzureRmVM
```

Dieser Befehl ruft alle virtuellen Computer in Ihrem Abonnement ab.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -DisplayHint
Bestimmt, wie das Objekt des virtuellen Computers angezeigt wird.

Gültige Werte sind:

– Kompakt: zeigt nur Eigenschaften der obersten Ebene an.

--Expand: zeigt alle Eigenschaften auf allen Ebenen an
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des abzurufenden virtuellen Computers an.

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nextlink
Gibt den nächsten Link an.

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView

## Notizen

## Verwandte Links

[Neu – AzureRmVM](./New-AzureRmVM.md)

[Remove-AzureRmVM](./Remove-AzureRmVM.md)

[Neustart-AzureRmVM](./Restart-AzureRmVM.md)

[Anfang-AzureRmVM](./Start-AzureRmVM.md)

[Stopp-AzureRmVM](./Stop-AzureRmVM.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)


