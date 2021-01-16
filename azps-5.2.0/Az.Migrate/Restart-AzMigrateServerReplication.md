---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363585"
---
# <span data-ttu-id="e47ef-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="e47ef-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="e47ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e47ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e47ef-103">Startet die Replikation für den angegebenen Server neu.</span><span class="sxs-lookup"><span data-stu-id="e47ef-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="e47ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e47ef-104">SYNTAX</span></span>

### <span data-ttu-id="e47ef-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="e47ef-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e47ef-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="e47ef-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e47ef-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e47ef-107">DESCRIPTION</span></span>
<span data-ttu-id="e47ef-108">Das Restart-AzMigrateServerReplication cmdlet repariert die Replikation für den angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="e47ef-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="e47ef-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e47ef-109">EXAMPLES</span></span>

### <span data-ttu-id="e47ef-110">Beispiel 1: Nach ID.</span><span class="sxs-lookup"><span data-stu-id="e47ef-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="e47ef-111">Nach ID.</span><span class="sxs-lookup"><span data-stu-id="e47ef-111">By id.</span></span>

### <span data-ttu-id="e47ef-112">Beispiel 2: Nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="e47ef-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="e47ef-113">Nach Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="e47ef-113">By Input Object.</span></span>

## <span data-ttu-id="e47ef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e47ef-114">PARAMETERS</span></span>

### <span data-ttu-id="e47ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47ef-115">-DefaultProfile</span></span>
<span data-ttu-id="e47ef-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e47ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e47ef-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e47ef-117">-InputObject</span></span>
<span data-ttu-id="e47ef-118">Gibt das Computerobjekt des replizierbaren Servers an.</span><span class="sxs-lookup"><span data-stu-id="e47ef-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="e47ef-119">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e47ef-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47ef-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e47ef-120">-SubscriptionId</span></span>
<span data-ttu-id="e47ef-121">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e47ef-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e47ef-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="e47ef-122">-TargetObjectID</span></span>
<span data-ttu-id="e47ef-123">Gibt den Wiederholungsserver an, für den die erneute Synchronisierung initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e47ef-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="e47ef-124">Die ID sollte mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e47ef-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47ef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47ef-125">CommonParameters</span></span>
<span data-ttu-id="e47ef-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e47ef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47ef-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e47ef-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47ef-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e47ef-128">INPUTS</span></span>

## <span data-ttu-id="e47ef-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e47ef-129">OUTPUTS</span></span>

### <span data-ttu-id="e47ef-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="e47ef-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="e47ef-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e47ef-131">NOTES</span></span>

<span data-ttu-id="e47ef-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e47ef-132">ALIASES</span></span>

<span data-ttu-id="e47ef-133">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e47ef-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e47ef-134">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e47ef-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e47ef-135">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e47ef-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e47ef-136">INPUTOBJECT <IMigrationItem> : Gibt das Computerobjekt des replizierbaren Servers an.</span><span class="sxs-lookup"><span data-stu-id="e47ef-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="e47ef-137">`[Location <String>]`: Ressourcenstandort</span><span class="sxs-lookup"><span data-stu-id="e47ef-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="e47ef-138">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="e47ef-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="e47ef-139">`[CurrentJobName <String>]`: Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="e47ef-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="e47ef-140">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="e47ef-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="e47ef-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Die benutzerdefinierten Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="e47ef-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="e47ef-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e47ef-142">RELATED LINKS</span></span>

