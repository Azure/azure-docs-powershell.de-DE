---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: b829321dc3d091549ff0b8a89a5ad564867db478
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297599"
---
# <span data-ttu-id="1b90c-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="1b90c-101">Update-AzImage</span></span>

## <span data-ttu-id="1b90c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b90c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b90c-103">Aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="1b90c-103">Updates an image.</span></span>

## <span data-ttu-id="1b90c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b90c-104">SYNTAX</span></span>

### <span data-ttu-id="1b90c-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b90c-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b90c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1b90c-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b90c-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1b90c-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b90c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b90c-108">DESCRIPTION</span></span>
<span data-ttu-id="1b90c-109">Das **Cmdlet "Update-AzImage"** aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="1b90c-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="1b90c-110">Derzeit können nur die Tags aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1b90c-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="1b90c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b90c-111">EXAMPLES</span></span>

### <span data-ttu-id="1b90c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b90c-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="1b90c-113">Mit diesem Befehl wird der Tagwert des vorhandenen Bilds "Image01" in der Ressourcengruppe "ResourceGroup01" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1b90c-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1b90c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b90c-114">PARAMETERS</span></span>

### <span data-ttu-id="1b90c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b90c-115">-AsJob</span></span>
<span data-ttu-id="1b90c-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="1b90c-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1b90c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b90c-117">-DefaultProfile</span></span>
<span data-ttu-id="1b90c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b90c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b90c-119">-Image</span><span class="sxs-lookup"><span data-stu-id="1b90c-119">-Image</span></span>
<span data-ttu-id="1b90c-120">Gibt ein lokales Bildobjekt an.</span><span class="sxs-lookup"><span data-stu-id="1b90c-120">Specifies a local image object.</span></span>

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

### <span data-ttu-id="1b90c-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="1b90c-121">-ImageName</span></span>
<span data-ttu-id="1b90c-122">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="1b90c-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="1b90c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b90c-123">-ResourceGroupName</span></span>
<span data-ttu-id="1b90c-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1b90c-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1b90c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b90c-125">-ResourceId</span></span>
<span data-ttu-id="1b90c-126">Die Ressourcen-ID für das Bild</span><span class="sxs-lookup"><span data-stu-id="1b90c-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="1b90c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="1b90c-127">-Tag</span></span>
<span data-ttu-id="1b90c-128">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="1b90c-128">Resource tags</span></span>

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

### <span data-ttu-id="1b90c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b90c-129">-Confirm</span></span>
<span data-ttu-id="1b90c-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b90c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b90c-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1b90c-131">-WhatIf</span></span>
<span data-ttu-id="1b90c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b90c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b90c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b90c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b90c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b90c-134">CommonParameters</span></span>
<span data-ttu-id="1b90c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b90c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b90c-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b90c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b90c-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b90c-137">INPUTS</span></span>

### <span data-ttu-id="1b90c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1b90c-138">System.String</span></span>

### <span data-ttu-id="1b90c-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="1b90c-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="1b90c-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b90c-140">OUTPUTS</span></span>

### <span data-ttu-id="1b90c-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="1b90c-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="1b90c-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1b90c-142">NOTES</span></span>

## <span data-ttu-id="1b90c-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1b90c-143">RELATED LINKS</span></span>
