---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 09871f6d7876b5f197af515f531c85b8bf6a3d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928648"
---
# <span data-ttu-id="63dd8-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="63dd8-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="63dd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="63dd8-103">Aktualisieren einer Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="63dd8-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="63dd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63dd8-104">SYNTAX</span></span>

### <span data-ttu-id="63dd8-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="63dd8-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63dd8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="63dd8-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63dd8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="63dd8-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63dd8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63dd8-108">DESCRIPTION</span></span>
<span data-ttu-id="63dd8-109">Aktualisieren einer Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="63dd8-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="63dd8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="63dd8-110">EXAMPLES</span></span>

### <span data-ttu-id="63dd8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63dd8-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="63dd8-112">Aktualisieren einer Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="63dd8-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="63dd8-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="63dd8-113">PARAMETERS</span></span>

### <span data-ttu-id="63dd8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63dd8-114">-AsJob</span></span>
<span data-ttu-id="63dd8-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="63dd8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63dd8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63dd8-116">-DefaultProfile</span></span>
<span data-ttu-id="63dd8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63dd8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63dd8-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63dd8-118">-Description</span></span>
<span data-ttu-id="63dd8-119">Die Beschreibung der Ressourcen für die Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="63dd8-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="63dd8-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="63dd8-120">-DisallowedDiskType</span></span>
<span data-ttu-id="63dd8-121">Die nicht zulässigen Datenträgertypen.</span><span class="sxs-lookup"><span data-stu-id="63dd8-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="63dd8-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="63dd8-122">-EndOfLifeDate</span></span>
<span data-ttu-id="63dd8-123">Das Datum des Lebenszyklus des Katalogs Bilddefinition</span><span class="sxs-lookup"><span data-stu-id="63dd8-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="63dd8-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="63dd8-124">-Eula</span></span>
<span data-ttu-id="63dd8-125">Der Eula-Vertrag für die Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="63dd8-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="63dd8-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="63dd8-126">-GalleryName</span></span>
<span data-ttu-id="63dd8-127">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="63dd8-127">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63dd8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63dd8-128">-InputObject</span></span>
<span data-ttu-id="63dd8-129">Das Bilddefinitionsobjekt des PS-Katalogs.</span><span class="sxs-lookup"><span data-stu-id="63dd8-129">The PS Gallery Image Definition Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63dd8-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="63dd8-130">-MaximumMemory</span></span>
<span data-ttu-id="63dd8-131">Das Maximum des empfohlenen Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="63dd8-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="63dd8-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="63dd8-132">-MaximumVCPU</span></span>
<span data-ttu-id="63dd8-133">Das Maximum des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="63dd8-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="63dd8-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="63dd8-134">-MinimumMemory</span></span>
<span data-ttu-id="63dd8-135">Das Minimum des empfohlenen Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="63dd8-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="63dd8-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="63dd8-136">-MinimumVCPU</span></span>
<span data-ttu-id="63dd8-137">Das Minimum des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="63dd8-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="63dd8-138">-Name</span><span class="sxs-lookup"><span data-stu-id="63dd8-138">-Name</span></span>
<span data-ttu-id="63dd8-139">Der Name der Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="63dd8-139">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63dd8-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="63dd8-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="63dd8-141">Der URI der Datenschutzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="63dd8-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="63dd8-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="63dd8-142">-PurchasePlanName</span></span>
<span data-ttu-id="63dd8-143">Die ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="63dd8-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="63dd8-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="63dd8-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="63dd8-145">Die Produkt-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="63dd8-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="63dd8-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="63dd8-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="63dd8-147">Die Herausgeber-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="63dd8-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="63dd8-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="63dd8-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="63dd8-149">Der URI für versionsnotizen.</span><span class="sxs-lookup"><span data-stu-id="63dd8-149">The release note uri.</span></span>

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

### <span data-ttu-id="63dd8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63dd8-150">-ResourceGroupName</span></span>
<span data-ttu-id="63dd8-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="63dd8-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63dd8-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63dd8-152">-ResourceId</span></span>
<span data-ttu-id="63dd8-153">Die Ressourcen-ID für die Bilddefinition</span><span class="sxs-lookup"><span data-stu-id="63dd8-153">The resource ID for the image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63dd8-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="63dd8-154">-Tag</span></span>
<span data-ttu-id="63dd8-155">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="63dd8-155">Resource tags</span></span>

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

### <span data-ttu-id="63dd8-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63dd8-156">-Confirm</span></span>
<span data-ttu-id="63dd8-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63dd8-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63dd8-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63dd8-158">-WhatIf</span></span>
<span data-ttu-id="63dd8-159">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63dd8-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63dd8-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63dd8-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63dd8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63dd8-161">CommonParameters</span></span>
<span data-ttu-id="63dd8-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63dd8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63dd8-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63dd8-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63dd8-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="63dd8-164">INPUTS</span></span>

### <span data-ttu-id="63dd8-165">System.String</span><span class="sxs-lookup"><span data-stu-id="63dd8-165">System.String</span></span>

### <span data-ttu-id="63dd8-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="63dd8-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="63dd8-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="63dd8-167">System.DateTime</span></span>

### <span data-ttu-id="63dd8-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="63dd8-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="63dd8-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="63dd8-169">System.Int32</span></span>

### <span data-ttu-id="63dd8-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="63dd8-170">System.String[]</span></span>

## <span data-ttu-id="63dd8-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="63dd8-171">OUTPUTS</span></span>

### <span data-ttu-id="63dd8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="63dd8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="63dd8-173">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="63dd8-173">NOTES</span></span>

## <span data-ttu-id="63dd8-174">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="63dd8-174">RELATED LINKS</span></span>
