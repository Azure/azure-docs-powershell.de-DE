---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152268"
---
# <span data-ttu-id="a3757-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="a3757-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="a3757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3757-102">SYNOPSIS</span></span>
<span data-ttu-id="a3757-103">Startet die Testmigration für den Replikatserver.</span><span class="sxs-lookup"><span data-stu-id="a3757-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="a3757-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3757-104">SYNTAX</span></span>

### <span data-ttu-id="a3757-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3757-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3757-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="a3757-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a3757-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3757-107">DESCRIPTION</span></span>
<span data-ttu-id="a3757-108">Das Start-AzMigrateTestMigration cmdlet initiiert die Testmigration für den replizierbaren Server.</span><span class="sxs-lookup"><span data-stu-id="a3757-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="a3757-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3757-109">EXAMPLES</span></span>

### <span data-ttu-id="a3757-110">Beispiel 1: Nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="a3757-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="a3757-111">Nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="a3757-111">By machine id.</span></span>

### <span data-ttu-id="a3757-112">Beispiel 2: Nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="a3757-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="a3757-113">Nach Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="a3757-113">By input object.</span></span>

## <span data-ttu-id="a3757-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3757-114">PARAMETERS</span></span>

### <span data-ttu-id="a3757-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3757-115">-DefaultProfile</span></span>
<span data-ttu-id="a3757-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3757-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3757-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3757-117">-InputObject</span></span>
<span data-ttu-id="a3757-118">Gibt den Replikatserver an, für den die Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a3757-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="a3757-119">Das Serverobjekt kann mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a3757-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="a3757-120">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a3757-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3757-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3757-121">-SubscriptionId</span></span>
<span data-ttu-id="a3757-122">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a3757-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a3757-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="a3757-123">-TargetObjectID</span></span>
<span data-ttu-id="a3757-124">Gibt den Replikatserver an, für den die Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a3757-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="a3757-125">Die ID sollte mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a3757-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="a3757-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="a3757-126">-TestNetworkID</span></span>
<span data-ttu-id="a3757-127">Aktualisiert die virtuelle Netzwerk-ID innerhalb des Azure-Zielabonnements, das für die Testmigration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3757-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3757-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3757-128">CommonParameters</span></span>
<span data-ttu-id="a3757-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3757-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3757-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3757-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3757-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3757-131">INPUTS</span></span>

## <span data-ttu-id="a3757-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3757-132">OUTPUTS</span></span>

### <span data-ttu-id="a3757-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="a3757-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="a3757-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3757-134">NOTES</span></span>

<span data-ttu-id="a3757-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a3757-135">ALIASES</span></span>

<span data-ttu-id="a3757-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a3757-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3757-137">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a3757-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3757-138">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3757-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3757-139">INPUTOBJECT : Gibt den Replikatserver an, für den <IMigrationItem> die Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a3757-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="a3757-140">Das Serverobjekt kann mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a3757-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="a3757-141">`[Location <String>]`: Ressourcenstandort</span><span class="sxs-lookup"><span data-stu-id="a3757-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="a3757-142">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="a3757-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="a3757-143">`[CurrentJobName <String>]`: Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="a3757-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="a3757-144">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="a3757-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="a3757-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Die benutzerdefinierten Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="a3757-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="a3757-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3757-146">RELATED LINKS</span></span>

