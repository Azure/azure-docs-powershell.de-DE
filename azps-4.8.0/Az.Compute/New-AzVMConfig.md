---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 8c20a6be76f77a74082090d1386054a23b9b9ea0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167120"
---
# <span data-ttu-id="bd1ee-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="bd1ee-101">New-AzVMConfig</span></span>

## <span data-ttu-id="bd1ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd1ee-102">SYNOPSIS</span></span>
<span data-ttu-id="bd1ee-103">Erstellt ein konfigurierbares Virtual Machine-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="bd1ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd1ee-104">SYNTAX</span></span>

### <span data-ttu-id="bd1ee-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd1ee-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd1ee-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd1ee-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd1ee-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd1ee-107">DESCRIPTION</span></span>
<span data-ttu-id="bd1ee-108">Das Cmdlet **New-AzVMConfig** erstellt ein konfigurierbares lokales virtuelles Computerobjekt für Azure.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="bd1ee-109">Andere Cmdlets können verwendet werden, um ein Objekt eines virtuellen Computers wie "AzVMOperatingSystem", "AzVMSourceImage", "Add-AzVMNetworkInterface" und "Menge-AzVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="bd1ee-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd1ee-110">EXAMPLES</span></span>

### <span data-ttu-id="bd1ee-111">Beispiel 1: Erstellen eines virtuellen Computerobjekts</span><span class="sxs-lookup"><span data-stu-id="bd1ee-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="bd1ee-112">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="bd1ee-113">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bd1ee-114">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bd1ee-115">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="bd1ee-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd1ee-116">PARAMETERS</span></span>

