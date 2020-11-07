---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 445029c41e27cce14bff2ac14d826adf28f3c9ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662187"
---
# <span data-ttu-id="4d280-101">Update-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4d280-101">Update-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="4d280-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d280-102">SYNOPSIS</span></span>
<span data-ttu-id="4d280-103">Aktualisieren einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="4d280-103">Update a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d280-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d280-104">SYNTAX</span></span>

### <span data-ttu-id="4d280-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d280-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d280-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4d280-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d280-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4d280-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d280-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d280-108">DESCRIPTION</span></span>
<span data-ttu-id="4d280-109">Aktualisieren einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="4d280-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="4d280-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d280-110">EXAMPLES</span></span>

### <span data-ttu-id="4d280-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d280-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="4d280-112">Aktualisieren einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="4d280-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="4d280-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d280-113">PARAMETERS</span></span>

### <span data-ttu-id="4d280-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d280-114">-AsJob</span></span>
<span data-ttu-id="4d280-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4d280-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d280-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d280-116">-DefaultProfile</span></span>
<span data-ttu-id="4d280-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d280-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d280-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d280-118">-Description</span></span>
<span data-ttu-id="4d280-119">Die Beschreibung der Galerie-Bild Definitions Ressource.</span><span class="sxs-lookup"><span data-stu-id="4d280-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="4d280-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="4d280-120">-DisallowedDiskType</span></span>
<span data-ttu-id="4d280-121">Die nicht zulässigen Datenträgertypen</span><span class="sxs-lookup"><span data-stu-id="4d280-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="4d280-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="4d280-122">-EndOfLifeDate</span></span>
<span data-ttu-id="4d280-123">Das Ende des Lebenszyklus der Galeriebild Definition</span><span class="sxs-lookup"><span data-stu-id="4d280-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="4d280-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="4d280-124">-Eula</span></span>
<span data-ttu-id="4d280-125">Die EULA-Vereinbarung für die Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="4d280-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="4d280-126">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="4d280-126">-GalleryName</span></span>
<span data-ttu-id="4d280-127">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="4d280-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="4d280-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4d280-128">-InputObject</span></span>
<span data-ttu-id="4d280-129">Das Bild Definitionsobjekt der PS-Galerie</span><span class="sxs-lookup"><span data-stu-id="4d280-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="4d280-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="4d280-130">-MaximumMemory</span></span>
<span data-ttu-id="4d280-131">Das Maximum des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="4d280-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="4d280-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="4d280-132">-MaximumVCPU</span></span>
<span data-ttu-id="4d280-133">Das Maximum des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="4d280-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="4d280-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="4d280-134">-MinimumMemory</span></span>
<span data-ttu-id="4d280-135">Das Mindeste des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="4d280-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="4d280-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="4d280-136">-MinimumVCPU</span></span>
<span data-ttu-id="4d280-137">Das Mindeste des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="4d280-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="4d280-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4d280-138">-Name</span></span>
<span data-ttu-id="4d280-139">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="4d280-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="4d280-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="4d280-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="4d280-141">Der URI für Datenschutzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="4d280-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="4d280-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="4d280-142">-PurchasePlanName</span></span>
<span data-ttu-id="4d280-143">Die ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="4d280-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4d280-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="4d280-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="4d280-145">Die Produkt-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="4d280-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4d280-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="4d280-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="4d280-147">Die Herausgeber-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="4d280-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="4d280-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="4d280-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="4d280-149">Der Versionshinweis-URI.</span><span class="sxs-lookup"><span data-stu-id="4d280-149">The release note uri.</span></span>

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

### <span data-ttu-id="4d280-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d280-150">-ResourceGroupName</span></span>
<span data-ttu-id="4d280-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d280-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d280-152">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4d280-152">-ResourceId</span></span>
<span data-ttu-id="4d280-153">Die Ressourcen-ID für die Bild Definition</span><span class="sxs-lookup"><span data-stu-id="4d280-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="4d280-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d280-154">-Tag</span></span>
<span data-ttu-id="4d280-155">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="4d280-155">Resource tags</span></span>

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

### <span data-ttu-id="4d280-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d280-156">-Confirm</span></span>
<span data-ttu-id="4d280-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d280-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d280-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d280-158">-WhatIf</span></span>
<span data-ttu-id="4d280-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d280-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d280-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d280-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d280-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d280-161">CommonParameters</span></span>
<span data-ttu-id="4d280-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d280-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d280-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d280-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d280-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d280-164">INPUTS</span></span>

### <span data-ttu-id="4d280-165">System. String</span><span class="sxs-lookup"><span data-stu-id="4d280-165">System.String</span></span>

### <span data-ttu-id="4d280-166">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="4d280-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="4d280-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="4d280-167">System.DateTime</span></span>

### <span data-ttu-id="4d280-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4d280-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4d280-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4d280-169">System.Int32</span></span>

### <span data-ttu-id="4d280-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="4d280-170">System.String[]</span></span>

## <span data-ttu-id="4d280-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d280-171">OUTPUTS</span></span>

### <span data-ttu-id="4d280-172">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="4d280-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="4d280-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d280-173">NOTES</span></span>

## <span data-ttu-id="4d280-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d280-174">RELATED LINKS</span></span>
