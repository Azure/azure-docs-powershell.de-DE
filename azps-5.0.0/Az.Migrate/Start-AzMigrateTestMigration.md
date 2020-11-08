---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178826"
---
# <span data-ttu-id="bc709-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="bc709-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="bc709-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc709-102">SYNOPSIS</span></span>
<span data-ttu-id="bc709-103">Startet die Testmigration für den replizierenden Server.</span><span class="sxs-lookup"><span data-stu-id="bc709-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="bc709-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc709-104">SYNTAX</span></span>

### <span data-ttu-id="bc709-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc709-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc709-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="bc709-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bc709-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc709-107">DESCRIPTION</span></span>
<span data-ttu-id="bc709-108">Das Start-AzMigrateTestMigration-Cmdlet initiiert die Testmigration für den replizierenden Server.</span><span class="sxs-lookup"><span data-stu-id="bc709-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="bc709-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc709-109">EXAMPLES</span></span>

### <span data-ttu-id="bc709-110">Beispiel 1: nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="bc709-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="bc709-111">Nach Computer-ID.</span><span class="sxs-lookup"><span data-stu-id="bc709-111">By machine id.</span></span>

### <span data-ttu-id="bc709-112">Beispiel 2: nach Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="bc709-112">Example 2: By input object</span></span>
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

<span data-ttu-id="bc709-113">Nach Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="bc709-113">By input object.</span></span>

## <span data-ttu-id="bc709-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc709-114">PARAMETERS</span></span>

### <span data-ttu-id="bc709-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc709-115">-DefaultProfile</span></span>
<span data-ttu-id="bc709-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc709-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc709-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc709-117">-InputObject</span></span>
<span data-ttu-id="bc709-118">Gibt den Replikationsserver an, für den die Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="bc709-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="bc709-119">Das Serverobjekt kann mit dem Get-AzMigrateServerReplication-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bc709-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="bc709-120">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="bc709-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc709-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="bc709-121">-SubscriptionId</span></span>
<span data-ttu-id="bc709-122">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="bc709-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="bc709-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="bc709-123">-TargetObjectID</span></span>
<span data-ttu-id="bc709-124">Gibt den Replikationsserver an, für den die Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="bc709-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="bc709-125">Die ID sollte mit dem Get-AzMigrateServerReplication-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bc709-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="bc709-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="bc709-126">-TestNetworkID</span></span>
<span data-ttu-id="bc709-127">Aktualisiert die virtuelle Netzwerk-ID innerhalb des Ziels Azure-Abonnements, die für die Testmigration verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc709-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

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

### <span data-ttu-id="bc709-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc709-128">CommonParameters</span></span>
<span data-ttu-id="bc709-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc709-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc709-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc709-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc709-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc709-131">INPUTS</span></span>

## <span data-ttu-id="bc709-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc709-132">OUTPUTS</span></span>

### <span data-ttu-id="bc709-133">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="bc709-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="bc709-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc709-134">NOTES</span></span>

<span data-ttu-id="bc709-135">Aliase</span><span class="sxs-lookup"><span data-stu-id="bc709-135">ALIASES</span></span>

<span data-ttu-id="bc709-136">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc709-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc709-137">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bc709-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc709-138">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="bc709-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc709-139">Inputobject <IMigrationItem> : gibt den Replikationsserver an, für den die Testmigration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="bc709-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="bc709-140">Das Serverobjekt kann mit dem Get-AzMigrateServerReplication-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bc709-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="bc709-141">`[Location <String>]`: Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="bc709-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="bc709-142">`[CurrentJobId <String>]`: Die Arm-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="bc709-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="bc709-143">`[CurrentJobName <String>]`: Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="bc709-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="bc709-144">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="bc709-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="bc709-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Benutzerdefinierte Einstellungen für den Migrations Anbieter.</span><span class="sxs-lookup"><span data-stu-id="bc709-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="bc709-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc709-146">RELATED LINKS</span></span>

