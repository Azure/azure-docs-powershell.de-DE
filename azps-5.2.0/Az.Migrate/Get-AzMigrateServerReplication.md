---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateServerReplication.md
ms.openlocfilehash: d66c21c33065fa1e142f38acbd3ef7971a7489dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356822"
---
# <span data-ttu-id="cb690-101">Get-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="cb690-101">Get-AzMigrateServerReplication</span></span>

## <span data-ttu-id="cb690-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb690-102">SYNOPSIS</span></span>
<span data-ttu-id="cb690-103">Ruft die Details des replizierbaren Servers ab.</span><span class="sxs-lookup"><span data-stu-id="cb690-103">Retrieves the details of the replicating server.</span></span>

## <span data-ttu-id="cb690-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb690-104">SYNTAX</span></span>

### <span data-ttu-id="cb690-105">ListByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cb690-105">ListByName (Default)</span></span>
```
Get-AzMigrateServerReplication -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-SkipToken <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb690-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb690-106">GetByInputObject</span></span>
```
Get-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb690-107">GetBySDSID</span><span class="sxs-lookup"><span data-stu-id="cb690-107">GetBySDSID</span></span>
```
Get-AzMigrateServerReplication -DiscoveredMachineId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb690-108">GetBySRSID</span><span class="sxs-lookup"><span data-stu-id="cb690-108">GetBySRSID</span></span>
```
Get-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cb690-109">ListById</span><span class="sxs-lookup"><span data-stu-id="cb690-109">ListById</span></span>
```
Get-AzMigrateServerReplication -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>]
 [-Filter <String>] [-SkipToken <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cb690-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb690-110">DESCRIPTION</span></span>
<span data-ttu-id="cb690-111">Das Get-AzMigrateServerReplication cmdlet ruft das Objekt für den replizierbaren Server ab.</span><span class="sxs-lookup"><span data-stu-id="cb690-111">The Get-AzMigrateServerReplication cmdlet retrieves the object for the replicating server.</span></span>

## <span data-ttu-id="cb690-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb690-112">EXAMPLES</span></span>

### <span data-ttu-id="cb690-113">Beispiel 1: Details nach ID erhalten</span><span class="sxs-lookup"><span data-stu-id="cb690-113">Example 1: Get details by id</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="cb690-114">"Nach ID erhalten".</span><span class="sxs-lookup"><span data-stu-id="cb690-114">Get by id.</span></span>

### <span data-ttu-id="cb690-115">Beispiel 2: Auflisten aller Im Projekt nach ID.</span><span class="sxs-lookup"><span data-stu-id="cb690-115">Example 2: List all in project by id.</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -ResourceGroupID /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020 -ProjectID "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Migrate/MigrateProjects/AzMigrateTestProjectPWSH"

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : 57b59212-6a2f-4333-8882-461647bb05f9
Health                      : Normal
HealthError                 : {593b735d-2a34-53b2-b8ed-e33da5650703}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : rb-w2k12r2-1
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="cb690-116">"Alle auflisten" aus.</span><span class="sxs-lookup"><span data-stu-id="cb690-116">List all.</span></span>

### <span data-ttu-id="cb690-117">Beispiel 2: Auflisten aller Projektnamen</span><span class="sxs-lookup"><span data-stu-id="cb690-117">Example 2: List all in project by name.</span></span>
```powershell
PS C:\> Get-AzMigrateServerReplication -ResourceGroupName azmigratepwshtestasr13072020 -ProjectName AzMigrateTestProjectPWSH

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : d8b110c6-3be9-4798-b2d4-9a1cd068adfb
Health                      : Normal
HealthError                 : {101883a0-23f7-538a-bbd5-6d8b4fa900e2}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : prsadhu-TestVM
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems

AllowedOperation            : {DisableMigration, TestMigrate, Migrate}
CurrentJobId                : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/None
CurrentJobName              : None
CurrentJobStartTime         : 1/1/53 1:01:01 AM
EventCorrelationId          : 57b59212-6a2f-4333-8882-461647bb05f9
Health                      : Normal
HealthError                 : {593b735d-2a34-53b2-b8ed-e33da5650703}
Id                          : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionCont
                              ainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-
                              e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
