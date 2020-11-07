---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844635"
---
# Get-AzVM

## Synopsis
Ruft die Eigenschaften eines virtuellen Computers ab.

## Syntax

### ListAllVirtualMachinesParamSet (Standard)
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVirtualMachineInResourceGroupParamSet
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetVirtualMachineInResourceGroupParamSet
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListNextLinkVirtualMachinesParamSet
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzVM** " Ruft die Modellansicht und die Instanzen Ansicht eines Azure Virtual Machine ab.
Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.
Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.
Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.

## Beispiele

### Beispiel 1: Abrufen von Modell-und Instanzen Ansichtseigenschaften
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

Mit diesem Befehl werden die Eigenschaften Modellansicht und Instanzen Ansicht des virtuellen Computers mit dem Namen VirtualMachine07 abgerufen.

### Beispiel 2: Abrufen von Instanzen Ansichtseigenschaften
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

Dieser Befehl ruft Eigenschaften des virtuellen Computers mit dem Namen VirtualMachine07 ab.
Mit diesem Befehl wird der *Status* -Parameter angegeben.
Daher ruft der Befehl nur die Eigenschaften der Instanzen Ansicht ab.

### Beispiel 3: Abrufen von Eigenschaften für alle virtuellen Computer in einer Ressourcengruppe
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

Dieser Befehl ruft Eigenschaften für alle virtuellen Computer in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.

### Beispiel 4: Abrufen aller virtuellen Computer in Ihrem Abonnement
```
PS C:\> Get-AzVM
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView

## Notizen

## Verwandte Links

[Neu – AzVM](./New-AzVM.md)

[Remove-AzVM](./Remove-AzVM.md)

[Neustart-AzVM](./Restart-AzVM.md)

[Anfang-AzVM](./Start-AzVM.md)

[Stopp-AzVM](./Stop-AzVM.md)

[Update-AzVM](./Update-AzVM.md)


