---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 47f87fc2f1f1d4e6186e9caaf4921990122c07fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931579"
---
# <span data-ttu-id="4966b-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="4966b-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="4966b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4966b-102">SYNOPSIS</span></span>
<span data-ttu-id="4966b-103">Startet die Migration für den Replikationsserver.</span><span class="sxs-lookup"><span data-stu-id="4966b-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="4966b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4966b-104">SYNTAX</span></span>

### <span data-ttu-id="4966b-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="4966b-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4966b-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="4966b-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4966b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4966b-107">DESCRIPTION</span></span>
<span data-ttu-id="4966b-108">Startet die Migration für den Replikationsserver.</span><span class="sxs-lookup"><span data-stu-id="4966b-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="4966b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4966b-109">EXAMPLES</span></span>

### <span data-ttu-id="4966b-110">Beispiel 1: Nach ID</span><span class="sxs-lookup"><span data-stu-id="4966b-110">Example 1: By id</span></span>
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

<span data-ttu-id="4966b-111">Nach ID</span><span class="sxs-lookup"><span data-stu-id="4966b-111">By id</span></span>

## <span data-ttu-id="4966b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4966b-112">PARAMETERS</span></span>

### <span data-ttu-id="4966b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4966b-113">-DefaultProfile</span></span>
<span data-ttu-id="4966b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4966b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4966b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4966b-115">-InputObject</span></span>
<span data-ttu-id="4966b-116">Gibt den Replikationsserver an, für den die Migration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4966b-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="4966b-117">Das Serverobjekt kann mithilfe des cmdlets Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4966b-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="4966b-118">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4966b-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4966b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4966b-119">-SubscriptionId</span></span>
<span data-ttu-id="4966b-120">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4966b-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4966b-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="4966b-121">-TargetObjectID</span></span>
<span data-ttu-id="4966b-122">Gibt den umzusendenden Server an, für den die Migration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4966b-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="4966b-123">Die ID sollte mithilfe des cmdlets Get-AzMigrateServerReplication werden.</span><span class="sxs-lookup"><span data-stu-id="4966b-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="4966b-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="4966b-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="4966b-125">Gibt an, ob der Quellserver nach der Migration deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4966b-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="4966b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4966b-126">CommonParameters</span></span>
<span data-ttu-id="4966b-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4966b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4966b-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4966b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4966b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4966b-129">INPUTS</span></span>

## <span data-ttu-id="4966b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4966b-130">OUTPUTS</span></span>

### <span data-ttu-id="4966b-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="4966b-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="4966b-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4966b-132">NOTES</span></span>

<span data-ttu-id="4966b-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4966b-133">ALIASES</span></span>

<span data-ttu-id="4966b-134">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="4966b-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4966b-135">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="4966b-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4966b-136">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4966b-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4966b-137">INPUTOBJECT <IMigrationItem> : Gibt den Replikationsserver an, für den die Migration initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4966b-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="4966b-138">Das Serverobjekt kann mithilfe des cmdlets Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4966b-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="4966b-139">`[Location <String>]`: Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="4966b-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="4966b-140">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="4966b-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="4966b-141">`[CurrentJobName <String>]`: Der Auftragsname.</span><span class="sxs-lookup"><span data-stu-id="4966b-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="4966b-142">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="4966b-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="4966b-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Benutzerdefinierte Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="4966b-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="4966b-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4966b-144">RELATED LINKS</span></span>

