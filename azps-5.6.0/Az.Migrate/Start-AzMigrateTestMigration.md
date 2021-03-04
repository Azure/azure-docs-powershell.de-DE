---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 2c0582f8e91218679b9fbaeb3192e15f2848fd1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947400"
---
# <span data-ttu-id="82792-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="82792-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="82792-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82792-102">SYNOPSIS</span></span>
<span data-ttu-id="82792-103">Startet die Testmigration für den replikationsserver.</span><span class="sxs-lookup"><span data-stu-id="82792-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="82792-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82792-104">SYNTAX</span></span>

### <span data-ttu-id="82792-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="82792-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="82792-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="82792-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="82792-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82792-107">DESCRIPTION</span></span>
<span data-ttu-id="82792-108">Das Start-AzMigrateTestMigration-Cmdlet initiiert die Testmigration für den replikationsserver.</span><span class="sxs-lookup"><span data-stu-id="82792-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="82792-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82792-109">EXAMPLES</span></span>

### <span data-ttu-id="82792-110">Beispiel 1: Nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="82792-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="82792-111">Nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="82792-111">By machine id.</span></span>

### <span data-ttu-id="82792-112">Beispiel 2: Nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="82792-112">Example 2: By input object</span></span>
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

<span data-ttu-id="82792-113">Nach Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="82792-113">By input object.</span></span>

## <span data-ttu-id="82792-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="82792-114">PARAMETERS</span></span>

### <span data-ttu-id="82792-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82792-115">-DefaultProfile</span></span>
<span data-ttu-id="82792-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82792-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82792-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82792-117">-InputObject</span></span>
<span data-ttu-id="82792-118">Gibt den Replikationsserver an, für den die Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="82792-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="82792-119">Das Serverobjekt kann mithilfe des cmdlets Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="82792-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="82792-120">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="82792-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="82792-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82792-121">-SubscriptionId</span></span>
<span data-ttu-id="82792-122">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="82792-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="82792-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="82792-123">-TargetObjectID</span></span>
<span data-ttu-id="82792-124">Gibt den Replikationsserver an, für den die Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="82792-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="82792-125">Die ID sollte mithilfe des cmdlets Get-AzMigrateServerReplication werden.</span><span class="sxs-lookup"><span data-stu-id="82792-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="82792-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="82792-126">-TestNetworkID</span></span>
<span data-ttu-id="82792-127">Aktualisiert die virtuelle Netzwerk-ID innerhalb des Azure-Zielabonnements, das für die Testmigration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="82792-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

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

### <span data-ttu-id="82792-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82792-128">CommonParameters</span></span>
<span data-ttu-id="82792-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82792-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82792-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82792-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82792-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82792-131">INPUTS</span></span>

## <span data-ttu-id="82792-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82792-132">OUTPUTS</span></span>

### <span data-ttu-id="82792-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="82792-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="82792-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="82792-134">NOTES</span></span>

<span data-ttu-id="82792-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="82792-135">ALIASES</span></span>

<span data-ttu-id="82792-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="82792-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="82792-137">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="82792-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="82792-138">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="82792-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="82792-139">INPUTOBJECT <IMigrationItem> : Gibt den Replikationsserver an, für den die Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="82792-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="82792-140">Das Serverobjekt kann mithilfe des cmdlets Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="82792-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="82792-141">`[Location <String>]`: Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="82792-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="82792-142">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="82792-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="82792-143">`[CurrentJobName <String>]`: Der Auftragsname.</span><span class="sxs-lookup"><span data-stu-id="82792-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="82792-144">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="82792-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="82792-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Benutzerdefinierte Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="82792-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="82792-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="82792-146">RELATED LINKS</span></span>

