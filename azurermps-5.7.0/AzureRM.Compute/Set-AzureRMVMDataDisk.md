---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499026"
---
# Set-AzureRmVMDataDisk

## Synopsis
Ändert die Eigenschaften eines Daten Datenträgers einer virtuellen Maschine.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ChangeWithName
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### ChangeWithLun
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
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
Eine Änderung des Cachemodus bewirkt, dass der virtuelle Computer neu gestartet wird.

## Parameter

### -Caching
Gibt den Zwischenspeichermodus des Datenträgers an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- ReadOnly
- ReadWrite

Der Standardwert ist ReadWrite.
Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.

Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Gibt die Größe für den Datenträger in Gigabyte an.

```yaml
Type: Int32
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
Type: Int32
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
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt den virtuellen Computer an, für den das Cmdlet einen Datenträger ändert.
Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.

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

[Update-AzureRmVM](./Update-AzureRmVM.md)


