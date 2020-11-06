---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d502596b8c5ddde576b5fd22ee31398b2c4e869a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504229"
---
# Stop-AzureRmBackupJob

## Synopsis
Bricht einen vorhandenen Backup-Auftrag ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### IdFiltersSet
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobFiltersSet
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Stop-AzureRmBackupJob** " wird ein vorhandener Azure Backup-Auftrag abgebrochen.
Verwenden Sie diesen Parameter, um einen Auftrag zu beenden, der zu lange dauert und andere Aktivitäten blockiert.

Sie können nur die folgenden Arten von Aufträgen stornieren: 

- Backup
- Wiederherstellungs

## Beispiele

### Beispiel 1: Beenden eines Sicherungsauftrags mithilfe einer Auftrags-ID
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.
Der Befehl speichert das Objekt in der $Vault Variablen.

Der zweite Befehl ruft mit dem Cmdlet **Get-AzureRmBackupJob** einen Sicherungsauftrag aus dem Tresor in $Vault ab.
Der Befehl speichert den Auftrag in der $Job-Variablen.
In diesem Beispiel ist nur ein Sicherungsvorgang im angegebenen Tresor vorhanden.

Der endgültige Befehl beendet den Auftrag mit der angegebenen ID.

### Beispiel 2: Beenden aller Wiederherstellungsvorgänge
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

Dieser Befehl ruft alle Wiederherstellungsvorgänge im Tresor in $Vault ab und übergibt diese dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet beendet die einzelnen Aufträge.

## Parameter

### -Job
Gibt einen Auftrag an, den dieses Cmdlet abbricht.
Verwenden Sie das Get-AzureRmBackupJob-Cmdlet, um ein **AzureRmBackupJob** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Gibt einen Auftrag an, den dieses Cmdlet abbricht.
Verwenden Sie das Get-AzureRmBackupJob-Cmdlet, um ein **AzureRmBackupJob** -Objekt zu erhalten.

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Gibt den sicherungstresor an, in dem dieses Cmdlet einen Auftrag abbricht.
Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### AzureRmBackupJob

## Ausgaben

### Keine

## Notizen

## Verwandte Links

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


