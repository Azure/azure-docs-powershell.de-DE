---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297623"
---
# <span data-ttu-id="4a8fb-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4a8fb-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="4a8fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a8fb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8fb-103">Aktualisieren einer Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="4a8fb-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="4a8fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a8fb-104">SYNTAX</span></span>

### <span data-ttu-id="4a8fb-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a8fb-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a8fb-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4a8fb-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a8fb-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4a8fb-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a8fb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a8fb-108">DESCRIPTION</span></span>
<span data-ttu-id="4a8fb-109">Aktualisieren einer Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="4a8fb-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="4a8fb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a8fb-110">EXAMPLES</span></span>

### <span data-ttu-id="4a8fb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a8fb-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="4a8fb-112">Aktualisieren einer Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="4a8fb-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="4a8fb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a8fb-113">PARAMETERS</span></span>

### <span data-ttu-id="4a8fb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a8fb-114">-AsJob</span></span>
<span data-ttu-id="4a8fb-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4a8fb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a8fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8fb-116">-DefaultProfile</span></span>
<span data-ttu-id="4a8fb-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a8fb-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a8fb-118">-Description</span></span>
<span data-ttu-id="4a8fb-119">Die Beschreibung der Bilddefinitionsressource des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="4a8fb-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="4a8fb-120">-DisallowedDiskType</span></span>
<span data-ttu-id="4a8fb-121">Die unzulässigen Datenträgertypen.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="4a8fb-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="4a8fb-122">-EndOfLifeDate</span></span>
<span data-ttu-id="4a8fb-123">Das Datum des Lebenszyklusendes der Katalogbilddefinition</span><span class="sxs-lookup"><span data-stu-id="4a8fb-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="4a8fb-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="4a8fb-124">-Eula</span></span>
<span data-ttu-id="4a8fb-125">Die Vereinbarung "Eula" für die Bilddefinition der Galerie.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="4a8fb-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="4a8fb-126">-GalleryName</span></span>
<span data-ttu-id="4a8fb-127">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="4a8fb-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a8fb-128">-InputObject</span></span>
<span data-ttu-id="4a8fb-129">Das Bilddefinitionsobjekt aus dem PS Gallery-Katalog.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="4a8fb-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="4a8fb-130">-MaximumMemory</span></span>
<span data-ttu-id="4a8fb-131">Das Maximum des empfohlenen Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="4a8fb-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="4a8fb-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="4a8fb-132">-MaximumVCPU</span></span>
<span data-ttu-id="4a8fb-133">Das Maximum des empfohlenen</span><span class="sxs-lookup"><span data-stu-id="4a8fb-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="4a8fb-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="4a8fb-134">-MinimumMemory</span></span>
<span data-ttu-id="4a8fb-135">Das Minimum des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="4a8fb-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="4a8fb-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="4a8fb-136">-MinimumVCPU</span></span>
<span data-ttu-id="4a8fb-137">Das Minimum des empfohlenen</span><span class="sxs-lookup"><span data-stu-id="4a8fb-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="4a8fb-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4a8fb-138">-Name</span></span>
<span data-ttu-id="4a8fb-139">Der Name der Katalogbilddefinition.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="4a8fb-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="4a8fb-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="4a8fb-141">Der URI der Datenschutzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="4a8fb-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="4a8fb-142">-PurchasePlanName</span></span>
<span data-ttu-id="4a8fb-143">Die ID für den Kaufplan.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4a8fb-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="4a8fb-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="4a8fb-145">Die Produkt-ID für den Kaufplan.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4a8fb-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4a8fb-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="4a8fb-147">Die Herausgeber-ID für den Kaufplan.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4a8fb-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="4a8fb-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="4a8fb-149">Der URI mit den Versionsnotizen.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-149">The release note uri.</span></span>

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

### <span data-ttu-id="4a8fb-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a8fb-150">-ResourceGroupName</span></span>
<span data-ttu-id="4a8fb-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a8fb-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a8fb-152">-ResourceId</span></span>
<span data-ttu-id="4a8fb-153">Die Ressourcen-ID für die Bilddefinition</span><span class="sxs-lookup"><span data-stu-id="4a8fb-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="4a8fb-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a8fb-154">-Tag</span></span>
<span data-ttu-id="4a8fb-155">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="4a8fb-155">Resource tags</span></span>

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

### <span data-ttu-id="4a8fb-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a8fb-156">-Confirm</span></span>
<span data-ttu-id="4a8fb-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a8fb-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4a8fb-158">-WhatIf</span></span>
<span data-ttu-id="4a8fb-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a8fb-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a8fb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8fb-161">CommonParameters</span></span>
<span data-ttu-id="4a8fb-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a8fb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8fb-163">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a8fb-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8fb-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a8fb-164">INPUTS</span></span>

### <span data-ttu-id="4a8fb-165">System.String</span><span class="sxs-lookup"><span data-stu-id="4a8fb-165">System.String</span></span>

### <span data-ttu-id="4a8fb-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="4a8fb-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="4a8fb-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="4a8fb-167">System.DateTime</span></span>

### <span data-ttu-id="4a8fb-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a8fb-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4a8fb-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4a8fb-169">System.Int32</span></span>

### <span data-ttu-id="4a8fb-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4a8fb-170">System.String[]</span></span>

## <span data-ttu-id="4a8fb-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a8fb-171">OUTPUTS</span></span>

### <span data-ttu-id="4a8fb-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="4a8fb-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="4a8fb-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4a8fb-173">NOTES</span></span>

## <span data-ttu-id="4a8fb-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4a8fb-174">RELATED LINKS</span></span>
