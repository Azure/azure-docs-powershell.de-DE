---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: a53d8cc94ffcc34ddf32d9cfec3b543b0bd006e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996146"
---
# <span data-ttu-id="cd3bb-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="cd3bb-101">New-AzVMConfig</span></span>

## <span data-ttu-id="cd3bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd3bb-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3bb-103">Erstellt ein konfigurierbares Virtual Machine-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="cd3bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd3bb-104">SYNTAX</span></span>

### <span data-ttu-id="cd3bb-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd3bb-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd3bb-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd3bb-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd3bb-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd3bb-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd3bb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd3bb-108">DESCRIPTION</span></span>
<span data-ttu-id="cd3bb-109">Das Cmdlet **New-AzVMConfig** erstellt ein konfigurierbares lokales virtuelles Computerobjekt für Azure.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="cd3bb-110">Andere Cmdlets können verwendet werden, um ein Objekt eines virtuellen Computers wie "AzVMOperatingSystem", "AzVMSourceImage", "Add-AzVMNetworkInterface" und "Menge-AzVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="cd3bb-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd3bb-111">EXAMPLES</span></span>

### <span data-ttu-id="cd3bb-112">Beispiel 1: Erstellen eines virtuellen Computerobjekts</span><span class="sxs-lookup"><span data-stu-id="cd3bb-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="cd3bb-113">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-113">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="cd3bb-114">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cd3bb-115">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="cd3bb-116">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="cd3bb-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd3bb-117">PARAMETERS</span></span>

### <span data-ttu-id="cd3bb-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cd3bb-118">-AssignIdentity</span></span>
<span data-ttu-id="cd3bb-119">Geben Sie die dem virtuellen Computer zugewiesene Identität für das System an.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd3bb-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="cd3bb-120">-AvailabilitySetId</span></span>
<span data-ttu-id="cd3bb-121">Gibt die ID eines Verfügbarkeits Satzes an.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="cd3bb-122">Verwenden Sie zum Abrufen eines Verfügbarkeits Satz-Objekts das Get-AzAvailabilitySet-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="cd3bb-123">Das Verfügbarkeits Satz-Objekt enthält eine ID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="cd3bb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3bb-124">-DefaultProfile</span></span>
<span data-ttu-id="cd3bb-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd3bb-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="cd3bb-126">-EnableUltraSSD</span></span>
<span data-ttu-id="cd3bb-127">Aktiviert eine Funktion, die einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem virtuellen Computer hat.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="cd3bb-128">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="cd3bb-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd3bb-129">-EvictionPolicy</span></span>
<span data-ttu-id="cd3bb-130">Die Räumungs Richtlinie für den virtuellen Computer mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-130">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="cd3bb-131">Nur unterstützter Wert ist "freigeben".</span><span class="sxs-lookup"><span data-stu-id="cd3bb-131">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="cd3bb-132">-Host-Nr</span><span class="sxs-lookup"><span data-stu-id="cd3bb-132">-HostId</span></span>
<span data-ttu-id="cd3bb-133">Die ID des Hosts</span><span class="sxs-lookup"><span data-stu-id="cd3bb-133">The Id of Host</span></span>

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

