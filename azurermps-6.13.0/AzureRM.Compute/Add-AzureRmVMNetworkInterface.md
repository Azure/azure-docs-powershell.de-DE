---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: a7e84ee56e09e2008d76ccd9177d320be7ada96a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663375"
---
# Add-AzureRmVMNetworkInterface

## Synopsis
Fügt eine Netzwerkschnittstelle zu einem virtuellen Computer hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### GetNicFromNicId (Standard)
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetNicFromNicObject
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureRmVMNetworkInterface** wird eine Netzwerkschnittstelle zu einem virtuellen Computer hinzugefügt.
Sie können eine Schnittstelle hinzufügen, wenn Sie einen virtuellen Computer erstellen oder einem vorhandenen virtuellen Computer einen hinzufügen.

## Beispiele

### Beispiel 1: Hinzufügen einer Netzwerkschnittstelle zu einem neuen virtuellen Computer
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.

### Beispiel 2: Hinzufügen einer Netzwerkschnittstelle zu einem vorhandenen virtuellen Computer
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet **Get-AzureRmVM** ab.
Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.
Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, eine Netzwerkschnittstelle hinzu.
Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.

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

### -ID
Gibt die ID einer Netzwerkschnittstelle an, die einem virtuellen Computer hinzugefügt werden soll.
Sie können das Cmdlet [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) verwenden, um eine Netzwerkschnittstelle zu erhalten.

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Network Interface
Gibt die Netzwerkschnittstelle an.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Primär
Gibt an, dass dieses Cmdlet die Netzwerkschnittstelle als primäre Schnittstelle hinzufügt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt ein lokales virtuelles Computerobjekt an, dem eine Netzwerkschnittstelle hinzugefügt werden soll.
Verwenden Sie zum Erstellen eines virtuellen Computers das Cmdlet **New-AzureRmVMConfig** .
Verwenden Sie zum Abrufen eines vorhandenen virtuellen Computers das Cmdlet **Get-AzureRmVM** .

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
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

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### System. String

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. Commands. Common. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]

### System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Notizen

## Verwandte Links

[Neu – AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmAvailabilitySet](./Get-AzureRmAvailabilitySet.md)
