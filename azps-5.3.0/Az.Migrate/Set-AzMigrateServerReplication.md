---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459035"
---
# <span data-ttu-id="c8259-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="c8259-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="c8259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8259-102">SYNOPSIS</span></span>
<span data-ttu-id="c8259-103">Aktualisiert die Zieleigenschaften für den Replikatierserver.</span><span class="sxs-lookup"><span data-stu-id="c8259-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c8259-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8259-104">SYNTAX</span></span>

### <span data-ttu-id="c8259-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8259-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8259-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="c8259-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c8259-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8259-107">DESCRIPTION</span></span>
<span data-ttu-id="c8259-108">Das Set-AzMigrateServerReplication cmdlet aktualisiert die Zieleigenschaften für den replizierbaren Server.</span><span class="sxs-lookup"><span data-stu-id="c8259-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c8259-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8259-109">EXAMPLES</span></span>

### <span data-ttu-id="c8259-110">Beispiel 1: Aktualisieren nach ID</span><span class="sxs-lookup"><span data-stu-id="c8259-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c8259-111">Nach ID.</span><span class="sxs-lookup"><span data-stu-id="c8259-111">By id.</span></span>

## <span data-ttu-id="c8259-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8259-112">PARAMETERS</span></span>

### <span data-ttu-id="c8259-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8259-113">-DefaultProfile</span></span>
<span data-ttu-id="c8259-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8259-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8259-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8259-115">-InputObject</span></span>
<span data-ttu-id="c8259-116">Gibt den replizierbaren Server an, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c8259-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c8259-117">Das Serverobjekt kann mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8259-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="c8259-118">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c8259-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8259-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="c8259-119">-NicToUpdate</span></span>
<span data-ttu-id="c8259-120">Aktualisiert die NIC für die zu erstellende Azure VM.</span><span class="sxs-lookup"><span data-stu-id="c8259-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="c8259-121">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c8259-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8259-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8259-122">-SubscriptionId</span></span>
<span data-ttu-id="c8259-123">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c8259-123">The subscription Id.</span></span>

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

### <span data-ttu-id="c8259-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c8259-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="c8259-125">Gibt den Verfügbarkeitssatz an, der für die Erstellung von VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8259-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="c8259-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="c8259-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="c8259-127">Gibt die Verfügbarkeitszone an, die für die Erstellung von VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8259-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="c8259-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="c8259-128">-TargetNetworkId</span></span>
<span data-ttu-id="c8259-129">Aktualisiert die virtuelle Netzwerk-ID innerhalb des Azure-Zielabonnements, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8259-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c8259-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="c8259-130">-TargetObjectID</span></span>
<span data-ttu-id="c8259-131">Gibt den Zusätzlichen Server an, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c8259-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c8259-132">Die ID sollte mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8259-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c8259-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="c8259-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="c8259-134">Aktualisiert die Ressourcengruppen-ID innerhalb des Azure-Zielabonnements, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8259-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c8259-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="c8259-135">-TargetVMName</span></span>
<span data-ttu-id="c8259-136">Gibt den Zusätzlichen Server an, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c8259-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c8259-137">Die ID sollte mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8259-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c8259-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="c8259-138">-TargetVMSize</span></span>
<span data-ttu-id="c8259-139">Aktualisiert die SKU der azure VM, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8259-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="c8259-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8259-140">CommonParameters</span></span>
<span data-ttu-id="c8259-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8259-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8259-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8259-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8259-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8259-143">INPUTS</span></span>

## <span data-ttu-id="c8259-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8259-144">OUTPUTS</span></span>

### <span data-ttu-id="c8259-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="c8259-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="c8259-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c8259-146">NOTES</span></span>

<span data-ttu-id="c8259-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c8259-147">ALIASES</span></span>

<span data-ttu-id="c8259-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c8259-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8259-149">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c8259-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8259-150">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8259-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8259-151">INPUTOBJECT <IMigrationItem> : Gibt den Replikatserver an, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c8259-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="c8259-152">Das Serverobjekt kann mit dem cmdlet Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8259-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="c8259-153">`[Location <String>]`: Ressourcenstandort</span><span class="sxs-lookup"><span data-stu-id="c8259-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="c8259-154">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c8259-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="c8259-155">`[CurrentJobName <String>]`: Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c8259-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="c8259-156">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c8259-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="c8259-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Die benutzerdefinierten Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="c8259-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="c8259-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Aktualisiert die NIC für die zu erstellende Azure VM.</span><span class="sxs-lookup"><span data-stu-id="c8259-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="c8259-159">`IsPrimaryNic <String>`: Ein Wert, der angibt, ob dies die primäre NIC ist.</span><span class="sxs-lookup"><span data-stu-id="c8259-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="c8259-160">`NicId <String>`: The NIC Id.</span><span class="sxs-lookup"><span data-stu-id="c8259-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="c8259-161">`[IsSelectedForMigration <String>]`: Ein Wert, der angibt, ob diese NIC für die Migration ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="c8259-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="c8259-162">`[TargetStaticIPAddress <String>]`: Die statische IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c8259-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="c8259-163">`[TargetSubnetName <String>]`: Zielname des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="c8259-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="c8259-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c8259-164">RELATED LINKS</span></span>

