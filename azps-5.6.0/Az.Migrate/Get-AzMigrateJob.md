---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: 9521e069f0b472353403a16caffad86e1147c1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934091"
---
# Get-AzMigrateJob

## SYNOPSIS
Ruft den Status eines Azure Migrate-Auftrags ab.

## SYNTAX

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

## BESCHREIBUNG
Das Get-AzMigrateJob cmdlet wiederholt den Status eines Azure Migrate-Auftrags.

## BEISPIELE

### Beispiel 1: Nach Auftrags-ID erhalten
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

Dadurch wird ein Auftrag mit der ID abgerufen.

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

Dadurch werden alle Aufträge in einem Projekt erhalten.

### Beispiel 3: Nach Ressourcengruppe, Projekt- und Auftragsname suchen
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

Dies erhält einen bestimmten Auftrag.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -InputObject
Gibt das Auftragsobjekt des replikationsservers an.
Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.

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

### -JobID
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

### -JobName
Auftragsbezeichner

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

### -ProjectID
Gibt das Azure Migrate Project an, in dem Server repliziert werden.

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
Der Name des Migrierenprojekts.

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
Gibt die Ressourcengruppe des Azure Migrate Project im aktuellen Abonnement an.

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
Der Name der Ressourcengruppe, in der sich der Wiederherstellungsdiensttresor befindet.

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

### -SubscriptionId
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob

## NOTIZEN

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält. Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.


INPUTOBJECT <IJob> : Gibt das Auftragsobjekt des replikationsservers an.
  - `[Location <String>]`: Ressourcenspeicherort
  - `[ActivityId <String>]`: Die Aktivitäts-ID.
  - `[AllowedAction <String[]>]`: Die Aktion "Zulässig" des Auftrags.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Die betroffenen Objekteigenschaften wie Quellserver, Quellwolke, Zielserver, Zielwolke usw. basierend auf den Details des Workflowobjekts.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.
  - `[EndTime <DateTime?>]`: Die Endzeit.
  - `[Error <IJobErrorDetails[]>]`: Die Fehler.
    - `[CreationTime <DateTime?>]`: Die Erstellungszeit des Auftragsfehlers.
    - `[ErrorLevel <String>]`: Fehlerebene.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: Der Fehlercode.
    - `[ProviderErrorDetailErrorId <String>]`: Die Fehler-ID des Anbieters.
    - `[ProviderErrorDetailErrorMessage <String>]`: Die Fehlermeldung.
    - `[ProviderErrorDetailPossibleCaus <String>]`: Die möglichen Ursachen für den Fehler.
    - `[ProviderErrorDetailRecommendedAction <String>]`: Die empfohlene Aktion zum Beheben des Fehlers.
    - `[ServiceErrorDetailActivityId <String>]`: Aktivitäts-ID.
    - `[ServiceErrorDetailCode <String>]`: Fehlercode.
    - `[ServiceErrorDetailMessage <String>]`: Fehlermeldung.
    - `[ServiceErrorDetailPossibleCaus <String>]`: Mögliche Fehlerursachen.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Empfohlene Aktion zum Beheben von Fehlern.
    - `[TaskId <String>]`: Die ID der Aufgabe.
  - `[FriendlyName <String>]`: Der Anzeigename.
  - `[ScenarioName <String>]`: Der Szenarioname.
  - `[StartTime <DateTime?>]`: Die Startzeit.
  - `[State <String>]`: Der Status des Auftrags. Es ist einer dieser Werte – NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended oder Other.
  - `[StateDescription <String>]`: Die Beschreibung des Zustands des Auftrags. Für z. B. – Für den Status "Erfolgreich" kann die Beschreibung abgeschlossen, Teilweisesukceed, CompletedWithInformation oder Übersprungen sein.
  - `[TargetInstanceType <String>]`: Der Typ des betroffenen Objekts der {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}-Klasse.
  - `[TargetObjectId <String>]`: Die betroffene Objekt-ID.
  - `[TargetObjectName <String>]`: Der Name des betroffenen Objekts.
  - `[Task <IAsrTask[]>]`: Die Aufgaben.
    - `[AllowedAction <String[]>]`: Der Zustand/die Aktionen, die für diese Aufgabe gelten.
    - `[CustomDetailInstanceType <String>]`: Der Typ der Vorgangsdetails.
    - `[EndTime <DateTime?>]`: Die Endzeit.
    - `[Error <IJobErrorDetails[]>]`: Die Details des Vorgangsfehlers.
    - `[FriendlyName <String>]`: Der Name.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Die untergeordneten Aufgaben.
    - `[GroupTaskCustomDetailInstanceType <String>]`: Der Typ der Vorgangsdetails.
    - `[Name <String>]`: Der eindeutige Vorgangsname.
    - `[StartTime <DateTime?>]`: Die Startzeit.
    - `[State <String>]`: Der Bundesland. Es ist einer dieser Werte – NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended oder Other.
    - `[StateDescription <String>]`: Die Beschreibung des Vorgangszustands. Beispiel: Für den Status "Erfolgreich" kann die Beschreibung "Completed", "PartiallySucceeded", "CompletedWithInformation" oder "Skipped" sein.
    - `[TaskId <String>]`: Die ID.
    - `[TaskType <String>]`: Der Vorgangstyp. Details in der CustomDetails-Eigenschaft hängen von diesem Typ ab.

## VERWANDTE LINKS

