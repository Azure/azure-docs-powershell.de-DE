---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 2022a8a830d868f412e505f23e65c4c297bea543
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505170"
---
# <span data-ttu-id="867b4-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="867b4-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="867b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="867b4-102">SYNOPSIS</span></span>
<span data-ttu-id="867b4-103">Erstellt ein konfigurierbares Virtual Machine-Objekt.</span><span class="sxs-lookup"><span data-stu-id="867b4-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="867b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="867b4-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [[-IdentityType] <ResourceIdentityType>] [-AssignIdentity] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="867b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="867b4-105">DESCRIPTION</span></span>
<span data-ttu-id="867b4-106">Das Cmdlet **New-AzureRmVMConfig** erstellt ein konfigurierbares lokales virtuelles Computerobjekt für Azure.</span><span class="sxs-lookup"><span data-stu-id="867b4-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="867b4-107">Andere Cmdlets können verwendet werden, um ein Objekt eines virtuellen Computers wie "AzureRmVMOperatingSystem", "AzureRmVMSourceImage", "Add-AzureRmVMNetworkInterface" und "Menge-AzureRmVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="867b4-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="867b4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="867b4-108">EXAMPLES</span></span>

### <span data-ttu-id="867b4-109">Beispiel 1: Erstellen eines virtuellen Computerobjekts</span><span class="sxs-lookup"><span data-stu-id="867b4-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="867b4-110">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="867b4-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="867b4-111">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="867b4-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="867b4-112">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="867b4-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="867b4-113">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="867b4-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="867b4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="867b4-114">PARAMETERS</span></span>

### <span data-ttu-id="867b4-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="867b4-115">-AssignIdentity</span></span>
<span data-ttu-id="867b4-116">Geben Sie die dem virtuellen Computer zugewiesene Identität für das System an.</span><span class="sxs-lookup"><span data-stu-id="867b4-116">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="867b4-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="867b4-117">-AvailabilitySetId</span></span>
<span data-ttu-id="867b4-118">Gibt die ID eines Verfügbarkeits Satzes an.</span><span class="sxs-lookup"><span data-stu-id="867b4-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="867b4-119">Verwenden Sie zum Abrufen eines Verfügbarkeits Satz-Objekts das Get-AzureRmAvailabilitySet-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="867b4-119">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="867b4-120">Das Verfügbarkeits Satz-Objekt enthält eine ID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="867b4-120">The availability set object contains an ID property.</span></span>

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

### <span data-ttu-id="867b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867b4-121">-DefaultProfile</span></span>
<span data-ttu-id="867b4-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="867b4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="867b4-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="867b4-123">-IdentityType</span></span>
<span data-ttu-id="867b4-124">Die Identität des virtuellen Computers, falls konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="867b4-124">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="867b4-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="867b4-125">-LicenseType</span></span>
<span data-ttu-id="867b4-126">Der Lizenztyp, der für die Einführung Ihres eigenen Lizenz Szenarios geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="867b4-126">The license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="867b4-127">-Tags</span><span class="sxs-lookup"><span data-stu-id="867b4-127">-Tags</span></span>
<span data-ttu-id="867b4-128">Die Tags, die der Ressource angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="867b4-128">The tags attached to the resource.</span></span>

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

### <span data-ttu-id="867b4-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="867b4-129">-VMName</span></span>
<span data-ttu-id="867b4-130">Gibt einen Namen für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="867b4-130">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="867b4-131">-VMSize</span><span class="sxs-lookup"><span data-stu-id="867b4-131">-VMSize</span></span>
<span data-ttu-id="867b4-132">Gibt die Größe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="867b4-132">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="867b4-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="867b4-133">-Zone</span></span>
<span data-ttu-id="867b4-134">Gibt die Zonenliste für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="867b4-134">Specifies the zone list for the virtual machine.</span></span>

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

### <span data-ttu-id="867b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867b4-135">CommonParameters</span></span>
<span data-ttu-id="867b4-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="867b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867b4-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="867b4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867b4-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="867b4-138">INPUTS</span></span>

## <span data-ttu-id="867b4-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="867b4-139">OUTPUTS</span></span>

## <span data-ttu-id="867b4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="867b4-140">NOTES</span></span>

## <span data-ttu-id="867b4-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="867b4-141">RELATED LINKS</span></span>

[<span data-ttu-id="867b4-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="867b4-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="867b4-143">Satz-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="867b4-143">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="867b4-144">Satz-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="867b4-144">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="867b4-145">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="867b4-145">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


