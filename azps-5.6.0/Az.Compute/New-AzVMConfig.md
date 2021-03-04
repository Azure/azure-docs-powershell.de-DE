---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938872"
---
# <span data-ttu-id="4f37c-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4f37c-101">New-AzVMConfig</span></span>

## <span data-ttu-id="4f37c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f37c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f37c-103">Erstellt ein konfigurierbares Objekt für einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4f37c-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="4f37c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f37c-104">SYNTAX</span></span>

### <span data-ttu-id="4f37c-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f37c-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f37c-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f37c-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f37c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f37c-107">DESCRIPTION</span></span>
<span data-ttu-id="4f37c-108">Das **Cmdlet New-AzVMConfig** erstellt ein konfigurierbares Objekt für einen lokalen virtuellen Computer für Azure.</span><span class="sxs-lookup"><span data-stu-id="4f37c-108">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="4f37c-109">Andere Cmdlets können zum Konfigurieren eines Virtuellen Computerobjekts verwendet werden, z. B. Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface und Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="4f37c-109">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="4f37c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f37c-110">EXAMPLES</span></span>

### <span data-ttu-id="4f37c-111">Beispiel 1: Erstellen eines Virtuellen Computerobjekts</span><span class="sxs-lookup"><span data-stu-id="4f37c-111">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="4f37c-112">Der erste Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="4f37c-112">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4f37c-113">Mit dem zweiten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4f37c-113">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4f37c-114">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="4f37c-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4f37c-115">Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4f37c-115">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="4f37c-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4f37c-116">PARAMETERS</span></span>

