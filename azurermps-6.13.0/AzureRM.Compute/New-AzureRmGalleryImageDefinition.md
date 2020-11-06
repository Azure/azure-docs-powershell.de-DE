---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 8dcfe4adedd7da375e888dade108125d7899d7d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504494"
---
# <span data-ttu-id="0fbdd-101">New-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="0fbdd-101">New-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="0fbdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fbdd-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbdd-103">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="0fbdd-103">Create a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fbdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fbdd-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Location] <String> -Publisher <String> -Offer <String> -Sku <String>
 -OsState <OperatingSystemStateTypes> -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fbdd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fbdd-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbdd-106">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="0fbdd-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="0fbdd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fbdd-107">EXAMPLES</span></span>

### <span data-ttu-id="0fbdd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fbdd-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="0fbdd-109">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="0fbdd-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="0fbdd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fbdd-110">PARAMETERS</span></span>

### <span data-ttu-id="0fbdd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fbdd-111">-AsJob</span></span>
<span data-ttu-id="0fbdd-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0fbdd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fbdd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbdd-113">-DefaultProfile</span></span>
<span data-ttu-id="0fbdd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fbdd-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fbdd-115">-Description</span></span>
<span data-ttu-id="0fbdd-116">Die Beschreibung der Galerie-Bild Definitions Ressource.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="0fbdd-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="0fbdd-117">-DisallowedDiskType</span></span>
<span data-ttu-id="0fbdd-118">Die nicht zulässigen Datenträgertypen</span><span class="sxs-lookup"><span data-stu-id="0fbdd-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="0fbdd-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="0fbdd-119">-EndOfLifeDate</span></span>
<span data-ttu-id="0fbdd-120">Das Ende des Lebenszyklus der Galeriebild Definition</span><span class="sxs-lookup"><span data-stu-id="0fbdd-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="0fbdd-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="0fbdd-121">-Eula</span></span>
<span data-ttu-id="0fbdd-122">Die EULA-Vereinbarung für die Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="0fbdd-123">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="0fbdd-123">-GalleryName</span></span>
<span data-ttu-id="0fbdd-124">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="0fbdd-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="0fbdd-125">-Location</span></span>
<span data-ttu-id="0fbdd-126">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="0fbdd-126">Resource location</span></span>

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

### <span data-ttu-id="0fbdd-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="0fbdd-127">-MaximumMemory</span></span>
<span data-ttu-id="0fbdd-128">Das Maximum des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="0fbdd-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="0fbdd-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="0fbdd-129">-MaximumVCPU</span></span>
<span data-ttu-id="0fbdd-130">Das Maximum des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="0fbdd-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="0fbdd-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="0fbdd-131">-MinimumMemory</span></span>
<span data-ttu-id="0fbdd-132">Das Mindeste des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="0fbdd-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="0fbdd-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="0fbdd-133">-MinimumVCPU</span></span>
<span data-ttu-id="0fbdd-134">Das Mindeste des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="0fbdd-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="0fbdd-135">-Name</span><span class="sxs-lookup"><span data-stu-id="0fbdd-135">-Name</span></span>
<span data-ttu-id="0fbdd-136">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-136">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="0fbdd-137">-Angebot</span><span class="sxs-lookup"><span data-stu-id="0fbdd-137">-Offer</span></span>
<span data-ttu-id="0fbdd-138">Der Name des Angebots zur Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="0fbdd-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="0fbdd-139">-OsState</span></span>
<span data-ttu-id="0fbdd-140">Status des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="0fbdd-140">The state of OS</span></span>

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

### <span data-ttu-id="0fbdd-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="0fbdd-141">-OsType</span></span>
<span data-ttu-id="0fbdd-142">Der Typ des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="0fbdd-142">The type of OS</span></span>

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

### <span data-ttu-id="0fbdd-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="0fbdd-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="0fbdd-144">Der URI für Datenschutzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="0fbdd-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0fbdd-145">-Publisher</span></span>
<span data-ttu-id="0fbdd-146">Der Name des Katalogs für Bild Definitions Bilder in Publisher.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="0fbdd-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="0fbdd-147">-PurchasePlanName</span></span>
<span data-ttu-id="0fbdd-148">Die ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="0fbdd-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="0fbdd-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="0fbdd-150">Die Produkt-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="0fbdd-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="0fbdd-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="0fbdd-152">Die Herausgeber-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="0fbdd-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="0fbdd-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="0fbdd-154">Der Versionshinweis-URI.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-154">The release note uri.</span></span>

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

### <span data-ttu-id="0fbdd-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbdd-155">-ResourceGroupName</span></span>
<span data-ttu-id="0fbdd-156">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="0fbdd-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="0fbdd-157">-Sku</span></span>
<span data-ttu-id="0fbdd-158">Der Name der Katalogbild Definitions-SKU.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="0fbdd-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="0fbdd-159">-Tag</span></span>
<span data-ttu-id="0fbdd-160">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="0fbdd-160">Resource tags</span></span>

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

### <span data-ttu-id="0fbdd-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0fbdd-161">-Confirm</span></span>
<span data-ttu-id="0fbdd-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fbdd-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fbdd-163">-WhatIf</span></span>
<span data-ttu-id="0fbdd-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fbdd-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fbdd-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbdd-166">CommonParameters</span></span>
<span data-ttu-id="0fbdd-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbdd-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fbdd-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbdd-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fbdd-169">INPUTS</span></span>

### <span data-ttu-id="0fbdd-170">System. String</span><span class="sxs-lookup"><span data-stu-id="0fbdd-170">System.String</span></span>

### <span data-ttu-id="0fbdd-171">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="0fbdd-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="0fbdd-172">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="0fbdd-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="0fbdd-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="0fbdd-173">System.DateTime</span></span>

### <span data-ttu-id="0fbdd-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0fbdd-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0fbdd-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0fbdd-175">System.Int32</span></span>

### <span data-ttu-id="0fbdd-176">System. String []</span><span class="sxs-lookup"><span data-stu-id="0fbdd-176">System.String[]</span></span>

## <span data-ttu-id="0fbdd-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fbdd-177">OUTPUTS</span></span>

### <span data-ttu-id="0fbdd-178">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="0fbdd-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="0fbdd-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fbdd-179">NOTES</span></span>

## <span data-ttu-id="0fbdd-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fbdd-180">RELATED LINKS</span></span>
