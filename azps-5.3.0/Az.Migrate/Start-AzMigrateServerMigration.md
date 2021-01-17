---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459028"
---
# <span data-ttu-id="ef125-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="ef125-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="ef125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef125-102">SYNOPSIS</span></span>
<span data-ttu-id="ef125-103">Startet die Migration für den replizierbaren Server.</span><span class="sxs-lookup"><span data-stu-id="ef125-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="ef125-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef125-104">SYNTAX</span></span>

### <span data-ttu-id="ef125-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef125-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ef125-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="ef125-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ef125-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef125-107">DESCRIPTION</span></span>
<span data-ttu-id="ef125-108">Startet die Migration für den replizierbaren Server.</span><span class="sxs-lookup"><span data-stu-id="ef125-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="ef125-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef125-109">EXAMPLES</span></span>

### <span data-ttu-id="ef125-110">Beispiel 1: Nach ID</span><span class="sxs-lookup"><span data-stu-id="ef125-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="ef125-111">Nach ID</span><span class="sxs-lookup"><span data-stu-id="ef125-111">By id</span></span>

## <span data-ttu-id="ef125-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef125-112">PARAMETERS</span></span>

### <span data-ttu-id="ef125-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef125-113">-DefaultProfile</span></span>
<span data-ttu-id="ef125-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef125-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef125-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef125-115">-InputObject</span></span>
<span data-ttu-id="ef125-116">Gibt den Replikatserver an, für den die Migration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ef125-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="ef125-117">Das Serverobjekt kann mithilfe des cmdlets Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ef125-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="ef125-118">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ef125-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ef125-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef125-119">-SubscriptionId</span></span>
<span data-ttu-id="ef125-120">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ef125-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ef125-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="ef125-121">-TargetObjectID</span></span>
<span data-ttu-id="ef125-122">Gibt den Wiederersprechungsserver an, für den die Migration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ef125-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="ef125-123">Die ID sollte mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ef125-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="ef125-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="ef125-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="ef125-125">Gibt an, ob der Quellserver nach der Migration deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef125-125">Specifies whether the source server should be turned off post migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef125-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef125-126">CommonParameters</span></span>
<span data-ttu-id="ef125-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef125-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef125-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef125-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef125-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef125-129">INPUTS</span></span>

## <span data-ttu-id="ef125-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef125-130">OUTPUTS</span></span>

### <span data-ttu-id="ef125-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="ef125-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="ef125-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef125-132">NOTES</span></span>

<span data-ttu-id="ef125-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ef125-133">ALIASES</span></span>

<span data-ttu-id="ef125-134">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ef125-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef125-135">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ef125-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef125-136">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ef125-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef125-137">INPUTOBJECT <IMigrationItem> : Gibt den Replikatserver an, für den die Migration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ef125-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="ef125-138">Das Serverobjekt kann mithilfe des cmdlets Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ef125-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="ef125-139">`[Location <String>]`: Ressourcenstandort</span><span class="sxs-lookup"><span data-stu-id="ef125-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="ef125-140">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="ef125-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="ef125-141">`[CurrentJobName <String>]`: Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="ef125-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="ef125-142">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="ef125-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="ef125-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Die benutzerdefinierten Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="ef125-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="ef125-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef125-144">RELATED LINKS</span></span>

