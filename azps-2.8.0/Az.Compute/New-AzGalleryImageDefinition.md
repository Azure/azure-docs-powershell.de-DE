---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: 7b2a0399be6412c3e33754a8e91b1a6120b5ec9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652084"
---
# <span data-ttu-id="b2c59-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="b2c59-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="b2c59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2c59-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c59-103">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="b2c59-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="b2c59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2c59-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>]
 [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>]
 [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c59-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2c59-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c59-106">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="b2c59-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="b2c59-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2c59-107">EXAMPLES</span></span>

### <span data-ttu-id="b2c59-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2c59-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="b2c59-109">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="b2c59-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="b2c59-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2c59-110">PARAMETERS</span></span>

### <span data-ttu-id="b2c59-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2c59-111">-AsJob</span></span>
<span data-ttu-id="b2c59-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b2c59-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2c59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c59-113">-DefaultProfile</span></span>
<span data-ttu-id="b2c59-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2c59-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2c59-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2c59-115">-Description</span></span>
<span data-ttu-id="b2c59-116">Die Beschreibung der Galerie-Bild Definitions Ressource.</span><span class="sxs-lookup"><span data-stu-id="b2c59-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="b2c59-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="b2c59-117">-DisallowedDiskType</span></span>
<span data-ttu-id="b2c59-118">Die nicht zulässigen Datenträgertypen</span><span class="sxs-lookup"><span data-stu-id="b2c59-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="b2c59-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="b2c59-119">-EndOfLifeDate</span></span>
<span data-ttu-id="b2c59-120">Das Ende des Lebenszyklus der Galeriebild Definition</span><span class="sxs-lookup"><span data-stu-id="b2c59-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="b2c59-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="b2c59-121">-Eula</span></span>
<span data-ttu-id="b2c59-122">Die EULA-Vereinbarung für die Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="b2c59-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="b2c59-123">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="b2c59-123">-GalleryName</span></span>
<span data-ttu-id="b2c59-124">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="b2c59-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="b2c59-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="b2c59-125">-Location</span></span>
<span data-ttu-id="b2c59-126">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="b2c59-126">Resource location</span></span>

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

### <span data-ttu-id="b2c59-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="b2c59-127">-MaximumMemory</span></span>
<span data-ttu-id="b2c59-128">Das Maximum des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="b2c59-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="b2c59-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="b2c59-129">-MaximumVCPU</span></span>
<span data-ttu-id="b2c59-130">Das Maximum des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="b2c59-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="b2c59-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="b2c59-131">-MinimumMemory</span></span>
<span data-ttu-id="b2c59-132">Das Mindeste des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="b2c59-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="b2c59-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="b2c59-133">-MinimumVCPU</span></span>
<span data-ttu-id="b2c59-134">Das Mindeste des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="b2c59-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="b2c59-135">-Name</span><span class="sxs-lookup"><span data-stu-id="b2c59-135">-Name</span></span>
<span data-ttu-id="b2c59-136">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="b2c59-136">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="b2c59-137">-Angebot</span><span class="sxs-lookup"><span data-stu-id="b2c59-137">-Offer</span></span>
<span data-ttu-id="b2c59-138">Der Name des Angebots zur Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="b2c59-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="b2c59-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="b2c59-139">-OsState</span></span>
<span data-ttu-id="b2c59-140">Status des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="b2c59-140">The state of OS</span></span>

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

### <span data-ttu-id="b2c59-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="b2c59-141">-OsType</span></span>
<span data-ttu-id="b2c59-142">Der Typ des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="b2c59-142">The type of OS</span></span>

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

### <span data-ttu-id="b2c59-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="b2c59-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="b2c59-144">Der URI für Datenschutzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="b2c59-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="b2c59-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b2c59-145">-Publisher</span></span>
<span data-ttu-id="b2c59-146">Der Name des Katalogs für Bild Definitions Bilder in Publisher.</span><span class="sxs-lookup"><span data-stu-id="b2c59-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="b2c59-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="b2c59-147">-PurchasePlanName</span></span>
<span data-ttu-id="b2c59-148">Die ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="b2c59-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="b2c59-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="b2c59-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="b2c59-150">Die Produkt-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="b2c59-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="b2c59-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b2c59-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="b2c59-152">Die Herausgeber-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="b2c59-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="b2c59-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="b2c59-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="b2c59-154">Der Versionshinweis-URI.</span><span class="sxs-lookup"><span data-stu-id="b2c59-154">The release note uri.</span></span>

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

### <span data-ttu-id="b2c59-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2c59-155">-ResourceGroupName</span></span>
<span data-ttu-id="b2c59-156">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b2c59-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2c59-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="b2c59-157">-Sku</span></span>
<span data-ttu-id="b2c59-158">Der Name der Katalogbild Definitions-SKU.</span><span class="sxs-lookup"><span data-stu-id="b2c59-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="b2c59-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2c59-159">-Tag</span></span>
<span data-ttu-id="b2c59-160">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="b2c59-160">Resource tags</span></span>

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

### <span data-ttu-id="b2c59-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2c59-161">-Confirm</span></span>
<span data-ttu-id="b2c59-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2c59-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c59-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c59-163">-WhatIf</span></span>
<span data-ttu-id="b2c59-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2c59-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2c59-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2c59-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c59-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c59-166">CommonParameters</span></span>
<span data-ttu-id="b2c59-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c59-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c59-168">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2c59-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c59-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2c59-169">INPUTS</span></span>

### <span data-ttu-id="b2c59-170">System. String</span><span class="sxs-lookup"><span data-stu-id="b2c59-170">System.String</span></span>

### <span data-ttu-id="b2c59-171">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="b2c59-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="b2c59-172">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="b2c59-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="b2c59-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="b2c59-173">System.DateTime</span></span>

### <span data-ttu-id="b2c59-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2c59-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b2c59-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b2c59-175">System.Int32</span></span>

### <span data-ttu-id="b2c59-176">System. String []</span><span class="sxs-lookup"><span data-stu-id="b2c59-176">System.String[]</span></span>

## <span data-ttu-id="b2c59-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2c59-177">OUTPUTS</span></span>

### <span data-ttu-id="b2c59-178">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="b2c59-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="b2c59-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2c59-179">NOTES</span></span>

## <span data-ttu-id="b2c59-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2c59-180">RELATED LINKS</span></span>
