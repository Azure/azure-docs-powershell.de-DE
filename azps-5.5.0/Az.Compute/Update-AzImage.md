---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144633"
---
# <span data-ttu-id="ace4f-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ace4f-101">Update-AzImage</span></span>

## <span data-ttu-id="ace4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ace4f-102">SYNOPSIS</span></span>
<span data-ttu-id="ace4f-103">Aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="ace4f-103">Updates an image.</span></span>

## <span data-ttu-id="ace4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ace4f-104">SYNTAX</span></span>

### <span data-ttu-id="ace4f-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="ace4f-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ace4f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ace4f-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ace4f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ace4f-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ace4f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ace4f-108">DESCRIPTION</span></span>
<span data-ttu-id="ace4f-109">Das **Cmdlet "Update-AzImage"** aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="ace4f-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="ace4f-110">Derzeit können nur die Tags aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ace4f-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="ace4f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ace4f-111">EXAMPLES</span></span>

### <span data-ttu-id="ace4f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ace4f-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="ace4f-113">Mit diesem Befehl wird der Tagwert des vorhandenen Bilds "Image01" in der Ressourcengruppe "ResourceGroup01" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ace4f-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ace4f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ace4f-114">PARAMETERS</span></span>

### <span data-ttu-id="ace4f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ace4f-115">-AsJob</span></span>
<span data-ttu-id="ace4f-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="ace4f-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ace4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace4f-117">-DefaultProfile</span></span>
<span data-ttu-id="ace4f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ace4f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ace4f-119">-Image</span><span class="sxs-lookup"><span data-stu-id="ace4f-119">-Image</span></span>
<span data-ttu-id="ace4f-120">Gibt ein lokales Bildobjekt an.</span><span class="sxs-lookup"><span data-stu-id="ace4f-120">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ace4f-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ace4f-121">-ImageName</span></span>
<span data-ttu-id="ace4f-122">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="ace4f-122">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace4f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace4f-123">-ResourceGroupName</span></span>
<span data-ttu-id="ace4f-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ace4f-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ace4f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ace4f-125">-ResourceId</span></span>
<span data-ttu-id="ace4f-126">Die Ressourcen-ID für das Bild</span><span class="sxs-lookup"><span data-stu-id="ace4f-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="ace4f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="ace4f-127">-Tag</span></span>
<span data-ttu-id="ace4f-128">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="ace4f-128">Resource tags</span></span>

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

### <span data-ttu-id="ace4f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ace4f-129">-Confirm</span></span>
<span data-ttu-id="ace4f-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ace4f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ace4f-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ace4f-131">-WhatIf</span></span>
<span data-ttu-id="ace4f-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ace4f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ace4f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ace4f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ace4f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace4f-134">CommonParameters</span></span>
<span data-ttu-id="ace4f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace4f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace4f-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ace4f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace4f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ace4f-137">INPUTS</span></span>

### <span data-ttu-id="ace4f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ace4f-138">System.String</span></span>

### <span data-ttu-id="ace4f-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="ace4f-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ace4f-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ace4f-140">OUTPUTS</span></span>

### <span data-ttu-id="ace4f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="ace4f-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ace4f-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ace4f-142">NOTES</span></span>

## <span data-ttu-id="ace4f-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ace4f-143">RELATED LINKS</span></span>
