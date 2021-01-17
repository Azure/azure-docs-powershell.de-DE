---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459032"
---
# <span data-ttu-id="c835c-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="c835c-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="c835c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c835c-102">SYNOPSIS</span></span>
<span data-ttu-id="c835c-103">Beendet die Replikation für den migrierten Server.</span><span class="sxs-lookup"><span data-stu-id="c835c-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="c835c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c835c-104">SYNTAX</span></span>

### <span data-ttu-id="c835c-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="c835c-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c835c-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="c835c-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c835c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c835c-107">DESCRIPTION</span></span>
<span data-ttu-id="c835c-108">Das Remove-AzMigrateServerReplication beendet die Replikation für einen migrierten Server.</span><span class="sxs-lookup"><span data-stu-id="c835c-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="c835c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c835c-109">EXAMPLES</span></span>

### <span data-ttu-id="c835c-110">Beispiel 1: Entfernen nach ID.</span><span class="sxs-lookup"><span data-stu-id="c835c-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="c835c-111">Erneute Synchronisierung nach ID.</span><span class="sxs-lookup"><span data-stu-id="c835c-111">Resync by id.</span></span>

### <span data-ttu-id="c835c-112">Beispiel 2: Entfernen durch Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="c835c-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c835c-113">Nach Name.</span><span class="sxs-lookup"><span data-stu-id="c835c-113">By name.</span></span>

## <span data-ttu-id="c835c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c835c-114">PARAMETERS</span></span>

### <span data-ttu-id="c835c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c835c-115">-DefaultProfile</span></span>
<span data-ttu-id="c835c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c835c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c835c-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="c835c-117">-ForceRemove</span></span>
<span data-ttu-id="c835c-118">Gibt an, ob die Replikationskraft für das Entfernen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c835c-118">Specifies whether the replication needs to be force removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c835c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c835c-119">-InputObject</span></span>
<span data-ttu-id="c835c-120">Gibt das Computerobjekt des replizierbaren Servers an.</span><span class="sxs-lookup"><span data-stu-id="c835c-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="c835c-121">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c835c-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c835c-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c835c-122">-SubscriptionId</span></span>
<span data-ttu-id="c835c-123">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c835c-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c835c-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="c835c-124">-TargetObjectID</span></span>
<span data-ttu-id="c835c-125">Gibt den Wiederholungsserver an, für den die Replikation deaktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c835c-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="c835c-126">Die ID sollte mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c835c-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c835c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c835c-127">CommonParameters</span></span>
<span data-ttu-id="c835c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c835c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c835c-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c835c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c835c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c835c-130">INPUTS</span></span>

## <span data-ttu-id="c835c-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c835c-131">OUTPUTS</span></span>

### <span data-ttu-id="c835c-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="c835c-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="c835c-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c835c-133">NOTES</span></span>

<span data-ttu-id="c835c-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c835c-134">ALIASES</span></span>

<span data-ttu-id="c835c-135">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c835c-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c835c-136">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c835c-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c835c-137">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c835c-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c835c-138">INPUTOBJECT <IMigrationItem> : Gibt das Computerobjekt des replizierbaren Servers an.</span><span class="sxs-lookup"><span data-stu-id="c835c-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="c835c-139">`[Location <String>]`: Ressourcenstandort</span><span class="sxs-lookup"><span data-stu-id="c835c-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="c835c-140">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c835c-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="c835c-141">`[CurrentJobName <String>]`: Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c835c-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="c835c-142">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c835c-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="c835c-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Die benutzerdefinierten Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="c835c-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="c835c-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c835c-144">RELATED LINKS</span></span>

