---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479390"
---
# Backup-AzureRmBackupItem

## Synopsis
Startet eine Sicherung für ein Sicherungselement.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Backup-AzureRmBackupItem** startet eine Sicherung für ein geschütztes Azure-Sicherungselement, das nicht an den Sicherungszeitplan gebunden ist.
Sie können eine erste Sicherung unmittelbar nach dem Aktivieren des Schutzes durchführen oder eine Sicherung starten, nachdem eine geplante Sicherung fehlschlägt.

Wenn ein vorhandener Backup-Auftrag ausgeführt wird, schlägt dieses Cmdlet fehl.

## Beispiele

### Beispiel 1: Starten der Sicherung eines virtuellen Computers
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.
Der Befehl speichert das Objekt in der $Vault Variablen.

Der zweite Befehl ruft mithilfe des Get-AzureRmBackupContainer-Cmdlets einen Container ab, der den angegebenen Namen im Tresor in $Vault aufweist.
Der Befehl speichert das Objekt in der $Container Variablen.

Der letzte Befehl ruft die Sicherungselemente in $Container mithilfe des Get-AzureRmBackupItem-Cmdlets ab.
Der Befehl übergibt die Elemente mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet beginnt mit dem Sichern des virtuellen Computers im Container.

## Parameter

### -Item
Gibt ein Sicherungselement an, für das dieses Cmdlet einen Sicherungsvorgang startet.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### AzureRMBackupItem

## Ausgaben

### AzureRmBackupJob

## Notizen

## Verwandte Links

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Wiederherstellen – AzureRmBackupItem](./Restore-AzureRmBackupItem.md)


