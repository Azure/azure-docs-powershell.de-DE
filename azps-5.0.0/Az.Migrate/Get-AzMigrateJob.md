---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180279"
---
# Get-AzMigrateJob

## Synopsis
Ruft den Status eines Azure-migrate-Auftrags ab.

## Syntax

### ListByName (Standard)
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ListById
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Beschreibung
Das Get-AzMigrateJob-Cmdlet retrives den Status eines Azure migrate-Auftrags.

## Beispiele

### Beispiel 1: Abrufen nach Auftrags-ID
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Damit wird ein Auftrag nach seiner ID abgerufen.

### Beispiel 2: Liste nach Ressourcengruppe und Projekt
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Dadurch werden alle Aufträge in einem Projekt abgerufen.

### Beispiel 3: Abrufen nach Ressourcengruppe, Projekt-und Auftragsname
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Dadurch wird eine bestimmte Aufgabe abgerufen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
OData-Filteroptionen.

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Gibt das Auftragsobjekt des replizierenden Servers an.
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Gibt die Auftrags-ID an, für die die Details abgerufen werden müssen.

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Jobname
Auftrags-ID

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Projekt-Nr.
Gibt das Azure-Migrationsprojekt an, in dem die Server repliziert werden.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectName
Der Name des migrieren-Projekts.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupID
Gibt die Ressourcengruppe des Azure-Migrationsprojekts im aktuellen Abonnement an.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, in der der Vault für Wiederherstellungsdienste vorhanden ist.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement-Nr
Azure-Abonnement-ID.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Inputobject <IJob> : gibt das Auftragsobjekt des replizierenden Servers an.
  - `[Location <String>]`: Ressourcen Standort
  - `[ActivityId <String>]`: Die Aktivitäts-ID.
  - `[AllowedAction <String[]>]`: Die zulässige Aktion des Auftrags.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Die betroffenen Objekteigenschaften wie Quellserver, Quell Wolke, Zielserver, Ziel Wolke usw. basierend auf den Details des Workflow Objekts.
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[EndTime <DateTime?>]`: Die Endzeit.
  - `[Error <IJobErrorDetails[]>]`: Die Fehler.
    - `[CreationTime <DateTime?>]`: Der Erstellungszeitpunkt des Auftragsfehlers.
    - `[ErrorLevel <String>]`: Fehlerstufe des Fehlers.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: Der Fehlercode.
    - `[ProviderErrorDetailErrorId <String>]`: Die Fehler-ID des Anbieters.
    - `[ProviderErrorDetailErrorMessage <String>]`: Die Fehlermeldung.
    - `[ProviderErrorDetailPossibleCaus <String>]`: Die möglichen Ursachen für den Fehler.
    - `[ProviderErrorDetailRecommendedAction <String>]`: Die empfohlene Aktion zur Behebung des Fehlers.
    - `[ServiceErrorDetailActivityId <String>]`: Aktivitäts-ID.
    - `[ServiceErrorDetailCode <String>]`: Fehlercode.
    - `[ServiceErrorDetailMessage <String>]`: Fehlermeldung.
    - `[ServiceErrorDetailPossibleCaus <String>]`: Mögliche Fehlerursachen.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Empfohlene Aktion zur Behebung des Fehlers.
    - `[TaskId <String>]`: Die ID der Aufgabe.
  - `[FriendlyName <String>]`: Der DisplayName.
  - `[ScenarioName <String>]`: Szenarioname.
  - `[StartTime <DateTime?>]`: Die Startzeit.
  - `[State <String>]`: Der Status des Auftrags. Es handelt sich um einen der folgenden Werte: NotStarted, InProgress, erfolgreich, fehlgeschlagen, storniert, angehalten oder andere.
  - `[StateDescription <String>]`: Die Beschreibung des Auftrags Zustands. Für z.b.-für den Zustand "erfolgreich" kann Description abgeschlossen, PartiallySucceeded, CompletedWithInformation oder übersprungen werden.
  - `[TargetInstanceType <String>]`: Der Typ des betroffenen Objekts, das die {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType}-Klasse ist.
  - `[TargetObjectId <String>]`: Die betroffene Objekt-ID.
  - `[TargetObjectName <String>]`: Der Name des betroffenen Objekts.
  - `[Task <IAsrTask[]>]`: Die Aufgaben.
    - `[AllowedAction <String[]>]`: Der Zustand/die Aktionen, die für diese Aufgabe gelten.
    - `[CustomDetailInstanceType <String>]`: Der Typ der Vorgangsdetails.
    - `[EndTime <DateTime?>]`: Die Endzeit.
    - `[Error <IJobErrorDetails[]>]`: Die Aufgaben Fehlerdetails.
    - `[FriendlyName <String>]`: Der Name.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Die untergeordneten Aufgaben.
    - `[GroupTaskCustomDetailInstanceType <String>]`: Der Typ der Vorgangsdetails.
    - `[Name <String>]`: Der Name der eindeutigen Aufgabe.
    - `[StartTime <DateTime?>]`: Die Startzeit.
    - `[State <String>]`: Der Zustand. Es handelt sich um einen der folgenden Werte: NotStarted, InProgress, erfolgreich, fehlgeschlagen, storniert, angehalten oder andere.
    - `[StateDescription <String>]`: Die Beschreibung des Vorgangs Zustands. Beispiel: für den Zustand "erfolgreich" kann Description abgeschlossen, PartiallySucceeded, CompletedWithInformation oder übersprungen werden.
    - `[TaskId <String>]`: Die ID.
    - `[TaskType <String>]`: Der Typ der Aufgabe. Details in der CustomDetails-Eigenschaft sind von diesem Typ abhängig.

## Verwandte Links

