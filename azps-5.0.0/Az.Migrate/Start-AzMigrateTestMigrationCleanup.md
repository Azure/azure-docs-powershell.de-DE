---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178825"
---
# <span data-ttu-id="b84bd-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="b84bd-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="b84bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b84bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b84bd-103">Bereinigt die Testmigration für den replizierenden Server.</span><span class="sxs-lookup"><span data-stu-id="b84bd-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="b84bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b84bd-104">SYNTAX</span></span>

### <span data-ttu-id="b84bd-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="b84bd-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b84bd-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="b84bd-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b84bd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b84bd-107">DESCRIPTION</span></span>
<span data-ttu-id="b84bd-108">Das Start-AzMigrateTestMigrationCleanup-Cmdlet initiiert das Bereinigen der Testmigration für den replizierenden Server.</span><span class="sxs-lookup"><span data-stu-id="b84bd-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="b84bd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b84bd-109">EXAMPLES</span></span>

### <span data-ttu-id="b84bd-110">Beispiel 1: nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="b84bd-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="b84bd-111">Nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="b84bd-111">By machine id.</span></span>

### <span data-ttu-id="b84bd-112">Beispiel 2: nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="b84bd-112">Example 2: By input object</span></span>
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

<span data-ttu-id="b84bd-113">Nach Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="b84bd-113">By input object.</span></span>

## <span data-ttu-id="b84bd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b84bd-114">PARAMETERS</span></span>

### <span data-ttu-id="b84bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b84bd-115">-DefaultProfile</span></span>
<span data-ttu-id="b84bd-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b84bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b84bd-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b84bd-117">-InputObject</span></span>
<span data-ttu-id="b84bd-118">Gibt den Replikationsserver an, für den die Test Migrations Bereinigung initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b84bd-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="b84bd-119">Das Serverobjekt kann mit dem Get-AzMigrateServerReplication-Cmdlet abgerufen werden, das Sie erstellen möchten, finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b84bd-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b84bd-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b84bd-120">-SubscriptionId</span></span>
<span data-ttu-id="b84bd-121">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b84bd-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b84bd-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="b84bd-122">-TargetObjectID</span></span>
<span data-ttu-id="b84bd-123">Gibt den Replikationsserver an, für den die Test Migrations Bereinigung initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b84bd-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="b84bd-124">Die ID sollte mit dem Get-AzMigrateServerReplication-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b84bd-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="b84bd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84bd-125">CommonParameters</span></span>
<span data-ttu-id="b84bd-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b84bd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84bd-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b84bd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84bd-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b84bd-128">INPUTS</span></span>

## <span data-ttu-id="b84bd-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b84bd-129">OUTPUTS</span></span>

### <span data-ttu-id="b84bd-130">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="b84bd-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="b84bd-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b84bd-131">NOTES</span></span>

<span data-ttu-id="b84bd-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="b84bd-132">ALIASES</span></span>

<span data-ttu-id="b84bd-133">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b84bd-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b84bd-134">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b84bd-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b84bd-135">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b84bd-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b84bd-136">Inputobject <IMigrationItem> : gibt den replizierenden Server an, für den die Test Migrations Bereinigung initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b84bd-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="b84bd-137">Das Serverobjekt kann mit dem Get-AzMigrateServerReplication-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b84bd-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="b84bd-138">`[Location <String>]`: Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="b84bd-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="b84bd-139">`[CurrentJobId <String>]`: Die Arm-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="b84bd-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="b84bd-140">`[CurrentJobName <String>]`: Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="b84bd-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="b84bd-141">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="b84bd-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="b84bd-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Benutzerdefinierte Einstellungen für den Migrations Anbieter.</span><span class="sxs-lookup"><span data-stu-id="b84bd-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="b84bd-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b84bd-143">RELATED LINKS</span></span>

