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
# <span data-ttu-id="8af4d-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="8af4d-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="8af4d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8af4d-102">SYNOPSIS</span></span>
<span data-ttu-id="8af4d-103">Ruft den Status eines Azure-migrate-Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="8af4d-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="8af4d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8af4d-104">SYNTAX</span></span>

### <span data-ttu-id="8af4d-105">ListByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8af4d-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8af4d-106">GetById</span><span class="sxs-lookup"><span data-stu-id="8af4d-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8af4d-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8af4d-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8af4d-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="8af4d-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8af4d-109">ListById</span><span class="sxs-lookup"><span data-stu-id="8af4d-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8af4d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8af4d-110">DESCRIPTION</span></span>
<span data-ttu-id="8af4d-111">Das Get-AzMigrateJob-Cmdlet retrives den Status eines Azure migrate-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="8af4d-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="8af4d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8af4d-112">EXAMPLES</span></span>

### <span data-ttu-id="8af4d-113">Beispiel 1: Abrufen nach Auftrags-ID</span><span class="sxs-lookup"><span data-stu-id="8af4d-113">Example 1: Get By Job Id</span></span>
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

<span data-ttu-id="8af4d-114">Damit wird ein Auftrag nach seiner ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8af4d-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="8af4d-115">Beispiel 2: Liste nach Ressourcengruppe und Projekt</span><span class="sxs-lookup"><span data-stu-id="8af4d-115">Example 2: List by resource group and project</span></span>
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

<span data-ttu-id="8af4d-116">Dadurch werden alle Aufträge in einem Projekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8af4d-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="8af4d-117">Beispiel 3: Abrufen nach Ressourcengruppe, Projekt-und Auftragsname</span><span class="sxs-lookup"><span data-stu-id="8af4d-117">Example 3: Get by resource group, project and job name</span></span>
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

<span data-ttu-id="8af4d-118">Dadurch wird eine bestimmte Aufgabe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8af4d-118">This gets a specific job.</span></span>

## <span data-ttu-id="8af4d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="8af4d-119">PARAMETERS</span></span>

### <span data-ttu-id="8af4d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af4d-120">-DefaultProfile</span></span>
<span data-ttu-id="8af4d-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8af4d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af4d-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="8af4d-122">-Filter</span></span>
<span data-ttu-id="8af4d-123">OData-Filteroptionen.</span><span class="sxs-lookup"><span data-stu-id="8af4d-123">OData filter options.</span></span>

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

### <span data-ttu-id="8af4d-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8af4d-124">-InputObject</span></span>
<span data-ttu-id="8af4d-125">Gibt das Auftragsobjekt des replizierenden Servers an.</span><span class="sxs-lookup"><span data-stu-id="8af4d-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="8af4d-126">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8af4d-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8af4d-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="8af4d-127">-JobID</span></span>
<span data-ttu-id="8af4d-128">Gibt die Auftrags-ID an, für die die Details abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8af4d-128">Specifies the job id for which the details needs to be retrieved.</span></span>

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

### <span data-ttu-id="8af4d-129">-Jobname</span><span class="sxs-lookup"><span data-stu-id="8af4d-129">-JobName</span></span>
<span data-ttu-id="8af4d-130">Auftrags-ID</span><span class="sxs-lookup"><span data-stu-id="8af4d-130">Job identifier</span></span>

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

### <span data-ttu-id="8af4d-131">-Projekt-Nr.</span><span class="sxs-lookup"><span data-stu-id="8af4d-131">-ProjectID</span></span>
<span data-ttu-id="8af4d-132">Gibt das Azure-Migrationsprojekt an, in dem die Server repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="8af4d-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="8af4d-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="8af4d-133">-ProjectName</span></span>
<span data-ttu-id="8af4d-134">Der Name des migrieren-Projekts.</span><span class="sxs-lookup"><span data-stu-id="8af4d-134">The name of the migrate project.</span></span>

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

