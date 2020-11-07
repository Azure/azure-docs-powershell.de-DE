---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: 7959f11931b815a8e096cf9b5223064aa3554757
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820679"
---
# <span data-ttu-id="907d3-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="907d3-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="907d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="907d3-102">SYNOPSIS</span></span>
<span data-ttu-id="907d3-103">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="907d3-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="907d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="907d3-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>]
 [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>]
 [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="907d3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="907d3-105">DESCRIPTION</span></span>
<span data-ttu-id="907d3-106">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="907d3-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="907d3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="907d3-107">EXAMPLES</span></span>

### <span data-ttu-id="907d3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="907d3-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="907d3-109">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="907d3-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="907d3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="907d3-110">PARAMETERS</span></span>

### <span data-ttu-id="907d3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="907d3-111">-AsJob</span></span>
<span data-ttu-id="907d3-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="907d3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="907d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907d3-113">-DefaultProfile</span></span>
<span data-ttu-id="907d3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="907d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="907d3-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="907d3-115">-Description</span></span>
<span data-ttu-id="907d3-116">Die Beschreibung der Galerie-Bild Definitions Ressource.</span><span class="sxs-lookup"><span data-stu-id="907d3-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="907d3-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="907d3-117">-DisallowedDiskType</span></span>
<span data-ttu-id="907d3-118">Die nicht zulässigen Datenträgertypen</span><span class="sxs-lookup"><span data-stu-id="907d3-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="907d3-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="907d3-119">-EndOfLifeDate</span></span>
<span data-ttu-id="907d3-120">Das Ende des Lebenszyklus der Galeriebild Definition</span><span class="sxs-lookup"><span data-stu-id="907d3-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="907d3-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="907d3-121">-Eula</span></span>
<span data-ttu-id="907d3-122">Die EULA-Vereinbarung für die Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="907d3-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="907d3-123">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="907d3-123">-GalleryName</span></span>
<span data-ttu-id="907d3-124">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="907d3-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="907d3-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="907d3-125">-Location</span></span>
<span data-ttu-id="907d3-126">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="907d3-126">Resource location</span></span>

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

### <span data-ttu-id="907d3-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="907d3-127">-MaximumMemory</span></span>
<span data-ttu-id="907d3-128">Das Maximum des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="907d3-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="907d3-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="907d3-129">-MaximumVCPU</span></span>
<span data-ttu-id="907d3-130">Das Maximum des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="907d3-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="907d3-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="907d3-131">-MinimumMemory</span></span>
<span data-ttu-id="907d3-132">Das Mindeste des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="907d3-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="907d3-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="907d3-133">-MinimumVCPU</span></span>
<span data-ttu-id="907d3-134">Das Mindeste des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="907d3-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="907d3-135">-Name</span><span class="sxs-lookup"><span data-stu-id="907d3-135">-Name</span></span>
<span data-ttu-id="907d3-136">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="907d3-136">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="907d3-137">-Angebot</span><span class="sxs-lookup"><span data-stu-id="907d3-137">-Offer</span></span>
<span data-ttu-id="907d3-138">Der Name des Angebots zur Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="907d3-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="907d3-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="907d3-139">-OsState</span></span>
<span data-ttu-id="907d3-140">Status des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="907d3-140">The state of OS</span></span>

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

### <span data-ttu-id="907d3-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="907d3-141">-OsType</span></span>
<span data-ttu-id="907d3-142">Der Typ des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="907d3-142">The type of OS</span></span>

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

### <span data-ttu-id="907d3-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="907d3-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="907d3-144">Der URI für Datenschutzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="907d3-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="907d3-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="907d3-145">-Publisher</span></span>
<span data-ttu-id="907d3-146">Der Name des Katalogs für Bild Definitions Bilder in Publisher.</span><span class="sxs-lookup"><span data-stu-id="907d3-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="907d3-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="907d3-147">-PurchasePlanName</span></span>
<span data-ttu-id="907d3-148">Die ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="907d3-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="907d3-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="907d3-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="907d3-150">Die Produkt-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="907d3-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="907d3-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="907d3-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="907d3-152">Die Herausgeber-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="907d3-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="907d3-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="907d3-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="907d3-154">Der Versionshinweis-URI.</span><span class="sxs-lookup"><span data-stu-id="907d3-154">The release note uri.</span></span>

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

### <span data-ttu-id="907d3-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907d3-155">-ResourceGroupName</span></span>
<span data-ttu-id="907d3-156">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="907d3-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="907d3-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="907d3-157">-Sku</span></span>
<span data-ttu-id="907d3-158">Der Name der Katalogbild Definitions-SKU.</span><span class="sxs-lookup"><span data-stu-id="907d3-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="907d3-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="907d3-159">-Tag</span></span>
<span data-ttu-id="907d3-160">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="907d3-160">Resource tags</span></span>

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

### <span data-ttu-id="907d3-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="907d3-161">-Confirm</span></span>
<span data-ttu-id="907d3-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="907d3-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="907d3-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="907d3-163">-WhatIf</span></span>
<span data-ttu-id="907d3-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="907d3-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="907d3-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="907d3-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="907d3-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907d3-166">CommonParameters</span></span>
<span data-ttu-id="907d3-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907d3-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907d3-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="907d3-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907d3-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="907d3-169">INPUTS</span></span>

### <span data-ttu-id="907d3-170">System. String</span><span class="sxs-lookup"><span data-stu-id="907d3-170">System.String</span></span>

### <span data-ttu-id="907d3-171">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="907d3-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="907d3-172">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="907d3-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="907d3-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="907d3-173">System.DateTime</span></span>

### <span data-ttu-id="907d3-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="907d3-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="907d3-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="907d3-175">System.Int32</span></span>

### <span data-ttu-id="907d3-176">System. String []</span><span class="sxs-lookup"><span data-stu-id="907d3-176">System.String[]</span></span>

## <span data-ttu-id="907d3-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="907d3-177">OUTPUTS</span></span>

### <span data-ttu-id="907d3-178">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="907d3-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="907d3-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="907d3-179">NOTES</span></span>

## <span data-ttu-id="907d3-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="907d3-180">RELATED LINKS</span></span>