### <span data-ttu-id="cd3bb-134">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="cd3bb-134">-IdentityId</span></span>
<span data-ttu-id="cd3bb-135">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-135">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="cd3bb-136">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="cd3bb-136">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="cd3bb-137">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cd3bb-137">-IdentityType</span></span>
<span data-ttu-id="cd3bb-138">Die Identität des virtuellen Computers, falls konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-138">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="cd3bb-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="cd3bb-139">-LicenseType</span></span>
<span data-ttu-id="cd3bb-140">Der Lizenztyp, der für die Einführung Ihres eigenen Lizenz Szenarios geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-140">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="cd3bb-141">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="cd3bb-141">-MaxPrice</span></span>
<span data-ttu-id="cd3bb-142">Gibt den Höchstpreis an, den Sie für eine VM-VMSS mit niedriger Priorität bezahlen möchten.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-142">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="cd3bb-143">Dieser Preis ist in US-Dollar angegeben.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-143">This price is in US Dollars.</span></span> <span data-ttu-id="cd3bb-144">Dieser Preis wird mit dem aktuellen Preis für niedrige Priorität für die VM-Größe verglichen.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-144">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="cd3bb-145">Außerdem werden die Preise zum Zeitpunkt der Erstellung/Aktualisierung von VM-VMSS mit niedriger Priorität verglichen, und der Vorgang ist nur erfolgreich, wenn der maxprice größer als der aktuelle Preis für niedrige Priorität ist.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-145">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="cd3bb-146">Die maxprice wird auch zum Entfernen einer VM-VMSS mit niedriger Priorität verwendet, wenn der aktuelle Preis für niedrige Priorität über die maxprice nach der Erstellung von VM/VMSS hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-146">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="cd3bb-147">Mögliche Werte sind: beliebiger Dezimalwert größer als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cd3bb-147">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="cd3bb-148">Beispiel: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-148">Example: 0.01538.</span></span>  <span data-ttu-id="cd3bb-149">-1 gibt an, dass die VM-VMSS mit niedriger Priorität aus Preisgründen nicht vertrieben werden sollte.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-149">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="cd3bb-150">Außerdem ist der standardmäßige Höchstpreis-1, wenn er nicht von Ihnen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-150">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="cd3bb-151">-Priorität</span><span class="sxs-lookup"><span data-stu-id="cd3bb-151">-Priority</span></span>
<span data-ttu-id="cd3bb-152">Die Priorität für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-152">The priority for the virtual machine.</span></span>  <span data-ttu-id="cd3bb-153">Nur Unterstützte Werte sind "Normal", "Spot" und "Low".</span><span class="sxs-lookup"><span data-stu-id="cd3bb-153">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="cd3bb-154">"Normal" ist für normalen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-154">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="cd3bb-155">"Spot" ist für Spot Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-155">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="cd3bb-156">"Low" ist auch für Spot Virtual Machine, wird aber durch "Spot" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-156">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="cd3bb-157">Bitte verwenden Sie "Spot" anstelle von "Low".</span><span class="sxs-lookup"><span data-stu-id="cd3bb-157">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="cd3bb-158">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="cd3bb-158">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="cd3bb-159">Die Ressourcen-ID der für diesen virtuellen Computer zu verwendenden Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-159">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="cd3bb-160">-Tags</span><span class="sxs-lookup"><span data-stu-id="cd3bb-160">-Tags</span></span>
<span data-ttu-id="cd3bb-161">Die Tags, die der Ressource angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-161">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="cd3bb-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="cd3bb-162">-VMName</span></span>
<span data-ttu-id="cd3bb-163">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-163">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="cd3bb-164">-VMSize</span><span class="sxs-lookup"><span data-stu-id="cd3bb-164">-VMSize</span></span>
<span data-ttu-id="cd3bb-165">Gibt die Größe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-165">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="cd3bb-166">-VmssId</span><span class="sxs-lookup"><span data-stu-id="cd3bb-166">-VmssId</span></span>
<span data-ttu-id="cd3bb-167">Die ID des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="cd3bb-167">The Id of virtual machine scale set</span></span>

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

### <span data-ttu-id="cd3bb-168">-Zone</span><span class="sxs-lookup"><span data-stu-id="cd3bb-168">-Zone</span></span>
<span data-ttu-id="cd3bb-169">Gibt die Liste der verfügbaren Zonen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-169">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="cd3bb-170">Die zulässigen Werte hängen von den Funktionen der Region ab.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-170">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="cd3bb-171">Zulässige Werte sind normalerweise 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-171">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="cd3bb-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3bb-172">CommonParameters</span></span>
<span data-ttu-id="cd3bb-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd3bb-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3bb-174">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd3bb-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3bb-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd3bb-175">INPUTS</span></span>

### <span data-ttu-id="cd3bb-176">System. String</span><span class="sxs-lookup"><span data-stu-id="cd3bb-176">System.String</span></span>

### <span data-ttu-id="cd3bb-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="cd3bb-177">System.String[]</span></span>

### <span data-ttu-id="cd3bb-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cd3bb-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cd3bb-179">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="cd3bb-179">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cd3bb-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd3bb-180">OUTPUTS</span></span>

### <span data-ttu-id="cd3bb-181">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cd3bb-181">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="cd3bb-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd3bb-182">NOTES</span></span>

## <span data-ttu-id="cd3bb-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd3bb-183">RELATED LINKS</span></span>

[<span data-ttu-id="cd3bb-184">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="cd3bb-184">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="cd3bb-185">Satz-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="cd3bb-185">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="cd3bb-186">Satz-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="cd3bb-186">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="cd3bb-187">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cd3bb-187">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


