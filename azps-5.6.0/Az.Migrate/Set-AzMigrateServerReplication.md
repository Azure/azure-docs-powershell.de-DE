---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: b87e541266c3ce555c0fc11910c9541914b14738
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947408"
---
# <span data-ttu-id="c9ab9-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="c9ab9-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="c9ab9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9ab9-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ab9-103">Aktualisiert die Zieleigenschaften für den replikationsserver.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c9ab9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9ab9-104">SYNTAX</span></span>

### <span data-ttu-id="c9ab9-105">ByIDVMwareCbt (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9ab9-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9ab9-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="c9ab9-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9ab9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9ab9-107">DESCRIPTION</span></span>
<span data-ttu-id="c9ab9-108">Das Set-AzMigrateServerReplication cmdlet aktualisiert die Zieleigenschaften für den replikationsserver.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c9ab9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c9ab9-109">EXAMPLES</span></span>

### <span data-ttu-id="c9ab9-110">Beispiel 1: Aktualisieren nach ID</span><span class="sxs-lookup"><span data-stu-id="c9ab9-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="c9ab9-111">Nach ID.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-111">By id.</span></span>

## <span data-ttu-id="c9ab9-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c9ab9-112">PARAMETERS</span></span>

### <span data-ttu-id="c9ab9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ab9-113">-DefaultProfile</span></span>
<span data-ttu-id="c9ab9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9ab9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9ab9-115">-InputObject</span></span>
<span data-ttu-id="c9ab9-116">Gibt den Replikationsserver an, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c9ab9-117">Das Serverobjekt kann mithilfe des cmdlets Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="c9ab9-118">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9ab9-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="c9ab9-119">-NicToUpdate</span></span>
<span data-ttu-id="c9ab9-120">Aktualisiert die NIC für die zu erstellende Azure-VM.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="c9ab9-121">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu den NICTOUPDATE-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9ab9-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9ab9-122">-SubscriptionId</span></span>
<span data-ttu-id="c9ab9-123">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-123">The subscription Id.</span></span>

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

### <span data-ttu-id="c9ab9-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c9ab9-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="c9ab9-125">Gibt den Verfügbarkeitssatz an, der für die Erstellung von VMs verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="c9ab9-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="c9ab9-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="c9ab9-127">Gibt die Verfügbarkeitszone an, die für die Erstellung von virtuellen Ressourcen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="c9ab9-128">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9ab9-128">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="c9ab9-129">Gibt das Speicherkonto an, das für die Startdiagnose verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-129">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="c9ab9-130">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="c9ab9-130">-TargetNetworkId</span></span>
<span data-ttu-id="c9ab9-131">Aktualisiert die Virtuelle Netzwerk-ID innerhalb des Azure-Zielabonnements, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-131">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c9ab9-132">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="c9ab9-132">-TargetObjectID</span></span>
<span data-ttu-id="c9ab9-133">Gibt den Replcatingserver an, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-133">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c9ab9-134">Die ID sollte mithilfe des cmdlets Get-AzMigrateServerReplication werden.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-134">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c9ab9-135">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="c9ab9-135">-TargetResourceGroupID</span></span>
<span data-ttu-id="c9ab9-136">Aktualisiert die Ressourcengruppen-ID innerhalb des Azure-Zielabonnements, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-136">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c9ab9-137">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="c9ab9-137">-TargetVMName</span></span>
<span data-ttu-id="c9ab9-138">Gibt den Replcatingserver an, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-138">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c9ab9-139">Die ID sollte mithilfe des cmdlets Get-AzMigrateServerReplication werden.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-139">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c9ab9-140">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="c9ab9-140">-TargetVMSize</span></span>
<span data-ttu-id="c9ab9-141">Aktualisiert die SKU der zu erstellende Azure-VM.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-141">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="c9ab9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ab9-142">CommonParameters</span></span>
<span data-ttu-id="c9ab9-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ab9-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9ab9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ab9-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c9ab9-145">INPUTS</span></span>

## <span data-ttu-id="c9ab9-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c9ab9-146">OUTPUTS</span></span>

### <span data-ttu-id="c9ab9-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="c9ab9-147">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="c9ab9-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c9ab9-148">NOTES</span></span>

<span data-ttu-id="c9ab9-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c9ab9-149">ALIASES</span></span>

<span data-ttu-id="c9ab9-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c9ab9-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9ab9-151">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9ab9-152">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9ab9-153">INPUTOBJECT <IMigrationItem> : Gibt den Replikationsserver an, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-153">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="c9ab9-154">Das Serverobjekt kann mithilfe des cmdlets Get-AzMigrateServerReplication abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-154">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="c9ab9-155">`[Location <String>]`: Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="c9ab9-155">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="c9ab9-156">`[CurrentJobId <String>]`: Die ARM-ID des ausgeführten Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-156">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="c9ab9-157">`[CurrentJobName <String>]`: Der Auftragsname.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-157">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="c9ab9-158">`[CurrentJobStartTime <DateTime?>]`: Die Startzeit des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-158">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="c9ab9-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Benutzerdefinierte Einstellungen des Migrationsanbieters.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-159">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="c9ab9-160">NICTOUPDATE <IVMwareCbtNicInput[]>: Aktualisiert die NIC für die zu erstellende Azure-VM.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-160">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="c9ab9-161">`IsPrimaryNic <String>`: Ein Wert, der angibt, ob es sich um die primäre NIC handelt.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-161">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="c9ab9-162">`NicId <String>`: Die NIC-ID.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-162">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="c9ab9-163">`[IsSelectedForMigration <String>]`: Ein Wert, der angibt, ob diese NIC für die Migration ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-163">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="c9ab9-164">`[TargetStaticIPAddress <String>]`: Die statische IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-164">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="c9ab9-165">`[TargetSubnetName <String>]`: Name des Zielsubnetzs.</span><span class="sxs-lookup"><span data-stu-id="c9ab9-165">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="c9ab9-166">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c9ab9-166">RELATED LINKS</span></span>

