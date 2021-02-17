---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152316"
---
# <span data-ttu-id="d9e6b-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="d9e6b-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="d9e6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e6b-103">Startet die Replikation für den angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="d9e6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9e6b-104">SYNTAX</span></span>

### <span data-ttu-id="d9e6b-105">ByIdDefaultUser (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9e6b-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9e6b-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="d9e6b-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9e6b-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="d9e6b-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9e6b-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="d9e6b-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d9e6b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9e6b-109">DESCRIPTION</span></span>
<span data-ttu-id="d9e6b-110">Das New-AzMigrateServerReplication cmdlet startet die Replikation für einen bestimmten ermittelten Server im Azure Migrate-Projekt.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="d9e6b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9e6b-111">EXAMPLES</span></span>

### <span data-ttu-id="d9e6b-112">Beispiel 1: Wenn nur ein Betriebssystemdatenträger vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="d9e6b-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="d9e6b-113">Dies gilt für das Szenario, in dem nur ein einziger Datenträger geschützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="d9e6b-114">Beispiel 2: Bei mehreren Datenträgern</span><span class="sxs-lookup"><span data-stu-id="d9e6b-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="d9e6b-115">Dies gilt für das Szenario, in dem mehrere Datenträger geschützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="d9e6b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9e6b-116">PARAMETERS</span></span>

### <span data-ttu-id="d9e6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e6b-117">-DefaultProfile</span></span>
<span data-ttu-id="d9e6b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9e6b-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="d9e6b-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="d9e6b-120">Gibt den zu verwendenden Datenträgerentitätssatz an.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e6b-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="d9e6b-121">-DiskToInclude</span></span>
<span data-ttu-id="d9e6b-122">Gibt die Datenträger auf dem Quellserver an, die für die Replikation einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="d9e6b-123">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu den #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e6b-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="d9e6b-124">-DiskType</span></span>
<span data-ttu-id="d9e6b-125">Gibt den Datenträgertyp an, der für die Azure VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e6b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9e6b-126">-InputObject</span></span>
<span data-ttu-id="d9e6b-127">Gibt den ermittelten Server an, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="d9e6b-128">Das Serverobjekt kann mit dem cmdlet Get-AzMigrateServer abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="d9e6b-129">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e6b-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d9e6b-130">-LicenseType</span></span>
<span data-ttu-id="d9e6b-131">Gibt an, ob für den Zu migrierenden Quellserver der Hybridvorteil von Azure gilt.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e6b-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="d9e6b-132">-MachineId</span></span>
<span data-ttu-id="d9e6b-133">Gibt die Computer-ID des ermittelten Servers an, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e6b-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="d9e6b-134">-OSDiskID</span></span>
<span data-ttu-id="d9e6b-135">Gibt den Betriebssystemdatenträger für den Quellserver an, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9e6b-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="d9e6b-136">-PerformAutoResync</span></span>
<span data-ttu-id="d9e6b-137">Gibt an, ob die Replikation automatisch repariert wird, falls die Änderungsnachverfolgung für den Quellserver bei der Replikation verloren geht.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="d9e6b-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9e6b-138">-SubscriptionId</span></span>
<span data-ttu-id="d9e6b-139">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d9e6b-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d9e6b-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="d9e6b-141">Gibt den Verfügbarkeitssatz an, der für die Erstellung von VM verwendet werden soll. Dabei wird der Verfügbarkeitssatz angegeben, der für die Erstellung von VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="d9e6b-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="d9e6b-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="d9e6b-143">Gibt die Verfügbarkeitszone an, die für die Erstellung von VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="d9e6b-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9e6b-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="d9e6b-145">Gibt das Speicherkonto an, das für die Startdiagnose verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="d9e6b-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="d9e6b-146">-TargetNetworkId</span></span>
<span data-ttu-id="d9e6b-147">Gibt die ID des virtuellen Netzwerks innerhalb des Azure-Zielabonnements an, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="d9e6b-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="d9e6b-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="d9e6b-149">Gibt die Ressourcengruppen-ID innerhalb des Azure-Zielabonnements an, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="d9e6b-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="d9e6b-150">-TargetSubnetName</span></span>
<span data-ttu-id="d9e6b-151">Gibt den Subnetznamen innerhalb des virtuellen Zielnetzwerks an, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="d9e6b-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="d9e6b-152">-TargetVMName</span></span>
<span data-ttu-id="d9e6b-153">Gibt den Namen der Azure VM an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="d9e6b-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="d9e6b-154">-TargetVMSize</span></span>
<span data-ttu-id="d9e6b-155">Gibt die SKU der zu erstellenden Azure VM an.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="d9e6b-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="d9e6b-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="d9e6b-157">Konto-ID.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-157">Account id.</span></span>

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

### <span data-ttu-id="d9e6b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e6b-158">CommonParameters</span></span>
<span data-ttu-id="d9e6b-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e6b-160">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9e6b-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e6b-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9e6b-161">INPUTS</span></span>

## <span data-ttu-id="d9e6b-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9e6b-162">OUTPUTS</span></span>

### <span data-ttu-id="d9e6b-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="d9e6b-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="d9e6b-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d9e6b-164">NOTES</span></span>

<span data-ttu-id="d9e6b-165">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d9e6b-165">ALIASES</span></span>

<span data-ttu-id="d9e6b-166">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d9e6b-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d9e6b-167">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9e6b-168">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d9e6b-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Gibt die Datenträger auf dem Quellserver an, die für die Replikation einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="d9e6b-170">`DiskId <String>`: Die Datenträger-ID.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="d9e6b-171">`IsOSDisk <String>`: Ein Wert, der angibt, ob es sich bei dem Datenträger um den Betriebssystemdatenträger handelt.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="d9e6b-172">`LogStorageAccountId <String>`: Das Protokollspeicherkonto ARM ID.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="d9e6b-173">`LogStorageAccountSasSecretName <String>`: Der geheime Schlüsselname des Protokollspeicherkontos.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="d9e6b-174">`[DiskEncryptionSetId <String>]`: Die DiskEncryptionSet-ARM-ID.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="d9e6b-175">`[DiskType <DiskAccountType?>]`: Der Datenträgertyp.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="d9e6b-176">INPUTOBJECT <IVMwareMachine> : Gibt den ermittelten Server an, der migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="d9e6b-177">Das Serverobjekt kann mit dem cmdlet Get-AzMigrateServer abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="d9e6b-178">`[GuestOSDetailOstype <String>]`: Typ des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="d9e6b-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="d9e6b-179">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d9e6b-179">RELATED LINKS</span></span>

