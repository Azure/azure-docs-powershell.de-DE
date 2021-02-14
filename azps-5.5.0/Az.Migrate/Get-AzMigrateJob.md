---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157420"
---
# <span data-ttu-id="1d175-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="1d175-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="1d175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d175-102">SYNOPSIS</span></span>
<span data-ttu-id="1d175-103">Ruft den Status eines Azure Migrate-Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="1d175-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="1d175-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d175-104">SYNTAX</span></span>

### <span data-ttu-id="1d175-105">ListByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d175-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1d175-106">GetById</span><span class="sxs-lookup"><span data-stu-id="1d175-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1d175-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d175-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1d175-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="1d175-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1d175-109">ListById</span><span class="sxs-lookup"><span data-stu-id="1d175-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1d175-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d175-110">DESCRIPTION</span></span>
<span data-ttu-id="1d175-111">Das Get-AzMigrateJob cmdlet wiederholt den Status eines Azure Migrate-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="1d175-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="1d175-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d175-112">EXAMPLES</span></span>

### <span data-ttu-id="1d175-113">Beispiel 1: Auftrags-ID erhalten</span><span class="sxs-lookup"><span data-stu-id="1d175-113">Example 1: Get By Job Id</span></span>
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

<span data-ttu-id="1d175-114">Dadurch wird ein Auftrag nach seiner ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1d175-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="1d175-115">Beispiel 2: Auflisten nach Ressourcengruppe und Projekt</span><span class="sxs-lookup"><span data-stu-id="1d175-115">Example 2: List by resource group and project</span></span>
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

<span data-ttu-id="1d175-116">Dadurch werden alle Aufträge in einem Projekt erhalten.</span><span class="sxs-lookup"><span data-stu-id="1d175-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="1d175-117">Beispiel 3: Erhalten nach Ressourcengruppe, Projekt- und Auftragsname</span><span class="sxs-lookup"><span data-stu-id="1d175-117">Example 3: Get by resource group, project and job name</span></span>
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

<span data-ttu-id="1d175-118">Dies erhält einen bestimmten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="1d175-118">This gets a specific job.</span></span>

## <span data-ttu-id="1d175-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d175-119">PARAMETERS</span></span>

### <span data-ttu-id="1d175-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d175-120">-DefaultProfile</span></span>
<span data-ttu-id="1d175-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d175-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d175-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="1d175-122">-Filter</span></span>
<span data-ttu-id="1d175-123">OData-Filteroptionen.</span><span class="sxs-lookup"><span data-stu-id="1d175-123">OData filter options.</span></span>

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

### <span data-ttu-id="1d175-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d175-124">-InputObject</span></span>
<span data-ttu-id="1d175-125">Gibt das Auftragsobjekt des replizierbaren Servers an.</span><span class="sxs-lookup"><span data-stu-id="1d175-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="1d175-126">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1d175-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1d175-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="1d175-127">-JobID</span></span>
<span data-ttu-id="1d175-128">Gibt die Auftrags-ID an, für die die Details abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1d175-128">Specifies the job id for which the details needs to be retrieved.</span></span>

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

### <span data-ttu-id="1d175-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="1d175-129">-JobName</span></span>
<span data-ttu-id="1d175-130">Auftrags-ID</span><span class="sxs-lookup"><span data-stu-id="1d175-130">Job identifier</span></span>

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

### <span data-ttu-id="1d175-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="1d175-131">-ProjectID</span></span>
<span data-ttu-id="1d175-132">Gibt das Azure Migrate Project an, in das Server repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="1d175-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="1d175-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="1d175-133">-ProjectName</span></span>
<span data-ttu-id="1d175-134">Der Name des Projekts zum Migrieren.</span><span class="sxs-lookup"><span data-stu-id="1d175-134">The name of the migrate project.</span></span>

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

