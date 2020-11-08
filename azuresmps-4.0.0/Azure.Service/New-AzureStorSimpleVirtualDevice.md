---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005717"
---
# New-AzureStorSimpleVirtualDevice

## Synopsis
Erstellt ein virtuelles StorSimple-Gerät.

## Syntax

### CreateNewStorageAccount
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UseExistingStorageAccount
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureStorSimpleVirtualDevice** wird ein virtuelles StorSimple-Gerät erstellt.
Geben Sie einen Gerätenamen für das Gerät an.
Geben Sie die Details für virtuelles Netzwerk und Subnetz für das virtuelle Netzwerk im gleichen Abonnement an.
Der Geo sollte mit dem Geo übereinstimmen, in dem die StorSimple-Ressource erstellt wird.
Wenn Sie ein vorhandenes Speicherkonto für dieses virtuelle Gerät verwenden möchten, geben Sie den Namen an.
Wenn Sie ein neues Speicherkonto für dieses virtuelle Gerät erstellen möchten, geben Sie den Parameter *StorageAccountName* und *CreateNewStorageAccount* an.

## Beispiele

### Beispiel 1: Erstellen eines virtuellen Geräts mit einem neuen Konto und einem vorhandenen Netzwerk
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

Mit diesem Befehl wird ein virtuelles Gerät erstellt, das ein neues Speicherkonto und ein vorhandenes virtuelles Netzwerk verwendet.

### Beispiel 2: Erstellen eines virtuellen Geräts mit einem vorhandenen Konto und einem virtuellen Netzwerk
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

Mit diesem Befehl wird ein virtuelles Gerät erstellt, das ein vorhandenes Speicherkonto und ein vorhandenes virtuelles Netzwerk verwendet.

## Parameter

### -CreateNewStorageAccount
Gibt an, dass dieses Cmdlet ein neues Speicherkonto erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersistAzureVMOnFailrue
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

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### -StorageAccountName
Gibt den Namen eines speicherkontos an.

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Gibt den Namen eines virtuellen Subnetzes an.

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

### -VirtualDeviceName
Gibt einen Namen für das virtuelle Gerät an.

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

### -VirtualNetworkName
Gibt den Namen eines virtuellen Netzwerks an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Zeichenfolge
Dieses Cmdlet gibt die ID des Auftrags zurück, der das virtuelle Gerät erstellt.
Sie können diese ID verwenden, um den Fortschritt mithilfe des Get-AzureStorSimpleJob-Cmdlets zu verfolgen.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)

[Satz-AzureStorSimpleVirtualDevice](./Set-AzureStorSimpleVirtualDevice.md)


