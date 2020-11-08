---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006404"
---
# New-AzureVMImageDiskConfigSet

## Synopsis
Erstellt ein Festplatten-Konfigurationssatz Objekt.

## Syntax

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureVMImageDiskConfigSet** erstellt ein Festplatten-Konfigurationssatz Objekt, das an das Image Update-Cmdlet übergeben wird.
Sie kapselt die OSDiskConfig und das DataDiskConfig-Objekt.
Verwenden Sie die Cmdlets " **Satz-AzureVMImageOSDiskConfig** " und " **AzureVMImageDataDiskConfig** ", um die Eigenschaften des Betriebssystems festzulegen und die Datenträgereigenschaften für das Bild des virtuellen Computers festzulegen.

## Beispiele

### Beispiel 1: Erstellen eines Festplatten-Konfigurationssatz Objekts
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

Mit diesem Befehl wird ein Festplatten-Konfigurationssatz Objekt erstellt, und die Ergebnisse werden in der Variablen mit dem Namen $Disk gespeichert.
Nachdem die Datenträgerkonfiguration erstellt wurde, wird Sie verwendet, um die OSDiskConfig und DataDiskConfig festzulegen.
Anschließend wird der virtuelle Computer mit der Konfiguration aktualisiert.

## Parameter

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. WindowsAzure. Commands. Servicemanagement. Model. VirtualMachineImageDiskConfigSet

## Notizen

## Verwandte Links

[Get-AzureVMImageDiskConfigSet](./Get-AzureVMImageDiskConfigSet.md)

[Satz-AzureVMImageOSDiskConfig](./Set-AzureVMImageOSDiskConfig.md)

[Satz-AzureVMImageDataDiskConfig](./Set-AzureVMImageDataDiskConfig.md)


