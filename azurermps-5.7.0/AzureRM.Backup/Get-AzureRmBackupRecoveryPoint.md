---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 2805ebfd5849306dadb4cf913660c8fac1602d79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497762"
---
# Get-AzureRmBackupRecoveryPoint

## Synopsis
Ruft die Wiederherstellungspunkte für ein gesichertes Element ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmBackupRecoveryPoint** " Ruft die Wiederherstellungspunkte für ein gesichertes Azure-Sicherungselement ab.
Nachdem ein Element gesichert wurde, speichert Backup einen oder mehrere Wiederherstellungspunkte.

## Beispiele

### Beispiel 1: Abrufen von Wiederherstellungspunkten für ein Element
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.
Der Befehl speichert das Objekt in der $Vault Variablen.

Der zweite Befehl ruft mit dem Cmdlet **Get-AzureRmBackupContainer** einen Container mit dem angegebenen Namen im Tresor in $Vault ab.
Der Befehl speichert das Objekt in der $Container Variablen.

Der dritte Befehl ruft das Sicherungselement im Container in $Container mit dem Cmdlet **Get-AzureRmBackupItem** ab.
Der Befehl speichert das Objekt in der $BackupItem Variablen.

Der endgültige Befehl ruft Wiederherstellungspunkte für das Element in $BackupItem ab.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Item
Gibt das Element an, für das dieses Cmdlet Wiederherstellungspunkte erhält.
Verwenden Sie zum Abrufen eines **AzureRmBackupItem** das Get-AzureRmBackupItem-Cmdlet.

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryPointId
Gibt die ID eines Wiederherstellungspunkts an, den dieses Cmdlet erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### AzureRmBackupItem

## Ausgaben

### AzureRmBackupRecoveryPoint

## Notizen

## Verwandte Links

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


