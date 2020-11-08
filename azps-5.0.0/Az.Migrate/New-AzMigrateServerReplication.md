---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177520"
---
# <span data-ttu-id="19177-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="19177-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="19177-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19177-102">SYNOPSIS</span></span>
<span data-ttu-id="19177-103">Startet die Replikation für den angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="19177-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="19177-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19177-104">SYNTAX</span></span>

### <span data-ttu-id="19177-105">ByIdDefaultUser (Standard)</span><span class="sxs-lookup"><span data-stu-id="19177-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19177-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="19177-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19177-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="19177-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19177-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="19177-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="19177-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19177-109">DESCRIPTION</span></span>
<span data-ttu-id="19177-110">Das New-AzMigrateServerReplication-Cmdlet startet die Replikation für einen bestimmten ermittelten Server im Azure migrate-Projekt.</span><span class="sxs-lookup"><span data-stu-id="19177-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="19177-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19177-111">EXAMPLES</span></span>

### <span data-ttu-id="19177-112">Beispiel 1: Wenn nur ein Betriebssystemdatenträger vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="19177-112">Example 1: When there is only OS disk</span></span>
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

<span data-ttu-id="19177-113">Dies gilt für das Szenario, wenn nur ein einziger Datenträger vorhanden ist, der geschützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="19177-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="19177-114">Beispiel 2: Wenn mehrere Datenträger vorhanden sind</span><span class="sxs-lookup"><span data-stu-id="19177-114">Example 2: When there are multiple disks</span></span>
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

<span data-ttu-id="19177-115">Dies gilt für das Szenario, wenn mehrere Datenträger vorhanden sind, die geschützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="19177-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="19177-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="19177-116">PARAMETERS</span></span>

### <span data-ttu-id="19177-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19177-117">-DefaultProfile</span></span>
<span data-ttu-id="19177-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19177-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19177-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="19177-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="19177-120">Gibt den festgelegten Festplatten-Verschlüsselungs an.</span><span class="sxs-lookup"><span data-stu-id="19177-120">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="19177-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="19177-121">-DiskToInclude</span></span>
<span data-ttu-id="19177-122">Gibt die Datenträger auf dem Quellserver an, die für die Replikation einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19177-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="19177-123">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für DISKTOINCLUDE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="19177-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="19177-124">-Disktype</span><span class="sxs-lookup"><span data-stu-id="19177-124">-DiskType</span></span>
<span data-ttu-id="19177-125">Gibt den Typ der für den Azure VM zu verwendenden Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="19177-125">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="19177-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="19177-126">-InputObject</span></span>
<span data-ttu-id="19177-127">Gibt den zu migrierenden gefundenen Server an.</span><span class="sxs-lookup"><span data-stu-id="19177-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="19177-128">Das Serverobjekt kann mit dem Get-AzMigrateServer-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="19177-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="19177-129">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="19177-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="19177-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="19177-130">-LicenseType</span></span>
<span data-ttu-id="19177-131">Gibt an, ob Azure Hybrid Benefit für den zu migrierenden Quellserver gilt.</span><span class="sxs-lookup"><span data-stu-id="19177-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

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

### <span data-ttu-id="19177-132">-Maschinen-Nr</span><span class="sxs-lookup"><span data-stu-id="19177-132">-MachineId</span></span>
<span data-ttu-id="19177-133">Gibt die Computer-ID des zu migrierenden gefundenen Servers an.</span><span class="sxs-lookup"><span data-stu-id="19177-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="19177-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="19177-134">-OSDiskID</span></span>
<span data-ttu-id="19177-135">Gibt den Betriebs System Datenträger für den zu migrierenden Quellserver an.</span><span class="sxs-lookup"><span data-stu-id="19177-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

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

