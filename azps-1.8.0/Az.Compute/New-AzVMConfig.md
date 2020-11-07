---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4fd4c3a903910068933a46d3343e8dc990565b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661512"
---
# <span data-ttu-id="ac751-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ac751-101">New-AzVMConfig</span></span>

## <span data-ttu-id="ac751-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac751-102">SYNOPSIS</span></span>
<span data-ttu-id="ac751-103">Erstellt ein konfigurierbares Virtual Machine-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ac751-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="ac751-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac751-104">SYNTAX</span></span>

### <span data-ttu-id="ac751-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac751-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac751-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac751-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>] [-Tags <Hashtable>]
 [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac751-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac751-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac751-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac751-108">DESCRIPTION</span></span>
<span data-ttu-id="ac751-109">Das Cmdlet **New-AzVMConfig** erstellt ein konfigurierbares lokales virtuelles Computerobjekt für Azure.</span><span class="sxs-lookup"><span data-stu-id="ac751-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="ac751-110">Andere Cmdlets können verwendet werden, um ein Objekt eines virtuellen Computers wie "AzVMOperatingSystem", "AzVMSourceImage", "Add-AzVMNetworkInterface" und "Menge-AzVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ac751-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="ac751-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac751-111">EXAMPLES</span></span>

### <span data-ttu-id="ac751-112">Beispiel 1: Erstellen eines virtuellen Computerobjekts</span><span class="sxs-lookup"><span data-stu-id="ac751-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="ac751-113">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="ac751-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ac751-114">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ac751-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ac751-115">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="ac751-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ac751-116">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ac751-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="ac751-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac751-117">PARAMETERS</span></span>

### <span data-ttu-id="ac751-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ac751-118">-AssignIdentity</span></span>
<span data-ttu-id="ac751-119">Geben Sie die dem virtuellen Computer zugewiesene Identität für das System an.</span><span class="sxs-lookup"><span data-stu-id="ac751-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="ac751-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="ac751-120">-AvailabilitySetId</span></span>
<span data-ttu-id="ac751-121">Gibt die ID eines Verfügbarkeits Satzes an.</span><span class="sxs-lookup"><span data-stu-id="ac751-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="ac751-122">Verwenden Sie zum Abrufen eines Verfügbarkeits Satz-Objekts das Get-AzAvailabilitySet-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac751-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="ac751-123">Das Verfügbarkeits Satz-Objekt enthält eine ID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ac751-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="ac751-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac751-124">-DefaultProfile</span></span>
<span data-ttu-id="ac751-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac751-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac751-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="ac751-126">-EnableUltraSSD</span></span>
<span data-ttu-id="ac751-127">Aktiviert eine Funktion, die einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem virtuellen Computer hat.</span><span class="sxs-lookup"><span data-stu-id="ac751-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="ac751-128">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ac751-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="ac751-129">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="ac751-129">-IdentityId</span></span>
<span data-ttu-id="ac751-130">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ac751-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ac751-131">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="ac751-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ac751-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ac751-132">-IdentityType</span></span>
<span data-ttu-id="ac751-133">Die Identität des virtuellen Computers, falls konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ac751-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="ac751-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ac751-134">-LicenseType</span></span>
<span data-ttu-id="ac751-135">Der Lizenztyp, der für die Einführung Ihres eigenen Lizenz Szenarios geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="ac751-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ac751-136">-Tags</span><span class="sxs-lookup"><span data-stu-id="ac751-136">-Tags</span></span>
<span data-ttu-id="ac751-137">Die Tags, die der Ressource angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="ac751-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="ac751-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="ac751-138">-VMName</span></span>
<span data-ttu-id="ac751-139">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ac751-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="ac751-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="ac751-140">-VMSize</span></span>
<span data-ttu-id="ac751-141">Gibt die Größe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ac751-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="ac751-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="ac751-142">-Zone</span></span>
<span data-ttu-id="ac751-143">Gibt die Liste der verfügbaren Zonen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ac751-143">Specifies the availability zone list for the virtual machine.</span></span> <span data-ttu-id="ac751-144">Die zulässigen Werte hängen von den Funktionen der Region ab.</span><span class="sxs-lookup"><span data-stu-id="ac751-144">The allowed values depend on the capabilities of the region.</span></span> <span data-ttu-id="ac751-145">Zulässige Werte sind normalerweise 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="ac751-145">Allowed values will normally be 1,2,3.</span></span>

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

### <span data-ttu-id="ac751-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac751-146">CommonParameters</span></span>
<span data-ttu-id="ac751-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac751-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac751-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac751-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac751-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac751-149">INPUTS</span></span>

### <span data-ttu-id="ac751-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ac751-150">System.String</span></span>

### <span data-ttu-id="ac751-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="ac751-151">System.String[]</span></span>

### <span data-ttu-id="ac751-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ac751-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ac751-153">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="ac751-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac751-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac751-154">OUTPUTS</span></span>

### <span data-ttu-id="ac751-155">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ac751-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ac751-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac751-156">NOTES</span></span>

## <span data-ttu-id="ac751-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac751-157">RELATED LINKS</span></span>

[<span data-ttu-id="ac751-158">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ac751-158">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="ac751-159">Satz-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ac751-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="ac751-160">Satz-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="ac751-160">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="ac751-161">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ac751-161">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