### <span data-ttu-id="4f37c-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="4f37c-117">-AvailabilitySetId</span></span>
<span data-ttu-id="4f37c-118">Gibt die ID eines Verfügbarkeitssets an.</span><span class="sxs-lookup"><span data-stu-id="4f37c-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="4f37c-119">Um ein Verfügbarkeitssatzobjekt zu erhalten, verwenden Sie das Get-AzAvailabilitySet Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f37c-119">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="4f37c-120">Das Verfügbarkeitssatzobjekt enthält eine ID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4f37c-120">The availability set object contains an ID property.</span></span> <br>
<span data-ttu-id="4f37c-121">Virtuelle Computer, die im gleichen Verfügbarkeitssatz angegeben sind, werden verschiedenen Knoten zugeordnet, um die Verfügbarkeit zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="4f37c-121">Virtual machines specified in the same availability set are allocated to different nodes to maximize availability.</span></span> <br>
<span data-ttu-id="4f37c-122">Weitere Informationen zu Verfügbarkeitssätzen finden Sie unter [Verwalten der Verfügbarkeit virtueller Computer.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="4f37c-122">For more information about availability sets, see [Manage the availability of virtual machines](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json).</span></span> <br>
<span data-ttu-id="4f37c-123">Weitere Informationen zur geplanten Wartung von Azure finden Sie unter [Geplante Wartung für virtuelle Computer in Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="4f37c-123">For more information on Azure planned maintenance, see [Planned maintenance for virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)</span></span> <br>
<span data-ttu-id="4f37c-124">Derzeit kann eine VM nur zur Verfügbarkeit hinzugefügt werden, die zur Erstellungszeit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="4f37c-124">Currently, a VM can only be added to availability set at creation time.</span></span> <span data-ttu-id="4f37c-125">Der Verfügbarkeitssatz, dem der virtuelle Computer hinzugefügt wird, sollte sich unter derselben Ressourcengruppe wie die Verfügbarkeitssatzressource befindet.</span><span class="sxs-lookup"><span data-stu-id="4f37c-125">The availability set to which the VM is being added should be under the same resource group as the availability set resource.</span></span> <span data-ttu-id="4f37c-126">Eine vorhandene VM kann einem Verfügbarkeitssatz nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4f37c-126">An existing VM cannot be added to an availability set.</span></span> <br>
<span data-ttu-id="4f37c-127">Diese Eigenschaft kann nicht zusammen mit einem Verweis auf "non-null properties.virtualMachineScaleSet" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4f37c-127">This property cannot exist along with a non-null properties.virtualMachineScaleSet reference.</span></span>

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

### <span data-ttu-id="4f37c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f37c-128">-DefaultProfile</span></span>
<span data-ttu-id="4f37c-129">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f37c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f37c-130">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="4f37c-130">-EnableUltraSSD</span></span>
<span data-ttu-id="4f37c-131">Ermöglicht eine Funktion, über eine oder mehrere verwaltete Datenträger mit UltraSSD_LRS Speicherkontotyp auf der VM zu verfügen.</span><span class="sxs-lookup"><span data-stu-id="4f37c-131">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="4f37c-132">Verwaltete Datenträger mit Speicherkontotyp UltraSSD_LRS einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4f37c-132">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="4f37c-133">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f37c-133">-EvictionPolicy</span></span>
<span data-ttu-id="4f37c-134">Die Räumungsrichtlinie für den virtuellen Azure Spot-Computer.</span><span class="sxs-lookup"><span data-stu-id="4f37c-134">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="4f37c-135">Unterstützte Werte sind "Deallocate" und "Delete".</span><span class="sxs-lookup"><span data-stu-id="4f37c-135">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="4f37c-136">-HostId</span><span class="sxs-lookup"><span data-stu-id="4f37c-136">-HostId</span></span>
<span data-ttu-id="4f37c-137">Die Id des Hosts</span><span class="sxs-lookup"><span data-stu-id="4f37c-137">The Id of Host</span></span>

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

### <span data-ttu-id="4f37c-138">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="4f37c-138">-IdentityId</span></span>
<span data-ttu-id="4f37c-139">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungssatz für virtuelle Computer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4f37c-139">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="4f37c-140">Die Benutzeridentitätsverweise werden ARM Ressourcen-ID im Formular "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f37c-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="4f37c-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4f37c-141">-IdentityType</span></span>
<span data-ttu-id="4f37c-142">Die Identität des virtuellen Computers, sofern konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4f37c-142">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="4f37c-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4f37c-143">-LicenseType</span></span>
<span data-ttu-id="4f37c-144">Gibt einen Lizenztyp an, der angibt, dass das Bild oder der Datenträger für den virtuellen Computer lokal lizenziert wurde.</span><span class="sxs-lookup"><span data-stu-id="4f37c-144">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="4f37c-145">Mögliche Werte für Windows Server sind:</span><span class="sxs-lookup"><span data-stu-id="4f37c-145">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="4f37c-146">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="4f37c-146">Windows_Client</span></span>
- <span data-ttu-id="4f37c-147">Windows_Server Mögliche Werte für Das Betriebssystem Linux Server sind:</span><span class="sxs-lookup"><span data-stu-id="4f37c-147">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="4f37c-148">RHEL_BYOS (für RREL)</span><span class="sxs-lookup"><span data-stu-id="4f37c-148">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="4f37c-149">SLES_BYOS (für SUSE)</span><span class="sxs-lookup"><span data-stu-id="4f37c-149">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="4f37c-150">-MaxPreis</span><span class="sxs-lookup"><span data-stu-id="4f37c-150">-MaxPrice</span></span>
<span data-ttu-id="4f37c-151">Gibt den Höchstpreis an, den Sie für eine VM/VMSS mit niedriger Priorität zahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="4f37c-151">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="4f37c-152">Dieser Preis ist in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="4f37c-152">This price is in US Dollars.</span></span> <span data-ttu-id="4f37c-153">Dieser Preis wird mit dem aktuellen Preis mit niedriger Priorität für die Größe des virtuellen Computers verglichen.</span><span class="sxs-lookup"><span data-stu-id="4f37c-153">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="4f37c-154">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM/VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der maxPreis größer als der aktuelle Preis mit niedriger Priorität ist.</span><span class="sxs-lookup"><span data-stu-id="4f37c-154">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="4f37c-155">Der maxPrice wird auch zum Räumung einer VM/VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis mit niedriger Priorität nach der Erstellung von VM/VMSS über den maxPreis hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="4f37c-155">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="4f37c-156">Mögliche Werte sind: jeder Dezimalwert größer als Null.</span><span class="sxs-lookup"><span data-stu-id="4f37c-156">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="4f37c-157">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="4f37c-157">Example: 0.01538.</span></span>  <span data-ttu-id="4f37c-158">-1 gibt an, dass die VM/VMSS mit niedriger Priorität aus Preisgründen nicht entfernt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="4f37c-158">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="4f37c-159">Außerdem ist der standardmäßige Höchstpreis -1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f37c-159">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="4f37c-160">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="4f37c-160">-EncryptionAtHost</span></span>
<span data-ttu-id="4f37c-161">Die EncryptionAtHost-Eigenschaft kann vom Benutzer in der Anforderung verwendet werden, um die Hostverschlüsselung für den Skalierungssatz des virtuellen Computers oder virtuellen Computers zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4f37c-161">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="4f37c-162">Dadurch wird die Verschlüsselung für alle Datenträger aktiviert, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst.</span><span class="sxs-lookup"><span data-stu-id="4f37c-162">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="4f37c-163">Standard: Die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4f37c-163">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="4f37c-164">-Priorität</span><span class="sxs-lookup"><span data-stu-id="4f37c-164">-Priority</span></span>
<span data-ttu-id="4f37c-165">Die Priorität für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4f37c-165">The priority for the virtual machine.</span></span>  <span data-ttu-id="4f37c-166">Nur unterstützte Werte sind "Normal", "Spot" und "Niedrig".</span><span class="sxs-lookup"><span data-stu-id="4f37c-166">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="4f37c-167">"Regular" ist für einen normalen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4f37c-167">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="4f37c-168">"Spot" ist für virtuelle Spotcomputer.</span><span class="sxs-lookup"><span data-stu-id="4f37c-168">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="4f37c-169">"Low" ist auch für virtuelle Spotcomputer, wird aber durch "Spot" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4f37c-169">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="4f37c-170">Verwenden Sie "Spot" statt "Niedrig".</span><span class="sxs-lookup"><span data-stu-id="4f37c-170">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="4f37c-171">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4f37c-171">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="4f37c-172">Die Ressourcen-ID der Näherungsgruppe, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f37c-172">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="4f37c-173">-Tags</span><span class="sxs-lookup"><span data-stu-id="4f37c-173">-Tags</span></span>
<span data-ttu-id="4f37c-174">Die Tags, die der Ressource angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="4f37c-174">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="4f37c-175">-VMName</span><span class="sxs-lookup"><span data-stu-id="4f37c-175">-VMName</span></span>
<span data-ttu-id="4f37c-176">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="4f37c-176">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="4f37c-177">-VMSize</span><span class="sxs-lookup"><span data-stu-id="4f37c-177">-VMSize</span></span>
<span data-ttu-id="4f37c-178">Gibt die Größe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="4f37c-178">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="4f37c-179">-VmssId</span><span class="sxs-lookup"><span data-stu-id="4f37c-179">-VmssId</span></span>
<span data-ttu-id="4f37c-180">Die ID des Skalierungssets für virtuelle Computer</span><span class="sxs-lookup"><span data-stu-id="4f37c-180">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="4f37c-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="4f37c-181">-Zone</span></span>
<span data-ttu-id="4f37c-182">Gibt die Liste der Verfügbarkeitszonen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="4f37c-182">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="4f37c-183">Die zulässigen Werte hängen von den Funktionen der Region ab.</span><span class="sxs-lookup"><span data-stu-id="4f37c-183">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="4f37c-184">Zulässige Werte sind normalerweise 1,2,3.</span><span class="sxs-lookup"><span data-stu-id="4f37c-184">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="4f37c-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f37c-185">CommonParameters</span></span>
<span data-ttu-id="4f37c-186">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f37c-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f37c-187">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f37c-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f37c-188">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f37c-188">INPUTS</span></span>

### <span data-ttu-id="4f37c-189">System.String</span><span class="sxs-lookup"><span data-stu-id="4f37c-189">System.String</span></span>

### <span data-ttu-id="4f37c-190">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4f37c-190">System.String[]</span></span>

### <span data-ttu-id="4f37c-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f37c-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4f37c-192">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4f37c-192">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4f37c-193">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f37c-193">OUTPUTS</span></span>

### <span data-ttu-id="4f37c-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4f37c-194">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4f37c-195">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4f37c-195">NOTES</span></span>

## <span data-ttu-id="4f37c-196">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4f37c-196">RELATED LINKS</span></span>

[<span data-ttu-id="4f37c-197">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4f37c-197">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="4f37c-198">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4f37c-198">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="4f37c-199">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="4f37c-199">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="4f37c-200">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4f37c-200">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


