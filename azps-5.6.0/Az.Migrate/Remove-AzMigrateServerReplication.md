---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: 65f9527005b849b9ffbcc8c343b57515b2d437c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946048"
---
# <span data-ttu-id="1fd58-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="1fd58-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="1fd58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fd58-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd58-103">Beendet die Replikation für den migrierten Server.</span><span class="sxs-lookup"><span data-stu-id="1fd58-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="1fd58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fd58-104">SYNTAX</span></span>

### <span data-ttu-id="1fd58-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fd58-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1fd58-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="1fd58-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1fd58-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fd58-107">DESCRIPTION</span></span>
<span data-ttu-id="1fd58-108">Das Remove-AzMigrateServerReplication-Cmdlet beendet die Replikation für einen migrierten Server.</span><span class="sxs-lookup"><span data-stu-id="1fd58-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="1fd58-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1fd58-109">EXAMPLES</span></span>

### <span data-ttu-id="1fd58-110">Beispiel 1: Entfernen nach ID.</span><span class="sxs-lookup"><span data-stu-id="1fd58-110">Example 1: Remove by id.</span></span>
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

<span data-ttu-id="1fd58-111">Erneutes Synchronisieren nach ID.</span><span class="sxs-lookup"><span data-stu-id="1fd58-111">Resync by id.</span></span>

### <span data-ttu-id="1fd58-112">Beispiel 2: Entfernen nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1fd58-112">Example 2: Remove by Input Object</span></span>
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

<span data-ttu-id="1fd58-113">Nach Name.</span><span class="sxs-lookup"><span data-stu-id="1fd58-113">By name.</span></span>

## <span data-ttu-id="1fd58-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1fd58-114">PARAMETERS</span></span>

### <span data-ttu-id="1fd58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd58-115">-DefaultProfile</span></span>
<span data-ttu-id="1fd58-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fd58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fd58-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="1fd58-117">-ForceRemove</span></span>
<span data-ttu-id="1fd58-118">Gibt an, ob die Replikation entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="1fd58-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="1fd58-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fd58-119">-InputObject</span></span>
<span data-ttu-id="1fd58-120">Gibt das Computerobjekt des replikationsservers an.</span><span class="sxs-lookup"><span data-stu-id="1fd58-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="1fd58-121">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1fd58-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1fd58-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fd58-122">-SubscriptionId</span></span>
<span data-ttu-id="1fd58-123">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1fd58-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1fd58-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="1fd58-124">-TargetObjectID</span></span>
<span data-ttu-id="1fd58-125">Gibt den Replcatingserver an, für den die Replicatio deaktiviert werden muss.</span><span class="sxs-lookup"><span data-stu-id="1fd58-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="1fd58-126">Die ID sollte mithilfe des cmdlets Get-AzMigrateServerReplication werden.</span><span class="sxs-lookup"><span data-stu-id="1fd58-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="1fd58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd58-127">CommonParameters</span></span>
<span data-ttu-id="1fd58-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fd58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd58-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fd58-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd58-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1fd58-130">INPUTS</span></span>

## <span data-ttu-id="1fd58-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1fd58-131">OUTPUTS</span></span>

### <span data-ttu-id="1fd58-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="1fd58-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="1fd58-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1fd58-133">NOTES</span></span>

<span data-ttu-id="1fd58-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1fd58-134">ALIASES</span></span>

<span data-ttu-id="1fd58-135">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="1fd58-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1fd58-136">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="1fd58-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1fd58-137">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1fd58-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1fd58-138">INPUTOBJECT <IMigrationItem> : Gibt das Computerobjekt des replikationsservers an.</span><span class="sxs-lookup"><span data-stu-id="1fd58-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="1fd58-139">`[Location <String>]`: Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="1fd58-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="1fd58-140">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="1fd58-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="1fd58-141">`[CurrentJobName <String>]`: Der Auftragsname.</span><span class="sxs-lookup"><span data-stu-id="1fd58-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="1fd58-142">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="1fd58-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="1fd58-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Benutzerdefinierte Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="1fd58-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="1fd58-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1fd58-144">RELATED LINKS</span></span>

