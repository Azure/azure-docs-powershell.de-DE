---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzImage.md
ms.openlocfilehash: 3798fccf0d3869d17fd0f79283aac93d0869a0e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651858"
---
# <span data-ttu-id="2d5d9-101">Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2d5d9-101">Update-AzImage</span></span>

## <span data-ttu-id="2d5d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="2d5d9-103">Aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-103">Updates an image.</span></span>

## <span data-ttu-id="2d5d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d5d9-104">SYNTAX</span></span>

### <span data-ttu-id="2d5d9-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d5d9-105">DefaultParameter (Default)</span></span>
```
Update-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d5d9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2d5d9-106">ResourceIdParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d5d9-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2d5d9-107">ObjectParameter</span></span>
```
Update-AzImage [-Tag <Hashtable>] [-AsJob] [-Image] <PSImage> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d5d9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d5d9-108">DESCRIPTION</span></span>
<span data-ttu-id="2d5d9-109">Das Cmdlet **Update-AzImage** aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-109">The **Update-AzImage** cmdlet updates an image.</span></span>
<span data-ttu-id="2d5d9-110">Derzeit können nur die Tags aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-110">Currently, only the Tags can be updated.</span></span>

## <span data-ttu-id="2d5d9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d5d9-111">EXAMPLES</span></span>

### <span data-ttu-id="2d5d9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d5d9-112">Example 1</span></span>
```
PS C:\> $image = Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' 
PS C:\> $image.Tags = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\> $image.Tags.Add("key1", "val1")
PS C:\> Update-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Image $image
```

<span data-ttu-id="2d5d9-113">Mit diesem Befehl wird der Tag-Wert des vorhandenen Bilds ' Image01 ' in der Ressourcengruppe ' ResourceGroup01 ' aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-113">This command updates the Tag value of the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2d5d9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d5d9-114">PARAMETERS</span></span>

### <span data-ttu-id="2d5d9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d5d9-115">-AsJob</span></span>
<span data-ttu-id="2d5d9-116">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2d5d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d5d9-117">-DefaultProfile</span></span>
<span data-ttu-id="2d5d9-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d5d9-119">-Bild</span><span class="sxs-lookup"><span data-stu-id="2d5d9-119">-Image</span></span>
<span data-ttu-id="2d5d9-120">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-120">Specifies a local image object.</span></span>

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

### <span data-ttu-id="2d5d9-121">-Bildname</span><span class="sxs-lookup"><span data-stu-id="2d5d9-121">-ImageName</span></span>
<span data-ttu-id="2d5d9-122">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-122">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="2d5d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d5d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d5d9-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2d5d9-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2d5d9-125">-ResourceId</span></span>
<span data-ttu-id="2d5d9-126">Die Ressourcen-ID für das Bild</span><span class="sxs-lookup"><span data-stu-id="2d5d9-126">The resource Id for the image</span></span>

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

### <span data-ttu-id="2d5d9-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d5d9-127">-Tag</span></span>
<span data-ttu-id="2d5d9-128">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="2d5d9-128">Resource tags</span></span>

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

### <span data-ttu-id="2d5d9-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d5d9-129">-Confirm</span></span>
<span data-ttu-id="2d5d9-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d5d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d5d9-131">-WhatIf</span></span>
<span data-ttu-id="2d5d9-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d5d9-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d5d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d5d9-134">CommonParameters</span></span>
<span data-ttu-id="2d5d9-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d5d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d5d9-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d5d9-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d5d9-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d5d9-137">INPUTS</span></span>

### <span data-ttu-id="2d5d9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2d5d9-138">System.String</span></span>

### <span data-ttu-id="2d5d9-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="2d5d9-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="2d5d9-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d5d9-140">OUTPUTS</span></span>

### <span data-ttu-id="2d5d9-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="2d5d9-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="2d5d9-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d5d9-142">NOTES</span></span>

## <span data-ttu-id="2d5d9-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d5d9-143">RELATED LINKS</span></span>
