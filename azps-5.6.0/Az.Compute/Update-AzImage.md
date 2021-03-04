---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: edf0ce1b67c25b8f5e48282dba45e845820c7b93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928320"
---
# <span data-ttu-id="00546-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="00546-101">Update-AzImage</span></span>

## <span data-ttu-id="00546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00546-102">SYNOPSIS</span></span>
<span data-ttu-id="00546-103">Aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="00546-103">Updates an image.</span></span>

## <span data-ttu-id="00546-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00546-104">SYNTAX</span></span>

### <span data-ttu-id="00546-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="00546-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00546-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="00546-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00546-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="00546-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00546-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00546-108">DESCRIPTION</span></span>
<span data-ttu-id="00546-109">Das **Update-AzImage-Cmdlet** aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="00546-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="00546-110">Derzeit können nur die Kategorien aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="00546-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="00546-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00546-111">EXAMPLES</span></span>

### <span data-ttu-id="00546-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00546-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="00546-113">Mit diesem Befehl wird der Tag-Wert des vorhandenen Bilds "Image01" in der Ressourcengruppe "ResourceGroup01" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="00546-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="00546-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="00546-114">PARAMETERS</span></span>

### <span data-ttu-id="00546-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00546-115">-AsJob</span></span>
<span data-ttu-id="00546-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="00546-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="00546-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00546-117">-DefaultProfile</span></span>
<span data-ttu-id="00546-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00546-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00546-119">-Image</span><span class="sxs-lookup"><span data-stu-id="00546-119">-Image</span></span>
<span data-ttu-id="00546-120">Gibt ein lokales Bildobjekt an.</span><span class="sxs-lookup"><span data-stu-id="00546-120">Specifies a local image object.</span></span>

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

### <span data-ttu-id="00546-121">-ImageName</span><span class="sxs-lookup"><span data-stu-id="00546-121">-ImageName</span></span>
<span data-ttu-id="00546-122">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="00546-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="00546-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00546-123">-ResourceGroupName</span></span>
<span data-ttu-id="00546-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="00546-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="00546-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00546-125">-ResourceId</span></span>
<span data-ttu-id="00546-126">Die Ressourcen-ID für das Bild</span><span class="sxs-lookup"><span data-stu-id="00546-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="00546-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="00546-127">-Tag</span></span>
<span data-ttu-id="00546-128">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="00546-128">Resource tags</span></span>

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

### <span data-ttu-id="00546-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00546-129">-Confirm</span></span>
<span data-ttu-id="00546-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00546-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00546-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00546-131">-WhatIf</span></span>
<span data-ttu-id="00546-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00546-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00546-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00546-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00546-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00546-134">CommonParameters</span></span>
<span data-ttu-id="00546-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00546-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00546-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00546-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00546-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00546-137">INPUTS</span></span>

### <span data-ttu-id="00546-138">System.String</span><span class="sxs-lookup"><span data-stu-id="00546-138">System.String</span></span>

### <span data-ttu-id="00546-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="00546-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="00546-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00546-140">OUTPUTS</span></span>

### <span data-ttu-id="00546-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="00546-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="00546-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="00546-142">NOTES</span></span>

## <span data-ttu-id="00546-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="00546-143">RELATED LINKS</span></span>
