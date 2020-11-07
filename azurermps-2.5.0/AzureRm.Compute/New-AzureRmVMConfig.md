---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmconfig
schema: 2.0.0
ms.openlocfilehash: 3e42cf7c2be8433d9e1b7e85987e53b9f0050038
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850128"
---
# <span data-ttu-id="5b45d-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="5b45d-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="5b45d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b45d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b45d-103">Erstellt ein konfigurierbares Virtual Machine-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5b45d-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b45d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b45d-104">SYNTAX</span></span>

### <span data-ttu-id="5b45d-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b45d-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-Zone <String[]>] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b45d-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b45d-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b45d-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b45d-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [-AssignIdentity] [-Zone <String[]>] [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b45d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b45d-108">DESCRIPTION</span></span>
<span data-ttu-id="5b45d-109">Das Cmdlet **New-AzureRmVMConfig** erstellt ein konfigurierbares lokales virtuelles Computerobjekt für Azure.</span><span class="sxs-lookup"><span data-stu-id="5b45d-109">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="5b45d-110">Andere Cmdlets können verwendet werden, um ein Objekt eines virtuellen Computers wie "AzureRmVMOperatingSystem", "AzureRmVMSourceImage", "Add-AzureRmVMNetworkInterface" und "Menge-AzureRmVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5b45d-110">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="5b45d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b45d-111">EXAMPLES</span></span>

### <span data-ttu-id="5b45d-112">Beispiel 1: Erstellen eines virtuellen Computerobjekts</span><span class="sxs-lookup"><span data-stu-id="5b45d-112">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="5b45d-113">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="5b45d-113">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="5b45d-114">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5b45d-114">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5b45d-115">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="5b45d-115">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="5b45d-116">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5b45d-116">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="5b45d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b45d-117">PARAMETERS</span></span>

### <span data-ttu-id="5b45d-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5b45d-118">-AssignIdentity</span></span>
<span data-ttu-id="5b45d-119">Geben Sie die dem virtuellen Computer zugewiesene Identität für das System an.</span><span class="sxs-lookup"><span data-stu-id="5b45d-119">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="5b45d-120">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="5b45d-120">-AvailabilitySetId</span></span>
<span data-ttu-id="5b45d-121">Gibt die ID eines Verfügbarkeits Satzes an.</span><span class="sxs-lookup"><span data-stu-id="5b45d-121">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="5b45d-122">Verwenden Sie zum Abrufen eines Verfügbarkeits Satz-Objekts das Get-AzureRmAvailabilitySet-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b45d-122">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="5b45d-123">Das Verfügbarkeits Satz-Objekt enthält eine ID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5b45d-123">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="5b45d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b45d-124">-DefaultProfile</span></span>
<span data-ttu-id="5b45d-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b45d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b45d-126">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="5b45d-126">-IdentityId</span></span>
<span data-ttu-id="5b45d-127">Gibt die Liste der Benutzeridentitäten an, die dem Skalierungs Satz der virtuellen Maschine zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5b45d-127">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5b45d-128">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="5b45d-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="5b45d-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5b45d-129">-IdentityType</span></span>
<span data-ttu-id="5b45d-130">Die Identität des virtuellen Computers, falls konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="5b45d-130">The identity of the virtual machine, if configured.</span></span>

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

### <span data-ttu-id="5b45d-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5b45d-131">-LicenseType</span></span>
<span data-ttu-id="5b45d-132">Der Lizenztyp, der für die Einführung Ihres eigenen Lizenz Szenarios geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="5b45d-132">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="5b45d-133">-Tags</span><span class="sxs-lookup"><span data-stu-id="5b45d-133">-Tags</span></span>
<span data-ttu-id="5b45d-134">Die Tags, die der Ressource angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="5b45d-134">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="5b45d-135">-VMName</span><span class="sxs-lookup"><span data-stu-id="5b45d-135">-VMName</span></span>
<span data-ttu-id="5b45d-136">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="5b45d-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="5b45d-137">-VMSize</span><span class="sxs-lookup"><span data-stu-id="5b45d-137">-VMSize</span></span>
<span data-ttu-id="5b45d-138">Gibt die Größe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="5b45d-138">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="5b45d-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="5b45d-139">-Zone</span></span>
<span data-ttu-id="5b45d-140">Gibt die Zonenliste für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="5b45d-140">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="5b45d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b45d-141">CommonParameters</span></span>
<span data-ttu-id="5b45d-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b45d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b45d-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b45d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b45d-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b45d-144">INPUTS</span></span>

### <span data-ttu-id="5b45d-145">Keine</span><span class="sxs-lookup"><span data-stu-id="5b45d-145">None</span></span>
<span data-ttu-id="5b45d-146">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5b45d-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b45d-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b45d-147">OUTPUTS</span></span>

### <span data-ttu-id="5b45d-148">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5b45d-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5b45d-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b45d-149">NOTES</span></span>

## <span data-ttu-id="5b45d-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b45d-150">RELATED LINKS</span></span>

[<span data-ttu-id="5b45d-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5b45d-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="5b45d-152">Satz-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5b45d-152">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="5b45d-153">Satz-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5b45d-153">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="5b45d-154">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5b45d-154">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


