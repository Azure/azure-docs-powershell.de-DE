---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009330"
---
# <span data-ttu-id="589b9-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="589b9-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="589b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="589b9-102">SYNOPSIS</span></span>
<span data-ttu-id="589b9-103">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="589b9-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="589b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="589b9-104">SYNTAX</span></span>

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

## <span data-ttu-id="589b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="589b9-105">DESCRIPTION</span></span>
<span data-ttu-id="589b9-106">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="589b9-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="589b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="589b9-107">EXAMPLES</span></span>

### <span data-ttu-id="589b9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="589b9-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="589b9-109">Erstellen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="589b9-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="589b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="589b9-110">PARAMETERS</span></span>

### <span data-ttu-id="589b9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="589b9-111">-AsJob</span></span>
<span data-ttu-id="589b9-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="589b9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="589b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="589b9-113">-DefaultProfile</span></span>
<span data-ttu-id="589b9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="589b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="589b9-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="589b9-115">-Description</span></span>
<span data-ttu-id="589b9-116">Die Beschreibung der Galerie-Bild Definitions Ressource.</span><span class="sxs-lookup"><span data-stu-id="589b9-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="589b9-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="589b9-117">-DisallowedDiskType</span></span>
<span data-ttu-id="589b9-118">Die nicht zulässigen Datenträgertypen</span><span class="sxs-lookup"><span data-stu-id="589b9-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="589b9-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="589b9-119">-EndOfLifeDate</span></span>
<span data-ttu-id="589b9-120">Das Ende des Lebenszyklus der Galeriebild Definition</span><span class="sxs-lookup"><span data-stu-id="589b9-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="589b9-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="589b9-121">-Eula</span></span>
<span data-ttu-id="589b9-122">Die EULA-Vereinbarung für die Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="589b9-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="589b9-123">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="589b9-123">-GalleryName</span></span>
<span data-ttu-id="589b9-124">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="589b9-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="589b9-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="589b9-125">-HyperVGeneration</span></span>
<span data-ttu-id="589b9-126">Die Hypervisor-Generierung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="589b9-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="589b9-127">Nur auf Betriebssystemdatenträger anwendbar.</span><span class="sxs-lookup"><span data-stu-id="589b9-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="589b9-128">Zulässige Werte sind v1 und v2.</span><span class="sxs-lookup"><span data-stu-id="589b9-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="589b9-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="589b9-129">-Location</span></span>
<span data-ttu-id="589b9-130">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="589b9-130">Resource location</span></span>

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

### <span data-ttu-id="589b9-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="589b9-131">-MaximumMemory</span></span>
<span data-ttu-id="589b9-132">Das Maximum des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="589b9-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="589b9-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="589b9-133">-MaximumVCPU</span></span>
<span data-ttu-id="589b9-134">Das Maximum des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="589b9-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="589b9-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="589b9-135">-MinimumMemory</span></span>
<span data-ttu-id="589b9-136">Das Mindeste des empfohlenen Speichers</span><span class="sxs-lookup"><span data-stu-id="589b9-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="589b9-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="589b9-137">-MinimumVCPU</span></span>
<span data-ttu-id="589b9-138">Das Mindeste des empfohlenen CPU-Kerns</span><span class="sxs-lookup"><span data-stu-id="589b9-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="589b9-139">-Name</span><span class="sxs-lookup"><span data-stu-id="589b9-139">-Name</span></span>
<span data-ttu-id="589b9-140">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="589b9-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="589b9-141">-Angebot</span><span class="sxs-lookup"><span data-stu-id="589b9-141">-Offer</span></span>
<span data-ttu-id="589b9-142">Der Name des Angebots zur Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="589b9-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="589b9-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="589b9-143">-OsState</span></span>
<span data-ttu-id="589b9-144">Status des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="589b9-144">The state of OS</span></span>

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

### <span data-ttu-id="589b9-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="589b9-145">-OsType</span></span>
<span data-ttu-id="589b9-146">Der Typ des Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="589b9-146">The type of OS</span></span>

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

### <span data-ttu-id="589b9-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="589b9-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="589b9-148">Der URI für Datenschutzbestimmungen.</span><span class="sxs-lookup"><span data-stu-id="589b9-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="589b9-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="589b9-149">-Publisher</span></span>
<span data-ttu-id="589b9-150">Der Name des Katalogs für Bild Definitions Bilder in Publisher.</span><span class="sxs-lookup"><span data-stu-id="589b9-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="589b9-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="589b9-151">-PurchasePlanName</span></span>
<span data-ttu-id="589b9-152">Die ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="589b9-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="589b9-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="589b9-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="589b9-154">Die Produkt-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="589b9-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="589b9-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="589b9-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="589b9-156">Die Herausgeber-ID für den Einkaufsplan.</span><span class="sxs-lookup"><span data-stu-id="589b9-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="589b9-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="589b9-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="589b9-158">Der Versionshinweis-URI.</span><span class="sxs-lookup"><span data-stu-id="589b9-158">The release note uri.</span></span>

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

### <span data-ttu-id="589b9-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="589b9-159">-ResourceGroupName</span></span>
<span data-ttu-id="589b9-160">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="589b9-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="589b9-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="589b9-161">-Sku</span></span>
<span data-ttu-id="589b9-162">Der Name der Katalogbild Definitions-SKU.</span><span class="sxs-lookup"><span data-stu-id="589b9-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="589b9-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="589b9-163">-Tag</span></span>
<span data-ttu-id="589b9-164">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="589b9-164">Resource tags</span></span>

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

### <span data-ttu-id="589b9-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="589b9-165">-Confirm</span></span>
<span data-ttu-id="589b9-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="589b9-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="589b9-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="589b9-167">-WhatIf</span></span>
<span data-ttu-id="589b9-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="589b9-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="589b9-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="589b9-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="589b9-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589b9-170">CommonParameters</span></span>
<span data-ttu-id="589b9-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="589b9-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589b9-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="589b9-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589b9-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="589b9-173">INPUTS</span></span>

### <span data-ttu-id="589b9-174">System. String</span><span class="sxs-lookup"><span data-stu-id="589b9-174">System.String</span></span>

### <span data-ttu-id="589b9-175">Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="589b9-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="589b9-176">Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="589b9-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="589b9-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="589b9-177">System.DateTime</span></span>

### <span data-ttu-id="589b9-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="589b9-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="589b9-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="589b9-179">System.Int32</span></span>

### <span data-ttu-id="589b9-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="589b9-180">System.String[]</span></span>

## <span data-ttu-id="589b9-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="589b9-181">OUTPUTS</span></span>

### <span data-ttu-id="589b9-182">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="589b9-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="589b9-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="589b9-183">NOTES</span></span>

## <span data-ttu-id="589b9-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="589b9-184">RELATED LINKS</span></span>
