---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 6809088110944648781fc2264bd2c56f98cbee1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499685"
---
# <span data-ttu-id="5d5cd-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="5d5cd-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="5d5cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5cd-103">Erstellt ein konfigurierbares Virtual Machine-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d5cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d5cd-104">SYNTAX</span></span>

### <span data-ttu-id="5d5cd-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d5cd-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d5cd-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d5cd-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d5cd-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d5cd-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d5cd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d5cd-108">DESCRIPTION</span></span>
<span data-ttu-id="5d5cd-109">Das Cmdlet **New-AzureRmVMConfig** erstellt ein konfigurierbares lokales virtuelles Computerobjekt für Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="5d5cd-110">Andere Cmdlets können verwendet werden, um ein Objekt eines virtuellen Computers wie "AzureRmVMOperatingSystem", "AzureRmVMSourceImage", "Add-AzureRmVMNetworkInterface" und "Menge-AzureRmVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="5d5cd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d5cd-111">EXAMPLES</span></span>

### <span data-ttu-id="5d5cd-112">Beispiel 1: Erstellen eines virtuellen Computerobjekts</span><span class="sxs-lookup"><span data-stu-id="5d5cd-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="5d5cd-113">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="5d5cd-114">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5d5cd-115">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="5d5cd-116">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="5d5cd-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d5cd-117">PARAMETERS</span></span>

### <span data-ttu-id="5d5cd-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5d5cd-118">-AssignIdentity</span></span>
<span data-ttu-id="5d5cd-119">Geben Sie die dem virtuellen Computer zugewiesene Identität für das System an.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="5d5cd-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="5d5cd-120">-AvailabilitySetId</span></span>
<span data-ttu-id="5d5cd-121">Gibt die ID eines Verfügbarkeits Satzes an.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="5d5cd-122">Verwenden Sie zum Abrufen eines Verfügbarkeits Satz-Objekts das Get-AzureRmAvailabilitySet-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="5d5cd-123">Das Verfügbarkeits Satz-Objekt enthält eine ID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="5d5cd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5cd-124">-DefaultProfile</span></span>
<span data-ttu-id="5d5cd-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5cd-126">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="5d5cd-126">-EnableUltraSSD</span></span>
<span data-ttu-id="5d5cd-127">Aktiviert eine Funktion, die einen oder mehrere verwaltete Datenlaufwerke mit UltraSSD_LRS Speicher Kontotyp auf dem virtuellen Computer hat.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-127">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="5d5cd-128">Verwaltete Datenträger mit Speicher Kontotyp UltraSSD_LRS können einem virtuellen Computer nur hinzugefügt werden, wenn diese Eigenschaft aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-128">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>


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

### <span data-ttu-id="5d5cd-129">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="5d5cd-129">-IdentityId</span></span>
<span data-ttu-id="5d5cd-130">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-130">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5d5cd-131">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="5d5cd-131">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="5d5cd-132">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5d5cd-132">-IdentityType</span></span>
<span data-ttu-id="5d5cd-133">Die Identität des virtuellen Computers, falls konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-133">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="5d5cd-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5d5cd-134">-LicenseType</span></span>
<span data-ttu-id="5d5cd-135">Der Lizenztyp, der für die Einführung Ihres eigenen Lizenz Szenarios geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-135">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="5d5cd-136">-Tags</span><span class="sxs-lookup"><span data-stu-id="5d5cd-136">-Tags</span></span>
<span data-ttu-id="5d5cd-137">Die Tags, die der Ressource angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-137">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="5d5cd-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="5d5cd-138">-VMName</span></span>
<span data-ttu-id="5d5cd-139">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-139">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="5d5cd-140">-VMSize</span><span class="sxs-lookup"><span data-stu-id="5d5cd-140">-VMSize</span></span>
<span data-ttu-id="5d5cd-141">Gibt die Größe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-141">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="5d5cd-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="5d5cd-142">-Zone</span></span>
<span data-ttu-id="5d5cd-143">Gibt die Zonenliste für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-143">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="5d5cd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5cd-144">CommonParameters</span></span>
<span data-ttu-id="5d5cd-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d5cd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d5cd-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d5cd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5cd-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d5cd-147">INPUTS</span></span>

### <span data-ttu-id="5d5cd-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5d5cd-148">System.String</span></span>

### <span data-ttu-id="5d5cd-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="5d5cd-149">System.String[]</span></span>

### <span data-ttu-id="5d5cd-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5d5cd-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5d5cd-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d5cd-151">OUTPUTS</span></span>

### <span data-ttu-id="5d5cd-152">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5d5cd-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5d5cd-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d5cd-153">NOTES</span></span>

## <span data-ttu-id="5d5cd-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d5cd-154">RELATED LINKS</span></span>

[<span data-ttu-id="5d5cd-155">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d5cd-155">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="5d5cd-156">Satz-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5d5cd-156">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="5d5cd-157">Satz-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5d5cd-157">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="5d5cd-158">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5d5cd-158">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


