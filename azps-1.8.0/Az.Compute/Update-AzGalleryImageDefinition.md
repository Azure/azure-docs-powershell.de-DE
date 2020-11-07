---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 338e65e4795f3b676a1f88e8a8281a41aee5a0c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820488"
---
# <span data-ttu-id="25a73-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="25a73-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="25a73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25a73-102">SYNOPSIS</span></span>
<span data-ttu-id="25a73-103">Aktualisieren einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="25a73-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="25a73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25a73-104">SYNTAX</span></span>

### <span data-ttu-id="25a73-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="25a73-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25a73-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="25a73-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25a73-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="25a73-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25a73-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25a73-108">DESCRIPTION</span></span>
<span data-ttu-id="25a73-109">Aktualisieren einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="25a73-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="25a73-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25a73-110">EXAMPLES</span></span>

### <span data-ttu-id="25a73-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25a73-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="25a73-112">Aktualisieren einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="25a73-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="25a73-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="25a73-113">PARAMETERS</span></span>

### <span data-ttu-id="25a73-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25a73-114">-AsJob</span></span>
<span data-ttu-id="25a73-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="25a73-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25a73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a73-116">-DefaultProfile</span></span>
<span data-ttu-id="25a73-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25a73-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25a73-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25a73-118">-Description</span></span>
<span data-ttu-id="25a73-119">Die Beschreibung der Galerie-Bild Definitions Ressource.</span><span class="sxs-lookup"><span data-stu-id="25a73-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="25a73-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="25a73-120">-DisallowedDiskType</span></span>
<span data-ttu-id="25a73-121">Die nicht zulässigen Datenträgertypen</span><span class="sxs-lookup"><span data-stu-id="25a73-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="25a73-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="25a73-122">-EndOfLifeDate</span></span>
<span data-ttu-id="25a73-123">Das Ende des Lebenszyklus der Galeriebild Definition</span><span class="sxs-lookup"><span data-stu-id="25a73-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="25a73-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="25a73-124">-Eula</span></span>
<span data-ttu-id="25a73-125">Die EULA-Vereinbarung für die Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="25a73-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="25a73-126">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="25a73-126">-GalleryName</span></span>
<span data-ttu-id="25a73-127">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="25a73-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="25a73-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25a73-128">-InputObject</span></span>
<span data-ttu-id="25a73-129">Das Bild Definitionsobjekt der PS-Galerie</span><span class="sxs-lookup"><span data-stu-id="25a73-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="25a73-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="25a73-130">-MaximumMemory</span></span>
<span data-ttu-id="25a73-131">Das Maximum des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="25a73-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="25a73-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="25a73-132">-MaximumVCPU</span></span>
<span data-ttu-id="25a73-133">Das Maximum des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="25a73-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="25a73-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="25a73-134">-MinimumMemory</span></span>
<span data-ttu-id="25a73-135">Das Mindeste des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="25a73-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="25a73-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="25a73-136">-MinimumVCPU</span></span>
<span data-ttu-id="25a73-137">Das Mindeste des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="25a73-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="25a73-138">-Name</span><span class="sxs-lookup"><span data-stu-id="25a73-138">-Name</span></span>
<span data-ttu-id="25a73-139">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="25a73-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="25a73-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="25a73-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="25a73-141">Der URI für Datenschutzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="25a73-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="25a73-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="25a73-142">-PurchasePlanName</span></span>
<span data-ttu-id="25a73-143">Die ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="25a73-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="25a73-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="25a73-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="25a73-145">Die Produkt-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="25a73-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="25a73-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="25a73-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="25a73-147">Die Herausgeber-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="25a73-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="25a73-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="25a73-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="25a73-149">Der Versionshinweis-URI.</span><span class="sxs-lookup"><span data-stu-id="25a73-149">The release note uri.</span></span>

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

### <span data-ttu-id="25a73-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a73-150">-ResourceGroupName</span></span>
<span data-ttu-id="25a73-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25a73-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="25a73-152">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="25a73-152">-ResourceId</span></span>
<span data-ttu-id="25a73-153">Die Ressourcen-ID für die Bild Definition</span><span class="sxs-lookup"><span data-stu-id="25a73-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="25a73-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="25a73-154">-Tag</span></span>
<span data-ttu-id="25a73-155">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="25a73-155">Resource tags</span></span>

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

### <span data-ttu-id="25a73-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25a73-156">-Confirm</span></span>
<span data-ttu-id="25a73-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25a73-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25a73-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25a73-158">-WhatIf</span></span>
<span data-ttu-id="25a73-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25a73-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25a73-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25a73-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25a73-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a73-161">CommonParameters</span></span>
<span data-ttu-id="25a73-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a73-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a73-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25a73-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a73-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25a73-164">INPUTS</span></span>

### <span data-ttu-id="25a73-165">System. String</span><span class="sxs-lookup"><span data-stu-id="25a73-165">System.String</span></span>

### <span data-ttu-id="25a73-166">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="25a73-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="25a73-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="25a73-167">System.DateTime</span></span>

### <span data-ttu-id="25a73-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="25a73-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="25a73-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="25a73-169">System.Int32</span></span>

### <span data-ttu-id="25a73-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="25a73-170">System.String[]</span></span>

## <span data-ttu-id="25a73-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25a73-171">OUTPUTS</span></span>

### <span data-ttu-id="25a73-172">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="25a73-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="25a73-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="25a73-173">NOTES</span></span>

## <span data-ttu-id="25a73-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25a73-174">RELATED LINKS</span></span>
