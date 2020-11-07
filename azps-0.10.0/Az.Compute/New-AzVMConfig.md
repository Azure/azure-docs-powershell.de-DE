---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 4b128346d77e090e5b0699ace8f03eaa9a4786a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844471"
---
# <span data-ttu-id="bffa5-101">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="bffa5-101">New-AzVMConfig</span></span>

## <span data-ttu-id="bffa5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bffa5-102">SYNOPSIS</span></span>
<span data-ttu-id="bffa5-103">Erstellt ein konfigurierbares Virtual Machine-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bffa5-103">Creates a configurable virtual machine object.</span></span>

## <span data-ttu-id="bffa5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bffa5-104">SYNTAX</span></span>

### <span data-ttu-id="bffa5-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bffa5-105">DefaultParameterSet (Default)</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bffa5-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="bffa5-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bffa5-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="bffa5-107">AssignIdentityParameterSet</span></span>
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bffa5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bffa5-108">DESCRIPTION</span></span>
<span data-ttu-id="bffa5-109">Das Cmdlet **New-AzVMConfig** erstellt ein konfigurierbares lokales virtuelles Computerobjekt für Azure.</span><span class="sxs-lookup"><span data-stu-id="bffa5-109">The **New-AzVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="bffa5-110">Andere Cmdlets können verwendet werden, um ein Objekt eines virtuellen Computers wie "AzVMOperatingSystem", "AzVMSourceImage", "Add-AzVMNetworkInterface" und "Menge-AzVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bffa5-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

## <span data-ttu-id="bffa5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bffa5-111">EXAMPLES</span></span>

### <span data-ttu-id="bffa5-112">Beispiel 1: Erstellen eines virtuellen Computerobjekts</span><span class="sxs-lookup"><span data-stu-id="bffa5-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="bffa5-113">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="bffa5-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="bffa5-114">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="bffa5-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bffa5-115">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="bffa5-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bffa5-116">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="bffa5-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="bffa5-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="bffa5-117">PARAMETERS</span></span>

### <span data-ttu-id="bffa5-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="bffa5-118">-AssignIdentity</span></span>
<span data-ttu-id="bffa5-119">Geben Sie die dem virtuellen Computer zugewiesene Identität für das System an.</span><span class="sxs-lookup"><span data-stu-id="bffa5-119">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="bffa5-120">-AvailabilitySetId</span></span>
<span data-ttu-id="bffa5-121">Gibt die ID eines Verfügbarkeits Satzes an.</span><span class="sxs-lookup"><span data-stu-id="bffa5-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="bffa5-122">Verwenden Sie zum Abrufen eines Verfügbarkeits Satz-Objekts das Get-AzAvailabilitySet-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bffa5-122">To obtain an availability set object, use the Get-AzAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="bffa5-123">Das Verfügbarkeits Satz-Objekt enthält eine ID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bffa5-123">The availability set object contains an ID property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bffa5-124">-DefaultProfile</span></span>
<span data-ttu-id="bffa5-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bffa5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-126">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="bffa5-126">-IdentityId</span></span>
<span data-ttu-id="bffa5-127">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bffa5-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="bffa5-128">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="bffa5-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="bffa5-129">-IdentityType</span></span>
<span data-ttu-id="bffa5-130">Die Identität des virtuellen Computers, falls konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="bffa5-130">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bffa5-131">-LicenseType</span></span>
<span data-ttu-id="bffa5-132">Der Lizenztyp, der für die Einführung Ihres eigenen Lizenz Szenarios geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="bffa5-132">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-133">-Tags</span><span class="sxs-lookup"><span data-stu-id="bffa5-133">-Tags</span></span>
<span data-ttu-id="bffa5-134">Die Tags, die der Ressource angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="bffa5-134">The tags attached to the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="bffa5-135">-VMName</span></span>
<span data-ttu-id="bffa5-136">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="bffa5-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="bffa5-137">-VMSize</span></span>
<span data-ttu-id="bffa5-138">Gibt die Größe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="bffa5-138">Specifies the size for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="bffa5-139">-Zone</span></span>
<span data-ttu-id="bffa5-140">Gibt die Zonenliste für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="bffa5-140">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bffa5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffa5-141">CommonParameters</span></span>
<span data-ttu-id="bffa5-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bffa5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffa5-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bffa5-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffa5-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bffa5-144">INPUTS</span></span>

### <span data-ttu-id="bffa5-145">Keine</span><span class="sxs-lookup"><span data-stu-id="bffa5-145">None</span></span>
<span data-ttu-id="bffa5-146">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bffa5-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bffa5-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bffa5-147">OUTPUTS</span></span>

### <span data-ttu-id="bffa5-148">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bffa5-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bffa5-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="bffa5-149">NOTES</span></span>

## <span data-ttu-id="bffa5-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bffa5-150">RELATED LINKS</span></span>

[<span data-ttu-id="bffa5-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bffa5-151">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="bffa5-152">Satz-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bffa5-152">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="bffa5-153">Satz-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="bffa5-153">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="bffa5-154">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="bffa5-154">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)