### <span data-ttu-id="1d175-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="1d175-135">-ResourceGroupID</span></span>
<span data-ttu-id="1d175-136">Gibt die Ressourcengruppe des Azure-Projekts "Migrieren" im aktuellen Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="1d175-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="1d175-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d175-137">-ResourceGroupName</span></span>
<span data-ttu-id="1d175-138">Der Name der Ressourcengruppe, in der sich der Tresor der Wiederherstellungsdienste befindet.</span><span class="sxs-lookup"><span data-stu-id="1d175-138">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="1d175-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d175-139">-SubscriptionId</span></span>
<span data-ttu-id="1d175-140">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1d175-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1d175-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d175-141">CommonParameters</span></span>
<span data-ttu-id="1d175-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d175-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d175-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d175-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d175-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d175-144">INPUTS</span></span>

## <span data-ttu-id="1d175-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d175-145">OUTPUTS</span></span>

### <span data-ttu-id="1d175-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="1d175-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="1d175-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d175-147">NOTES</span></span>

<span data-ttu-id="1d175-148">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1d175-148">ALIASES</span></span>

<span data-ttu-id="1d175-149">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1d175-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1d175-150">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1d175-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1d175-151">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1d175-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1d175-152">INPUTOBJECT <IJob> : Gibt das Auftragsobjekt des replizierbaren Servers an.</span><span class="sxs-lookup"><span data-stu-id="1d175-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="1d175-153">`[Location <String>]`: Ressourcenstandort</span><span class="sxs-lookup"><span data-stu-id="1d175-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="1d175-154">`[ActivityId <String>]`: Die Aktivitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="1d175-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="1d175-155">`[AllowedAction <String[]>]`: Die Aktion "Zulässig" für den Auftrag.</span><span class="sxs-lookup"><span data-stu-id="1d175-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="1d175-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Die betroffenen Objekteigenschaften wie Quellserver, Quellwolke, Zielserver, Zielwolke usw. basierend auf den Details des Workflowobjekts.</span><span class="sxs-lookup"><span data-stu-id="1d175-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="1d175-157">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="1d175-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1d175-158">`[EndTime <DateTime?>]`: Die Endzeit.</span><span class="sxs-lookup"><span data-stu-id="1d175-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="1d175-159">`[Error <IJobErrorDetails[]>]`: Die Fehler.</span><span class="sxs-lookup"><span data-stu-id="1d175-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="1d175-160">`[CreationTime <DateTime?>]`: Die Erstellungszeit des Auftragsfehlers.</span><span class="sxs-lookup"><span data-stu-id="1d175-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="1d175-161">`[ErrorLevel <String>]`: Fehlerebene.</span><span class="sxs-lookup"><span data-stu-id="1d175-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="1d175-162">`[ProviderErrorDetailErrorCode <Int32?>]`: Der Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1d175-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="1d175-163">`[ProviderErrorDetailErrorId <String>]`: Die Fehler-ID des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="1d175-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="1d175-164">`[ProviderErrorDetailErrorMessage <String>]`: Die Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="1d175-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="1d175-165">`[ProviderErrorDetailPossibleCaus <String>]`: Die möglichen Ursachen für den Fehler.</span><span class="sxs-lookup"><span data-stu-id="1d175-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="1d175-166">`[ProviderErrorDetailRecommendedAction <String>]`: Die empfohlene Aktion zum Beheben des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="1d175-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="1d175-167">`[ServiceErrorDetailActivityId <String>]`: Aktivitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="1d175-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="1d175-168">`[ServiceErrorDetailCode <String>]`: Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1d175-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="1d175-169">`[ServiceErrorDetailMessage <String>]`: Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="1d175-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="1d175-170">`[ServiceErrorDetailPossibleCaus <String>]`: Mögliche Fehlerursachen.</span><span class="sxs-lookup"><span data-stu-id="1d175-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="1d175-171">`[ServiceErrorDetailRecommendedAction <String>]`: Empfohlene Aktion zum Beheben von Fehlern.</span><span class="sxs-lookup"><span data-stu-id="1d175-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="1d175-172">`[TaskId <String>]`: Die ID des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1d175-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="1d175-173">`[FriendlyName <String>]`: Der Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="1d175-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="1d175-174">`[ScenarioName <String>]`: Der ScenarioName.</span><span class="sxs-lookup"><span data-stu-id="1d175-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="1d175-175">`[StartTime <DateTime?>]`: Die Startzeit.</span><span class="sxs-lookup"><span data-stu-id="1d175-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="1d175-176">`[State <String>]`: Der Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="1d175-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="1d175-177">Dies ist einer der folgenden Werte: "NotStarted", "InProgress", "Succeeded", "Failed", "Cancelled", "Suspended" oder "Other".</span><span class="sxs-lookup"><span data-stu-id="1d175-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="1d175-178">`[StateDescription <String>]`: Die Beschreibung des Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="1d175-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="1d175-179">Beispiel: "- Für den Status "Succeeded" kann die Beschreibung abgeschlossen, teilweise bzw. übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="1d175-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="1d175-180">`[TargetInstanceType <String>]`: Der Typ des betroffenen Objekts, der von der {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType}-Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="1d175-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="1d175-181">`[TargetObjectId <String>]`: Die betroffene Objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="1d175-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="1d175-182">`[TargetObjectName <String>]`: Der Name des betroffenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="1d175-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="1d175-183">`[Task <IAsrTask[]>]`: Die Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="1d175-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="1d175-184">`[AllowedAction <String[]>]`: Der Zustand/die Aktionen, die für diese Aufgabe gelten.</span><span class="sxs-lookup"><span data-stu-id="1d175-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="1d175-185">`[CustomDetailInstanceType <String>]`: Der Typ der Vorgangsdetails.</span><span class="sxs-lookup"><span data-stu-id="1d175-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="1d175-186">`[EndTime <DateTime?>]`: Die Endzeit.</span><span class="sxs-lookup"><span data-stu-id="1d175-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="1d175-187">`[Error <IJobErrorDetails[]>]`: Die Details des Aufgabenfehlers.</span><span class="sxs-lookup"><span data-stu-id="1d175-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="1d175-188">`[FriendlyName <String>]`: Der Name.</span><span class="sxs-lookup"><span data-stu-id="1d175-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="1d175-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Die untergeordneten Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="1d175-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="1d175-190">`[GroupTaskCustomDetailInstanceType <String>]`: Der Typ der Vorgangsdetails.</span><span class="sxs-lookup"><span data-stu-id="1d175-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="1d175-191">`[Name <String>]`: Der eindeutige Aufgabenname.</span><span class="sxs-lookup"><span data-stu-id="1d175-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="1d175-192">`[StartTime <DateTime?>]`: Die Startzeit.</span><span class="sxs-lookup"><span data-stu-id="1d175-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="1d175-193">`[State <String>]`: Der Zustand.</span><span class="sxs-lookup"><span data-stu-id="1d175-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="1d175-194">Dies ist einer der folgenden Werte: "NotStarted", "InProgress", "Succeeded", "Failed", "Cancelled", "Suspended" oder "Other".</span><span class="sxs-lookup"><span data-stu-id="1d175-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="1d175-195">`[StateDescription <String>]`: Beschreibung des Vorgangszustands.</span><span class="sxs-lookup"><span data-stu-id="1d175-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="1d175-196">Beispiel: Für den Status "Succeeded" kann die Beschreibung "Completed", "PartiallySucceeded", "CompletedWithInformation" oder "Skipped" sein.</span><span class="sxs-lookup"><span data-stu-id="1d175-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="1d175-197">`[TaskId <String>]`: Die ID.</span><span class="sxs-lookup"><span data-stu-id="1d175-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="1d175-198">`[TaskType <String>]`: Der Vorgangstyp.</span><span class="sxs-lookup"><span data-stu-id="1d175-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="1d175-199">Details in der Eigenschaft "CustomDetails" hängen von diesem Typ ab.</span><span class="sxs-lookup"><span data-stu-id="1d175-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="1d175-200">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d175-200">RELATED LINKS</span></span>

