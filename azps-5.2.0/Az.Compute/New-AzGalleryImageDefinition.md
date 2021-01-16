---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357046"
---
# <span data-ttu-id="58fb2-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="58fb2-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="58fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="58fb2-103">Erstellen sie eine Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="58fb2-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="58fb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58fb2-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58fb2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="58fb2-106">Erstellen sie eine Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="58fb2-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="58fb2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58fb2-107">EXAMPLES</span></span>

### <span data-ttu-id="58fb2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58fb2-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="58fb2-109">Erstellen sie eine Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="58fb2-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="58fb2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58fb2-110">PARAMETERS</span></span>

### <span data-ttu-id="58fb2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58fb2-111">-AsJob</span></span>
<span data-ttu-id="58fb2-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="58fb2-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58fb2-113">-DefaultProfile</span></span>
<span data-ttu-id="58fb2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58fb2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58fb2-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58fb2-115">-Description</span></span>
<span data-ttu-id="58fb2-116">Die Beschreibung der Bilddefinitionsressource des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="58fb2-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="58fb2-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="58fb2-117">-DisallowedDiskType</span></span>
<span data-ttu-id="58fb2-118">Die unzulässigen Datenträgertypen.</span><span class="sxs-lookup"><span data-stu-id="58fb2-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="58fb2-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="58fb2-119">-EndOfLifeDate</span></span>
<span data-ttu-id="58fb2-120">Das Datum des Lebenszyklusendes der Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="58fb2-120">The end of life date of the gallery Image Definition</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="58fb2-121">-Eula</span></span>
<span data-ttu-id="58fb2-122">Die Vereinbarung "Eula" für die Bilddefinition der Galerie.</span><span class="sxs-lookup"><span data-stu-id="58fb2-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="58fb2-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="58fb2-123">-GalleryName</span></span>
<span data-ttu-id="58fb2-124">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="58fb2-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="58fb2-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="58fb2-125">-HyperVGeneration</span></span>
<span data-ttu-id="58fb2-126">Die Hypervisorgenerierung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="58fb2-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="58fb2-127">Gilt nur für Betriebssystemdatenträger.</span><span class="sxs-lookup"><span data-stu-id="58fb2-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="58fb2-128">Zulässige Werte sind V1 und V2.</span><span class="sxs-lookup"><span data-stu-id="58fb2-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="58fb2-129">-Location</span><span class="sxs-lookup"><span data-stu-id="58fb2-129">-Location</span></span>
<span data-ttu-id="58fb2-130">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="58fb2-130">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="58fb2-131">-MaximumMemory</span></span>
<span data-ttu-id="58fb2-132">Das Maximum des empfohlenen Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="58fb2-132">The maximum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="58fb2-133">-MaximumVCPU</span></span>
<span data-ttu-id="58fb2-134">Das Maximum des empfohlenen</span><span class="sxs-lookup"><span data-stu-id="58fb2-134">The maximum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="58fb2-135">-MinimumMemory</span></span>
<span data-ttu-id="58fb2-136">Das Minimum des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="58fb2-136">The minimum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="58fb2-137">-MinimumVCPU</span></span>
<span data-ttu-id="58fb2-138">Das Minimum des empfohlenen</span><span class="sxs-lookup"><span data-stu-id="58fb2-138">The minimum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-139">-Name</span><span class="sxs-lookup"><span data-stu-id="58fb2-139">-Name</span></span>
<span data-ttu-id="58fb2-140">Der Name der Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="58fb2-140">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-141">-Offer</span><span class="sxs-lookup"><span data-stu-id="58fb2-141">-Offer</span></span>
<span data-ttu-id="58fb2-142">Der Name des Katalog-Bilderdefinitionsangebots.</span><span class="sxs-lookup"><span data-stu-id="58fb2-142">The name of the gallery Image Definition offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="58fb2-143">-OsState</span></span>
<span data-ttu-id="58fb2-144">Der Zustand des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="58fb2-144">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="58fb2-145">-OsType</span></span>
<span data-ttu-id="58fb2-146">Der Typ des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="58fb2-146">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="58fb2-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="58fb2-148">Der URI der Datenschutzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="58fb2-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="58fb2-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="58fb2-149">-Publisher</span></span>
<span data-ttu-id="58fb2-150">Der Name des Herausgebers der Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="58fb2-150">The name of the gallery Image Definition publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="58fb2-151">-PurchasePlanName</span></span>
<span data-ttu-id="58fb2-152">Die ID für den Kaufplan.</span><span class="sxs-lookup"><span data-stu-id="58fb2-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="58fb2-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="58fb2-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="58fb2-154">Die Produkt-ID für den Kaufplan.</span><span class="sxs-lookup"><span data-stu-id="58fb2-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="58fb2-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="58fb2-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="58fb2-156">Die Herausgeber-ID für den Kaufplan.</span><span class="sxs-lookup"><span data-stu-id="58fb2-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="58fb2-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="58fb2-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="58fb2-158">Der URI mit den Versionsnotizen.</span><span class="sxs-lookup"><span data-stu-id="58fb2-158">The release note uri.</span></span>

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

### <span data-ttu-id="58fb2-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58fb2-159">-ResourceGroupName</span></span>
<span data-ttu-id="58fb2-160">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="58fb2-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="58fb2-161">-Sku</span></span>
<span data-ttu-id="58fb2-162">Der Name der Bilddefinitions-SKU des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="58fb2-162">The name of the gallery Image Definition SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="58fb2-163">-Tag</span></span>
<span data-ttu-id="58fb2-164">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="58fb2-164">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58fb2-165">-Confirm</span></span>
<span data-ttu-id="58fb2-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58fb2-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-167">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="58fb2-167">-WhatIf</span></span>
<span data-ttu-id="58fb2-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58fb2-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58fb2-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58fb2-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fb2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58fb2-170">CommonParameters</span></span>
<span data-ttu-id="58fb2-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58fb2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58fb2-172">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58fb2-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58fb2-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58fb2-173">INPUTS</span></span>

### <span data-ttu-id="58fb2-174">System.String</span><span class="sxs-lookup"><span data-stu-id="58fb2-174">System.String</span></span>

### <span data-ttu-id="58fb2-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="58fb2-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="58fb2-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="58fb2-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="58fb2-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="58fb2-177">System.DateTime</span></span>

### <span data-ttu-id="58fb2-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="58fb2-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="58fb2-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="58fb2-179">System.Int32</span></span>

### <span data-ttu-id="58fb2-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="58fb2-180">System.String[]</span></span>

## <span data-ttu-id="58fb2-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58fb2-181">OUTPUTS</span></span>

### <span data-ttu-id="58fb2-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="58fb2-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="58fb2-183">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58fb2-183">NOTES</span></span>

## <span data-ttu-id="58fb2-184">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58fb2-184">RELATED LINKS</span></span>
