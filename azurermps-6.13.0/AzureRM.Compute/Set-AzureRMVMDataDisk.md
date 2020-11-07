---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 4ed0abb355bf7a755e5acaa36f8bb11e88d80c5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662832"
---
# Set-AzureRmVMDataDisk

## Synopsis
Ändert die Eigenschaften eines Daten Datenträgers einer virtuellen Maschine.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ChangeWithName
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ChangeWithLun
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmVMDataDisk** " ändert die Eigenschaften eines Datenträgers einer virtuellen Maschine.

## Beispiele

### Beispiel 1: Ändern des Cachemodus eines Datenlaufwerks
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

Der erste Befehl ruft den virtuellen Computer mit dem Namen ContosoVM07 mithilfe von **Get-AzureRmVM**.
Der Befehl speichert Sie in der $VM-Variablen.
Der zweite Befehl ändert den Zwischenspeicherungsmodus für den Datenträger mit dem Namen DataDisk01 auf dem virtuellen Computer in $VM.
Der Befehl übergibt das Ergebnis an das Update-AzureRmVM-Cmdlet, das Ihre Änderungen implementiert.
Eine Änderung des Einzahlungs Modus bewirkt, dass der virtuelle Computer neu gestartet wird.

## Parameter

### -Caching
Gibt den Zwischenspeichermodus des Datenträgers an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- ReadOnly
- ReadWrite der Standardwert ist ReadWrite.
Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.
Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
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

### -DiskSizeInGB
Gibt die Größe für den Datenträger in Gigabyte an.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Gibt die logische Einheitsnummer (LUN) des Daten Datenträgers an, der von diesem Cmdlet geändert wird.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Daten Datenträgers an, der von diesem Cmdlet geändert wird.

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Der Kontotyp des verwalteten Datenträgers des virtuellen Computers.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt den virtuellen Computer an, für den das Cmdlet einen Datenträger ändert.
Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.

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

### -WriteAccelerator
Gibt an, ob WriteAccelerator auf dem Datenträger aktiviert oder deaktiviert werden soll.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### System. String

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Notizen

## Verwandte Links

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)


