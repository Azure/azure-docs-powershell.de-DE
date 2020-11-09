---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300700"
---
# <span data-ttu-id="a09d0-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="a09d0-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="a09d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a09d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a09d0-103">Löschen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="a09d0-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="a09d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a09d0-104">SYNTAX</span></span>

### <span data-ttu-id="a09d0-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="a09d0-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a09d0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a09d0-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a09d0-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a09d0-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a09d0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a09d0-108">DESCRIPTION</span></span>
<span data-ttu-id="a09d0-109">Löschen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="a09d0-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="a09d0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a09d0-110">EXAMPLES</span></span>

### <span data-ttu-id="a09d0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a09d0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="a09d0-112">Entfernen Sie die Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="a09d0-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="a09d0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a09d0-113">PARAMETERS</span></span>

### <span data-ttu-id="a09d0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a09d0-114">-AsJob</span></span>
<span data-ttu-id="a09d0-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a09d0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a09d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09d0-116">-DefaultProfile</span></span>
<span data-ttu-id="a09d0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a09d0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a09d0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a09d0-118">-Force</span></span>
<span data-ttu-id="a09d0-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a09d0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a09d0-120">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="a09d0-120">-GalleryName</span></span>
<span data-ttu-id="a09d0-121">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="a09d0-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="a09d0-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a09d0-122">-InputObject</span></span>
<span data-ttu-id="a09d0-123">Das Bild Definitionsobjekt der PS-Galerie</span><span class="sxs-lookup"><span data-stu-id="a09d0-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="a09d0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a09d0-124">-Name</span></span>
<span data-ttu-id="a09d0-125">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="a09d0-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="a09d0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09d0-126">-ResourceGroupName</span></span>
<span data-ttu-id="a09d0-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a09d0-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a09d0-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a09d0-128">-ResourceId</span></span>
<span data-ttu-id="a09d0-129">Die Ressourcen-ID für die Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="a09d0-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="a09d0-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a09d0-130">-Confirm</span></span>
<span data-ttu-id="a09d0-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a09d0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a09d0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a09d0-132">-WhatIf</span></span>
<span data-ttu-id="a09d0-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a09d0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a09d0-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a09d0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a09d0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09d0-135">CommonParameters</span></span>
<span data-ttu-id="a09d0-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a09d0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09d0-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a09d0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09d0-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a09d0-138">INPUTS</span></span>

### <span data-ttu-id="a09d0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a09d0-139">System.String</span></span>

### <span data-ttu-id="a09d0-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="a09d0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="a09d0-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a09d0-141">OUTPUTS</span></span>

### <span data-ttu-id="a09d0-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a09d0-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a09d0-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a09d0-143">NOTES</span></span>

## <span data-ttu-id="a09d0-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a09d0-144">RELATED LINKS</span></span>