LastTestMigrationStatus     :
LastTestMigrationTime       :
Location                    :
MachineName                 : rb-w2k12r2-1
MigrationState              : Replicating
MigrationStateDescription   : Ready to migrate
Name                        : bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629
PolicyFriendlyName          : migrateAzMigratePWSHTc8d1sitepolicy
PolicyId                    : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServ
                              ices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy
ProviderSpecificDetail      : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtMigrationDetails
TestMigrateState            : None
TestMigrateStateDescription : None
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationMigrationItems
```

<span data-ttu-id="cb690-118">"Alle auflisten" aus.</span><span class="sxs-lookup"><span data-stu-id="cb690-118">List all.</span></span>

## <span data-ttu-id="cb690-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb690-119">PARAMETERS</span></span>

### <span data-ttu-id="cb690-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb690-120">-DefaultProfile</span></span>
<span data-ttu-id="cb690-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb690-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb690-122">-DiscoveredMachineId</span><span class="sxs-lookup"><span data-stu-id="cb690-122">-DiscoveredMachineId</span></span>
<span data-ttu-id="cb690-123">Gibt die Computer-ID des ermittelten Servers an.</span><span class="sxs-lookup"><span data-stu-id="cb690-123">Specifies the machine ID of the discovered server.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySDSID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb690-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="cb690-124">-Filter</span></span>
<span data-ttu-id="cb690-125">OData-Filteroptionen.</span><span class="sxs-lookup"><span data-stu-id="cb690-125">OData filter options.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb690-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb690-126">-InputObject</span></span>
<span data-ttu-id="cb690-127">Gibt das Computerobjekt des replizierbaren Servers an.</span><span class="sxs-lookup"><span data-stu-id="cb690-127">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="cb690-128">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cb690-128">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb690-129">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="cb690-129">-ProjectID</span></span>
<span data-ttu-id="cb690-130">Gibt das Azure Migrate Project an, in das Server repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="cb690-130">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb690-131">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="cb690-131">-ProjectName</span></span>
<span data-ttu-id="cb690-132">Gibt das Projekt "Azure Migrate" im aktuellen Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="cb690-132">Specifies the Azure Migrate project  in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb690-133">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="cb690-133">-ResourceGroupID</span></span>
<span data-ttu-id="cb690-134">Gibt die Ressourcengruppe des Azure-Projekts "Migrieren" im aktuellen Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="cb690-134">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb690-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb690-135">-ResourceGroupName</span></span>
<span data-ttu-id="cb690-136">Gibt die Ressourcengruppe des Azure-Projekts "Migrieren" im aktuellen Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="cb690-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb690-137">-SkipToken</span><span class="sxs-lookup"><span data-stu-id="cb690-137">-SkipToken</span></span>
<span data-ttu-id="cb690-138">Das Paginierungstoken.</span><span class="sxs-lookup"><span data-stu-id="cb690-138">The pagination token.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb690-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb690-139">-SubscriptionId</span></span>
<span data-ttu-id="cb690-140">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="cb690-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="cb690-141">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="cb690-141">-TargetObjectID</span></span>
<span data-ttu-id="cb690-142">Gibt den replizierbaren Server an.</span><span class="sxs-lookup"><span data-stu-id="cb690-142">Specifies the replicating server.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySRSID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb690-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb690-143">CommonParameters</span></span>
<span data-ttu-id="cb690-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb690-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb690-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb690-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb690-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb690-146">INPUTS</span></span>

## <span data-ttu-id="cb690-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb690-147">OUTPUTS</span></span>

### <span data-ttu-id="cb690-148">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem</span><span class="sxs-lookup"><span data-stu-id="cb690-148">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem</span></span>

## <span data-ttu-id="cb690-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cb690-149">NOTES</span></span>

<span data-ttu-id="cb690-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cb690-150">ALIASES</span></span>

<span data-ttu-id="cb690-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cb690-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb690-152">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cb690-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb690-153">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb690-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb690-154">INPUTOBJECT <IMigrationItem> : Gibt das Computerobjekt des replizierbaren Servers an.</span><span class="sxs-lookup"><span data-stu-id="cb690-154">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="cb690-155">`[Location <String>]`: Ressourcenstandort</span><span class="sxs-lookup"><span data-stu-id="cb690-155">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="cb690-156">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="cb690-156">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="cb690-157">`[CurrentJobName <String>]`: Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="cb690-157">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="cb690-158">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="cb690-158">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="cb690-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Die benutzerdefinierten Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="cb690-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="cb690-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cb690-160">RELATED LINKS</span></span>