### <span data-ttu-id="bd1ee-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="bd1ee-117">-AvailabilitySetId</span></span>
<span data-ttu-id="bd1ee-118">Gibt die ID eines Verfügbarkeits Satzes an.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="bd1ee-119">Verwenden Sie zum Abrufen eines Verfügbarkeits Satz-Objekts das Get-AzAvailabilitySet-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="bd1ee-120">Das Verfügbarkeits Satz-Objekt enthält eine ID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="bd1ee-121">Virtuelle Computer, die im gleichen Verfügbarkeits Satz angegeben sind, werden unterschiedlichen Knoten zugewiesen, um die Verfügbarkeit zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="bd1ee-122">Weitere Informationen zu Verfügbarkeits Sätzen finden Sie unter [Verwalten der Verfügbarkeit virtueller Computer](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="bd1ee-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="bd1ee-123">Weitere Informationen zu Azure Planned Maintenance finden Sie unter [geplante Wartung für virtuelle Computer in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) .</span><span class="sxs-lookup"><span data-stu-id="bd1ee-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="bd1ee-124">Derzeit kann eine VM nur zum Zeitpunkt der Erstellung der Verfügbarkeitseinstellung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="bd1ee-125">Der Verfügbarkeits Satz, dem der VM hinzugefügt wird, sollte der gleichen Ressourcengruppe wie die Verfügbarkeits Satz-Ressource entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="bd1ee-126">Ein vorhandener VM kann einem Verfügbarkeits Satz nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="bd1ee-127">Diese Eigenschaft kann nicht zusammen mit einem nicht-NULL-Eigenschaften-virtualMachineScaleSet-Verweis vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd1ee-128">-DefaultProfile</span></span>
<span data-ttu-id="bd1ee-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="bd1ee-130">-EnableUltraSSD</span></span>
<span data-ttu-id="bd1ee-131">Aktiviert eine Funktion, die einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem virtuellen Computer hat.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="bd1ee-132">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="bd1ee-133">-EvictionPolicy</span></span>
<span data-ttu-id="bd1ee-134">Die Räumungs Richtlinie für den virtuellen Azure Spot-Computer.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="bd1ee-135">Unterstützte Werte sind "freigeben" und "Löschen".</span><span class="sxs-lookup"><span data-stu-id="bd1ee-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-136">-Host-Nr</span><span class="sxs-lookup"><span data-stu-id="bd1ee-136">-HostId</span></span>
<span data-ttu-id="bd1ee-137">Die ID des Hosts</span><span class="sxs-lookup"><span data-stu-id="bd1ee-137">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-138">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="bd1ee-138">-IdentityId</span></span>
<span data-ttu-id="bd1ee-139">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="bd1ee-140">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="bd1ee-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="bd1ee-141">-IdentityType</span></span>
<span data-ttu-id="bd1ee-142">Die Identität des virtuellen Computers, falls konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-142">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bd1ee-143">-LicenseType</span></span>
<span data-ttu-id="bd1ee-144">Der Lizenztyp, der für die Einführung Ihres eigenen Lizenz Szenarios geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-144">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-145">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="bd1ee-145">-MaxPrice</span></span>
<span data-ttu-id="bd1ee-146">Gibt den Höchstpreis an, den Sie für eine VM-VMSS mit niedriger Priorität bezahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-146">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="bd1ee-147">Dieser Preis ist in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-147">This price is in US Dollars.</span></span> <span data-ttu-id="bd1ee-148">Dieser Preis wird mit dem aktuellen Preis für niedrige Priorität für die VM-Größe verglichen.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-148">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="bd1ee-149">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM-VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der maxprice größer als der aktuelle Preis für niedrige Priorität ist.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-149">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="bd1ee-150">Die maxprice wird auch zum Entfernen einer VM-VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis für niedrige Priorität über die maxprice nach der Erstellung von VM/VMSS hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-150">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="bd1ee-151">Mögliche Werte sind: beliebiger Dezimalwert größer als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bd1ee-151">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="bd1ee-152">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-152">Example: 0.01538.</span></span>  <span data-ttu-id="bd1ee-153">-1 gibt an, dass die VM-VMSS mit niedriger Priorität aus Preisgründen nicht vertrieben werden sollte.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-153">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="bd1ee-154">Außerdem ist der standardmäßige Höchstpreis-1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-154">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-155">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="bd1ee-155">-EncryptionAtHost</span></span>
<span data-ttu-id="bd1ee-156">Die EncryptionAtHost-Eigenschaft kann vom Benutzer in der Anforderung zum Aktivieren oder Deaktivieren der Host Verschlüsselung für den Skalierungs Satz der virtuellen Maschine oder des virtuellen Computers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-156">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="bd1ee-157">Dadurch wird die Verschlüsselung für alle Datenträger einschließlich des Ressourcen/temporären Datenträgers am Host selbst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-157">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="bd1ee-158">Standard: die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-158">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-159">-Priorität</span><span class="sxs-lookup"><span data-stu-id="bd1ee-159">-Priority</span></span>
<span data-ttu-id="bd1ee-160">Die Priorität für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-160">The priority for the virtual machine.</span></span>  <span data-ttu-id="bd1ee-161">Nur Unterstützte Werte sind "Normal", "Spot" und "Low".</span><span class="sxs-lookup"><span data-stu-id="bd1ee-161">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="bd1ee-162">"Normal" ist für normalen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-162">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="bd1ee-163">"Spot" ist für Spot Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-163">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="bd1ee-164">"Low" ist auch für Spot Virtual Machine, wird aber durch "Spot" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-164">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="bd1ee-165">Bitte verwenden Sie "Spot" anstelle von "Low".</span><span class="sxs-lookup"><span data-stu-id="bd1ee-165">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-166">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="bd1ee-166">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="bd1ee-167">Die Ressourcen-ID der für diesen virtuellen Computer zu verwendenden Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-167">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-168">-Tags</span><span class="sxs-lookup"><span data-stu-id="bd1ee-168">-Tags</span></span>
<span data-ttu-id="bd1ee-169">Die Tags, die der Ressource angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-169">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-170">-VMName</span><span class="sxs-lookup"><span data-stu-id="bd1ee-170">-VMName</span></span>
<span data-ttu-id="bd1ee-171">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-171">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-172">-VMSize</span><span class="sxs-lookup"><span data-stu-id="bd1ee-172">-VMSize</span></span>
<span data-ttu-id="bd1ee-173">Gibt die Größe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-173">Specifies the size for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-174">-VmssId</span><span class="sxs-lookup"><span data-stu-id="bd1ee-174">-VmssId</span></span>
<span data-ttu-id="bd1ee-175">Die ID des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="bd1ee-175">The Id of virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-176">-Zone</span><span class="sxs-lookup"><span data-stu-id="bd1ee-176">-Zone</span></span>
<span data-ttu-id="bd1ee-177">Gibt die Liste der verfügbaren Zonen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-177">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="bd1ee-178">Die zulässigen Werte hängen von den Funktionen der Region ab.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-178">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="bd1ee-179">Zulässige Werte sind normalerweise 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-179">Allowed values will normally be 1,2,3.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1ee-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd1ee-180">CommonParameters</span></span>
<span data-ttu-id="bd1ee-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd1ee-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd1ee-182">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd1ee-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd1ee-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd1ee-183">INPUTS</span></span>

### <span data-ttu-id="bd1ee-184">System. String</span><span class="sxs-lookup"><span data-stu-id="bd1ee-184">System.String</span></span>

### <span data-ttu-id="bd1ee-185">System. String []</span><span class="sxs-lookup"><span data-stu-id="bd1ee-185">System.String[]</span></span>

### <span data-ttu-id="bd1ee-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd1ee-186">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bd1ee-187">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="bd1ee-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bd1ee-188">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd1ee-188">OUTPUTS</span></span>

### <span data-ttu-id="bd1ee-189">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bd1ee-189">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bd1ee-190">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd1ee-190">NOTES</span></span>

## <span data-ttu-id="bd1ee-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd1ee-191">RELATED LINKS</span></span>

[<span data-ttu-id="bd1ee-192">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd1ee-192">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="bd1ee-193">Satz-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bd1ee-193">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="bd1ee-194">Satz-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="bd1ee-194">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="bd1ee-195">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bd1ee-195">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


