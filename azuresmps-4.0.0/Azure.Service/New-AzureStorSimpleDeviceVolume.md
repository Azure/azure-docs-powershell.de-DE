---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005729"
---
# New-AzureStorSimpleDeviceVolume

## Synopsis
Erstellt ein Volume in einem angegebenen Volumen Container.

## Syntax

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorSimpleDeviceVolume** erstellt ein Volume in einem angegebenen Volumen Container.
Mit diesem Cmdlet werden die einzelnen Volumes mit mindestens einem Zugriffssteuerungseintrag verknüpft.
Verwenden Sie zum Abrufen von **AccessControlRecord** -Objekten das Cmdlet **Get-AzureStorSimpleAccessControlRecord** .
Geben Sie einen Namen, eine Größe und einen AppType für das Volume an.
Geben Sie außerdem an, ob das Volume online erstellt werden soll, ob die Standardsicherung aktiviert werden soll und ob die Überwachung aktiviert werden soll.

## Beispiele

### Beispiel 1: Erstellen eines Volumes
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

Der erste Befehl ruft die Zugriffssteuerungseinträge in der StorSimple-Manager-Dienstkonfiguration mit dem Cmdlet **Get-AzureStorSimpleAccessControlRecord** ab und speichert Sie dann in der $AcrList-Variablen.

Der zweite Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** den Volumen Container mit dem Namen VolumeContainer07 für das Gerät mit dem Namen Contoso63-AppVm ab.
Der Befehl übergibt diesen Container mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Mit diesem Cmdlet wird das Volume erstellt.
Der Befehl gibt den Namen des Volumes, die Größe und die Zugriffssteuerungseinträge an, die in $AcrList gespeichert sind.
Mit diesem Befehl wird der Auftrag gestartet, und dann wird ein **TaskResponse** -Objekt zurückgegeben.
Verwenden Sie das Cmdlet " **Get-AzureStorSimpleTask** ", um den Status des Auftrags anzuzeigen.

### Beispiel 2: Erstellen eines Volumes ohne Access Controlaccess Control recordsaccess-Steuerelement
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

Dieser Befehl ruft mit dem Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** den Volumen Container mit dem Namen VolumeContainer01 für das Gerät mit dem Namen Contoso63-AppVm ab.
Der Befehl übergibt diesen Container mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Mit diesem Cmdlet wird das Volume erstellt.
Der Befehl gibt den Namen des Volumes, die Größe und einen leeren Wert für die Zugriffssteuerungsdaten Sätze an.
Dieser Befehl gibt den *WaitForComplete* -Parameter an, sodass nach dem Erstellen des Volumes ein **TaskStatusInfo** -Wert zurückgegeben wird.

Da der Befehl keine Zugriffssteuerungseinträge angibt, kann auf dieses Volume nicht zugegriffen werden.
Sie können später mithilfe des Cmdlets " **Satz-AzureStorSimpleDeviceVolume** " Zugriff hinzufügen.

## Parameter

### -AccessControlRecords
Gibt eine Liste der Zugriffssteuerungseinträge an, die dem Datenträger zugeordnet werden sollen.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceName
Gibt den Namen des StorSimple-Geräts an, auf dem das Volume erstellt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDefaultBackup
Gibt an, ob die Standardsicherung für das Volume aktiviert werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableMonitoring
Gibt an, ob die Überwachung des Volumes aktiviert werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Online
Gibt an, ob das Volume online erstellt werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt ein Azure-Profil an.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumeAppType
Gibt an, ob ein primäres oder Archiv Volume erstellt werden soll.
Gültige Werte sind: PrimaryVolume und ArchiveVolume.

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumeContainer
Gibt den Container als **DataContainer-Objekt an** , in dem das Volume erstellt werden soll.
Verwenden Sie das Cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** , um ein **VirtualDisk** -Objekt abzurufen.

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Volumename
Gibt einen Namen für das neue Volume an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumeSizeInBytes
Gibt die Datenträgergröße in Bytes an.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Gibt an, dass dieses Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.

```yaml
Type: SwitchParameter
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

### DataContainer, Liste\<AccessControlRecord\>
Dieses Cmdlet akzeptiert ein **DataContainer** -Objekt und eine Liste von **AccessControlRecord** -Objekten für das neue Volume.

## Ausgaben

### TaskStatusInfo
Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, wenn Sie den *WaitForComplete* -Parameter angeben.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Remove-AzureStorSimpleDeviceVolume](./Remove-AzureStorSimpleDeviceVolume.md)

[Satz-AzureStorSimpleDeviceVolume](./Set-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


