---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
ms.openlocfilehash: c2a65eeb742d4182dfad0cd32be1d78951977096
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480442"
---
# <span data-ttu-id="3a898-101">Remove-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3a898-101">Remove-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="3a898-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a898-102">SYNOPSIS</span></span>
<span data-ttu-id="3a898-103">Löschen einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3a898-103">Delete a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a898-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a898-104">SYNTAX</span></span>

### <span data-ttu-id="3a898-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a898-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a898-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3a898-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a898-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3a898-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a898-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a898-108">DESCRIPTION</span></span>
<span data-ttu-id="3a898-109">Löschen einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3a898-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="3a898-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a898-110">EXAMPLES</span></span>

### <span data-ttu-id="3a898-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a898-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="3a898-112">Löschen Sie die angegebene Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3a898-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="3a898-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a898-113">PARAMETERS</span></span>

### <span data-ttu-id="3a898-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a898-114">-AsJob</span></span>
<span data-ttu-id="3a898-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3a898-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a898-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a898-116">-DefaultProfile</span></span>
<span data-ttu-id="3a898-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a898-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a898-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3a898-118">-Force</span></span>
<span data-ttu-id="3a898-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3a898-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a898-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3a898-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="3a898-121">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="3a898-121">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a898-122">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="3a898-122">-GalleryName</span></span>
<span data-ttu-id="3a898-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="3a898-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="3a898-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3a898-124">-InputObject</span></span>
<span data-ttu-id="3a898-125">Das Version-Objekt des PS Gallery-Bilds</span><span class="sxs-lookup"><span data-stu-id="3a898-125">The PS Gallery Image Version Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a898-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3a898-126">-Name</span></span>
<span data-ttu-id="3a898-127">Der Name der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3a898-127">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a898-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a898-128">-ResourceGroupName</span></span>
<span data-ttu-id="3a898-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a898-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a898-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3a898-130">-ResourceId</span></span>
<span data-ttu-id="3a898-131">Die Ressourcen-ID für die Version des Galeriebilds</span><span class="sxs-lookup"><span data-stu-id="3a898-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="3a898-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a898-132">-Confirm</span></span>
<span data-ttu-id="3a898-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a898-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a898-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a898-134">-WhatIf</span></span>
<span data-ttu-id="3a898-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a898-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a898-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a898-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a898-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a898-137">CommonParameters</span></span>
<span data-ttu-id="3a898-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a898-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a898-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a898-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a898-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a898-140">INPUTS</span></span>

### <span data-ttu-id="3a898-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3a898-141">System.String</span></span>

### <span data-ttu-id="3a898-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3a898-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="3a898-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a898-143">OUTPUTS</span></span>

### <span data-ttu-id="3a898-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3a898-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3a898-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a898-145">NOTES</span></span>

## <span data-ttu-id="3a898-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a898-146">RELATED LINKS</span></span>
