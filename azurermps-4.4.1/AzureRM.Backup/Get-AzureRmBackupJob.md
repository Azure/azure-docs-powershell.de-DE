---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479366"
---
# Get-AzureRmBackupJob

## Synopsis
Ruft Backup-Aufträge ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Filterset (Standard)
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobsListFilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmBackupJob** " ruft Azure Backup-Aufträge für einen bestimmten Tresor ab.

## Beispiele

### Beispiel 1: Abrufen aller Aufträge in einem sicherungstresor
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.
Der Befehl speichert das Objekt in der $Vault Variablen.

Der zweite Befehl ruft alle Aufträge für den Tresor in $Vault ab.

### Beispiel 2: Abrufen abgeschlossener Aufträge
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Dieser Befehl ruft abgeschlossene Aufträge aus dem Tresor in $Vault ab.

### Beispiel 3: Abrufen von fehlgeschlagenen Aufträgen für die letzte Woche
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

Dieser Befehl ruft fehlerhafte Aufträge aus der letzten Woche aus dem Tresor in $Vault ab.
Der Parameter from gibt eine Uhrzeit *von* sieben Tagen in der Vergangenheit an.
Der Befehl gibt keinen Wert für den Parameter " *to" an* .
Daher wird der Standardwert für die aktuelle Uhrzeit verwendet.

### Beispiel 4: Abrufen der Sicherung für einen in Bearbeitung befindlichen Auftrag, der abgeschlossen ist
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Dieses Skript ruft den ersten Job ab, der gerade ausgeführt wird, bis der Auftrag abgeschlossen ist.

Die erste Zeile des Skripts Ruft alle Aufträge in $Vault ab, die in Bearbeitung sind, und speichert diese Aufträge dann in der $Jobs-Arrayvariablen.

In der zweiten Zeile wird der erste Auftrag aus dem $Jobs-Array in der $Job Variablen gespeichert.

In der dritten Zeile wird eine **while** -Schleife gestartet, die den aktuellen Status des Auftrags überprüft, bis der Vorgang abgeschlossen ist.
Für Informationen zum Schlüsselwort **while** geben Sie `Get-Help about_While` .

Die **while** -Schleife schreibt eine Nachricht in die Konsole, schläft zehn Sekunden lang und aktualisiert dann die $Job-Variable.
Das Skript aktualisiert die $Job-Variable unter Verwendung des vorhandenen Werts von $Job und des aktuellen Cmdlets, um den aktuellen Status des Auftrags abzurufen.
Wenn Sie Informationen zu den Windows PowerShell-Cmdlets erhalten, geben Sie `Get-Help Write-Host` und ein `Get-Help Start-Sleep` .

In der letzten Zeile des Skripts wird Ihnen mitgeteilt, dass das Skript beendet wurde.

## Parameter

### -Ab
Gibt den Anfang als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.
Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.
Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Gibt einen Auftrag an, den dieses Cmdlet erhält.
Verwenden Sie das Get-AzureRmBackupJob-Cmdlet, um ein **AzureRmBackupJob** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.
Die ID ist die **InstanceId** -Eigenschaft eines **AzureRmBackupJob** -Objekts.
Verwenden Sie Get-AzureRmBackupJob, um ein **AzureRmBackupJob** -Objekt zu erhalten.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vorgang
Gibt einen Vorgang der Aufträge an, die dieses Cmdlet erhält.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Backup 
- ConfigureBackup 
- DeleteBackupData 
- Registrieren 
- Wiederherstellungs 
- Schutz aufheben 
- Registrierung

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Gibt den Status der Aufträge an, die dieses Cmdlet erhält.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- InProgress
- Fehlgeschlagen
- Storniert
- Abbrechen
- Abgeschlossen
- CompletedWithWarnings 

Sie können diesen Parameter angeben, um alle in Bearbeitung befindlichen Aufträge oder alle fehlgeschlagenen Aufträge zu finden.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Gibt das Ende als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.
Der Standardwert ist die aktuelle Systemzeit.
Wenn Sie diesen Parameter angeben, müssen Sie auch den *from* -Parameter angeben.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Typ
Gibt den Typ des Containers an, für den das Cmdlet Sicherungsaufträge erhält.
Derzeit ist der einzige unterstützte Wert AzureVM.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Gibt den sicherungstresor an, für den dieses Cmdlet Aufträge erhält.
Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
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

### AzureRmBackupVault

## Ausgaben

### AzureRmBackupJob[]
Dieses Cmdlet gibt einen oder mehrere Sicherungsaufträge zurück.

## Notizen
* Keine

## Verwandte Links

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Stopp-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


