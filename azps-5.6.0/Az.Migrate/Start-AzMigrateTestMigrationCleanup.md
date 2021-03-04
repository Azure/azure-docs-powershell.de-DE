---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: 534728e98d913a3de7f7b02628451433b252ded9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947387"
---
# <span data-ttu-id="90808-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="90808-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="90808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90808-102">SYNOPSIS</span></span>
<span data-ttu-id="90808-103">Bereinigt die Testmigration für den replikationsserver.</span><span class="sxs-lookup"><span data-stu-id="90808-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="90808-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90808-104">SYNTAX</span></span>

### <span data-ttu-id="90808-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="90808-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="90808-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="90808-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="90808-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90808-107">DESCRIPTION</span></span>
<span data-ttu-id="90808-108">Das Start-AzMigrateTestMigrationCleanup-Cmdlet initiiert die Bereinigung der Testmigration für den replikationsserver.</span><span class="sxs-lookup"><span data-stu-id="90808-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="90808-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90808-109">EXAMPLES</span></span>

### <span data-ttu-id="90808-110">Beispiel 1: Nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="90808-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigrationCleanup -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="90808-111">Nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="90808-111">By machine id.</span></span>

### <span data-ttu-id="90808-112">Beispiel 2: Nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="90808-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigrationCleanup -InputObject $ob


AllowedOperation            : {DisableMigration, TestMigrate, Migrate}

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="90808-113">Nach Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="90808-113">By input object.</span></span>

## <span data-ttu-id="90808-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="90808-114">PARAMETERS</span></span>

### <span data-ttu-id="90808-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90808-115">-DefaultProfile</span></span>
<span data-ttu-id="90808-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90808-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90808-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90808-117">-InputObject</span></span>
<span data-ttu-id="90808-118">Gibt den Replikationsserver an, für den die Bereinigung der Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="90808-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="90808-119">Das Serverobjekt kann mithilfe des Get-AzMigrateServerReplication Cmdlets To abgerufen werden. Informationen finden Sie im Abschnitt NOTIZEN zu inputOBJECT-Eigenschaften und erstellen sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="90808-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="90808-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90808-120">-SubscriptionId</span></span>
<span data-ttu-id="90808-121">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="90808-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="90808-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="90808-122">-TargetObjectID</span></span>
<span data-ttu-id="90808-123">Gibt den Replikationsserver an, für den die Bereinigung der Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="90808-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="90808-124">Die ID sollte mithilfe des cmdlets Get-AzMigrateServerReplication werden.</span><span class="sxs-lookup"><span data-stu-id="90808-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="90808-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90808-125">CommonParameters</span></span>
<span data-ttu-id="90808-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90808-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90808-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90808-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90808-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90808-128">INPUTS</span></span>

## <span data-ttu-id="90808-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90808-129">OUTPUTS</span></span>

### <span data-ttu-id="90808-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="90808-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="90808-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="90808-131">NOTES</span></span>

<span data-ttu-id="90808-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="90808-132">ALIASES</span></span>

<span data-ttu-id="90808-133">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="90808-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90808-134">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="90808-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90808-135">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90808-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90808-136">INPUTOBJECT <IMigrationItem> : Gibt den Replikationsserver an, für den die Bereinigung der Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="90808-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="90808-137">Das Serverobjekt kann mithilfe des cmdlets Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="90808-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="90808-138">`[Location <String>]`: Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="90808-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="90808-139">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="90808-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="90808-140">`[CurrentJobName <String>]`: Der Auftragsname.</span><span class="sxs-lookup"><span data-stu-id="90808-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="90808-141">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="90808-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="90808-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Benutzerdefinierte Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="90808-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="90808-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="90808-143">RELATED LINKS</span></span>

