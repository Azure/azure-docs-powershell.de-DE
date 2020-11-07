---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847648"
---
# <span data-ttu-id="764c9-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="764c9-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="764c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="764c9-102">SYNOPSIS</span></span>
<span data-ttu-id="764c9-103">Löschen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="764c9-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="764c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="764c9-104">SYNTAX</span></span>

### <span data-ttu-id="764c9-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="764c9-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="764c9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="764c9-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="764c9-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="764c9-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="764c9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="764c9-108">DESCRIPTION</span></span>
<span data-ttu-id="764c9-109">Löschen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="764c9-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="764c9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="764c9-110">EXAMPLES</span></span>

### <span data-ttu-id="764c9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="764c9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="764c9-112">Entfernen Sie die Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="764c9-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="764c9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="764c9-113">PARAMETERS</span></span>

### <span data-ttu-id="764c9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="764c9-114">-AsJob</span></span>
<span data-ttu-id="764c9-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="764c9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="764c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="764c9-116">-DefaultProfile</span></span>
<span data-ttu-id="764c9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="764c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="764c9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="764c9-118">-Force</span></span>
<span data-ttu-id="764c9-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="764c9-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="764c9-120">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="764c9-120">-GalleryName</span></span>
<span data-ttu-id="764c9-121">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="764c9-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="764c9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="764c9-122">-InputObject</span></span>
<span data-ttu-id="764c9-123">Das Bild Definitionsobjekt der PS-Galerie</span><span class="sxs-lookup"><span data-stu-id="764c9-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="764c9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="764c9-124">-Name</span></span>
<span data-ttu-id="764c9-125">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="764c9-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="764c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="764c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="764c9-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="764c9-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="764c9-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="764c9-128">-ResourceId</span></span>
<span data-ttu-id="764c9-129">Die Ressourcen-ID für die Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="764c9-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="764c9-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="764c9-130">-Confirm</span></span>
<span data-ttu-id="764c9-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="764c9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="764c9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="764c9-132">-WhatIf</span></span>
<span data-ttu-id="764c9-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="764c9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="764c9-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="764c9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="764c9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764c9-135">CommonParameters</span></span>
<span data-ttu-id="764c9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="764c9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764c9-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="764c9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764c9-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="764c9-138">INPUTS</span></span>

### <span data-ttu-id="764c9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="764c9-139">System.String</span></span>

### <span data-ttu-id="764c9-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="764c9-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="764c9-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="764c9-141">OUTPUTS</span></span>

### <span data-ttu-id="764c9-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="764c9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="764c9-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="764c9-143">NOTES</span></span>

## <span data-ttu-id="764c9-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="764c9-144">RELATED LINKS</span></span>