### <span data-ttu-id="8af4d-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="8af4d-135">-ResourceGroupID</span></span>
<span data-ttu-id="8af4d-136">Gibt die Ressourcengruppe des Azure-Migrationsprojekts im aktuellen Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="8af4d-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="8af4d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af4d-137">-ResourceGroupName</span></span>
<span data-ttu-id="8af4d-138">Der Name der Ressourcengruppe, in der der Vault für Wiederherstellungsdienste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8af4d-138">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="8af4d-139">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8af4d-139">-SubscriptionId</span></span>
<span data-ttu-id="8af4d-140">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="8af4d-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8af4d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af4d-141">CommonParameters</span></span>
<span data-ttu-id="8af4d-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8af4d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af4d-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8af4d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af4d-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8af4d-144">INPUTS</span></span>

## <span data-ttu-id="8af4d-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8af4d-145">OUTPUTS</span></span>

### <span data-ttu-id="8af4d-146">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="8af4d-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="8af4d-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="8af4d-147">NOTES</span></span>

<span data-ttu-id="8af4d-148">Aliase</span><span class="sxs-lookup"><span data-stu-id="8af4d-148">ALIASES</span></span>

<span data-ttu-id="8af4d-149">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8af4d-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8af4d-150">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8af4d-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8af4d-151">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="8af4d-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8af4d-152">Inputobject <IJob> : gibt das Auftragsobjekt des replizierenden Servers an.</span><span class="sxs-lookup"><span data-stu-id="8af4d-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="8af4d-153">`[Location <String>]`: Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="8af4d-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="8af4d-154">`[ActivityId <String>]`: Die Aktivitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="8af4d-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="8af4d-155">`[AllowedAction <String[]>]`: Die zulässige Aktion des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="8af4d-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="8af4d-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Die betroffenen Objekteigenschaften wie Quellserver, Quell Wolke, Zielserver, Ziel Wolke usw. basierend auf den Details des Workflow Objekts.</span><span class="sxs-lookup"><span data-stu-id="8af4d-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="8af4d-157">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8af4d-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8af4d-158">`[EndTime <DateTime?>]`: Die Endzeit.</span><span class="sxs-lookup"><span data-stu-id="8af4d-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="8af4d-159">`[Error <IJobErrorDetails[]>]`: Die Fehler.</span><span class="sxs-lookup"><span data-stu-id="8af4d-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="8af4d-160">`[CreationTime <DateTime?>]`: Der Erstellungszeitpunkt des Auftragsfehlers.</span><span class="sxs-lookup"><span data-stu-id="8af4d-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="8af4d-161">`[ErrorLevel <String>]`: Fehlerstufe des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="8af4d-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="8af4d-162">`[ProviderErrorDetailErrorCode <Int32?>]`: Der Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8af4d-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="8af4d-163">`[ProviderErrorDetailErrorId <String>]`: Die Fehler-ID des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="8af4d-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="8af4d-164">`[ProviderErrorDetailErrorMessage <String>]`: Die Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="8af4d-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="8af4d-165">`[ProviderErrorDetailPossibleCaus <String>]`: Die möglichen Ursachen für den Fehler.</span><span class="sxs-lookup"><span data-stu-id="8af4d-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="8af4d-166">`[ProviderErrorDetailRecommendedAction <String>]`: Die empfohlene Aktion zur Behebung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="8af4d-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="8af4d-167">`[ServiceErrorDetailActivityId <String>]`: Aktivitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="8af4d-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="8af4d-168">`[ServiceErrorDetailCode <String>]`: Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8af4d-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="8af4d-169">`[ServiceErrorDetailMessage <String>]`: Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="8af4d-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="8af4d-170">`[ServiceErrorDetailPossibleCaus <String>]`: Mögliche Fehlerursachen.</span><span class="sxs-lookup"><span data-stu-id="8af4d-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="8af4d-171">`[ServiceErrorDetailRecommendedAction <String>]`: Empfohlene Aktion zur Behebung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="8af4d-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="8af4d-172">`[TaskId <String>]`: Die ID der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="8af4d-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="8af4d-173">`[FriendlyName <String>]`: Der DisplayName.</span><span class="sxs-lookup"><span data-stu-id="8af4d-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="8af4d-174">`[ScenarioName <String>]`: Szenarioname.</span><span class="sxs-lookup"><span data-stu-id="8af4d-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="8af4d-175">`[StartTime <DateTime?>]`: Die Startzeit.</span><span class="sxs-lookup"><span data-stu-id="8af4d-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="8af4d-176">`[State <String>]`: Der Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="8af4d-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="8af4d-177">Es handelt sich um einen der folgenden Werte: NotStarted, InProgress, erfolgreich, fehlgeschlagen, storniert, angehalten oder andere.</span><span class="sxs-lookup"><span data-stu-id="8af4d-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="8af4d-178">`[StateDescription <String>]`: Die Beschreibung des Auftrags Zustands.</span><span class="sxs-lookup"><span data-stu-id="8af4d-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="8af4d-179">Für z.b.-für den Zustand "erfolgreich" kann Description abgeschlossen, PartiallySucceeded, CompletedWithInformation oder übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="8af4d-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="8af4d-180">`[TargetInstanceType <String>]`: Der Typ des betroffenen Objekts, das die {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType}-Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="8af4d-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="8af4d-181">`[TargetObjectId <String>]`: Die betroffene Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="8af4d-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="8af4d-182">`[TargetObjectName <String>]`: Der Name des betroffenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="8af4d-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="8af4d-183">`[Task <IAsrTask[]>]`: Die Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="8af4d-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="8af4d-184">`[AllowedAction <String[]>]`: Der Zustand/die Aktionen, die für diese Aufgabe gelten.</span><span class="sxs-lookup"><span data-stu-id="8af4d-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="8af4d-185">`[CustomDetailInstanceType <String>]`: Der Typ der Vorgangsdetails.</span><span class="sxs-lookup"><span data-stu-id="8af4d-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="8af4d-186">`[EndTime <DateTime?>]`: Die Endzeit.</span><span class="sxs-lookup"><span data-stu-id="8af4d-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="8af4d-187">`[Error <IJobErrorDetails[]>]`: Die Aufgaben Fehlerdetails.</span><span class="sxs-lookup"><span data-stu-id="8af4d-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="8af4d-188">`[FriendlyName <String>]`: Der Name.</span><span class="sxs-lookup"><span data-stu-id="8af4d-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="8af4d-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Die untergeordneten Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="8af4d-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="8af4d-190">`[GroupTaskCustomDetailInstanceType <String>]`: Der Typ der Vorgangsdetails.</span><span class="sxs-lookup"><span data-stu-id="8af4d-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="8af4d-191">`[Name <String>]`: Der Name der eindeutigen Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="8af4d-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="8af4d-192">`[StartTime <DateTime?>]`: Die Startzeit.</span><span class="sxs-lookup"><span data-stu-id="8af4d-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="8af4d-193">`[State <String>]`: Der Zustand.</span><span class="sxs-lookup"><span data-stu-id="8af4d-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="8af4d-194">Es handelt sich um einen der folgenden Werte: NotStarted, InProgress, erfolgreich, fehlgeschlagen, storniert, angehalten oder andere.</span><span class="sxs-lookup"><span data-stu-id="8af4d-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="8af4d-195">`[StateDescription <String>]`: Die Beschreibung des Vorgangs Zustands.</span><span class="sxs-lookup"><span data-stu-id="8af4d-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="8af4d-196">Beispiel: für den Zustand "erfolgreich" kann Description abgeschlossen, PartiallySucceeded, CompletedWithInformation oder übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="8af4d-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="8af4d-197">`[TaskId <String>]`: Die ID.</span><span class="sxs-lookup"><span data-stu-id="8af4d-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="8af4d-198">`[TaskType <String>]`: Der Typ der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="8af4d-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="8af4d-199">Details in der CustomDetails-Eigenschaft sind von diesem Typ abhängig.</span><span class="sxs-lookup"><span data-stu-id="8af4d-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="8af4d-200">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8af4d-200">RELATED LINKS</span></span>