### <span data-ttu-id="19177-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="19177-136">-PerformAutoResync</span></span>
<span data-ttu-id="19177-137">Gibt an, ob die Replikation automatisch repariert werden soll, falls die Änderungsnachverfolgung für den Quellserver unter Replikation verloren geht.</span><span class="sxs-lookup"><span data-stu-id="19177-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="19177-138">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="19177-138">-SubscriptionId</span></span>
<span data-ttu-id="19177-139">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="19177-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="19177-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="19177-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="19177-141">Gibt den verfügbaren Verfügbarkeits Satz an, der für die VM-creationSpecifies des für die VM-Erstellung zu verwendenden Verfügbarkeits Satzes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19177-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="19177-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="19177-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="19177-143">Gibt die Verfügbarkeits Zone an, die für die VM-Erstellung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="19177-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="19177-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19177-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="19177-145">Gibt das für die Start Diagnose zu verwendende Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="19177-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="19177-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="19177-146">-TargetNetworkId</span></span>
<span data-ttu-id="19177-147">Gibt die virtuelle Netzwerk-ID innerhalb des Ziels Azure-Abonnements an, für das der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="19177-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="19177-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="19177-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="19177-149">Gibt die ID der Ressourcengruppe innerhalb des Ziels Azure-Abonnements an, für das der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="19177-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="19177-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="19177-150">-TargetSubnetName</span></span>
<span data-ttu-id="19177-151">Gibt den Namen des Subnetzes innerhalb des virtuellen Ziel Netowk an, zu dem der Server migriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="19177-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="19177-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="19177-152">-TargetVMName</span></span>
<span data-ttu-id="19177-153">Gibt den Namen der Azure VM an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="19177-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="19177-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="19177-154">-TargetVMSize</span></span>
<span data-ttu-id="19177-155">Gibt die SKU der Azure-VM an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="19177-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="19177-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="19177-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="19177-157">Konto-ID.</span><span class="sxs-lookup"><span data-stu-id="19177-157">Account id.</span></span>

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

### <span data-ttu-id="19177-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19177-158">CommonParameters</span></span>
<span data-ttu-id="19177-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19177-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19177-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19177-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19177-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19177-161">INPUTS</span></span>

## <span data-ttu-id="19177-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19177-162">OUTPUTS</span></span>

### <span data-ttu-id="19177-163">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="19177-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="19177-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="19177-164">NOTES</span></span>

<span data-ttu-id="19177-165">Aliase</span><span class="sxs-lookup"><span data-stu-id="19177-165">ALIASES</span></span>

<span data-ttu-id="19177-166">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19177-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19177-167">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="19177-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19177-168">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="19177-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19177-169">DISKTOINCLUDE <IVMwareCbtDiskInput [] >: gibt die Datenträger auf dem Quellserver an, die für die Replikation einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19177-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="19177-170">`DiskId <String>`: Die Datenträger-ID.</span><span class="sxs-lookup"><span data-stu-id="19177-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="19177-171">`IsOSDisk <String>`: Ein Wert, der angibt, ob es sich bei dem Datenträger um den Betriebssystemdatenträger handelt.</span><span class="sxs-lookup"><span data-stu-id="19177-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="19177-172">`LogStorageAccountId <String>`: Die ID des Protokollspeicher Kontos.</span><span class="sxs-lookup"><span data-stu-id="19177-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="19177-173">`LogStorageAccountSasSecretName <String>`: Der schlüsseltresor-geheim Name des Protokollspeicher Kontos.</span><span class="sxs-lookup"><span data-stu-id="19177-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="19177-174">`[DiskEncryptionSetId <String>]`: Die DiskEncryptionSet-Arm-ID.</span><span class="sxs-lookup"><span data-stu-id="19177-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="19177-175">`[DiskType <DiskAccountType?>]`: Der Datenträgertyp.</span><span class="sxs-lookup"><span data-stu-id="19177-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="19177-176">Inputobject <IVMwareMachine> : gibt den zu migrierenden gefundenen Server an.</span><span class="sxs-lookup"><span data-stu-id="19177-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="19177-177">Das Serverobjekt kann mit dem Get-AzMigrateServer-Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="19177-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="19177-178">`[GuestOSDetailOstype <String>]`: Typ des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="19177-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="19177-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19177-179">RELATED LINKS</span></span>

