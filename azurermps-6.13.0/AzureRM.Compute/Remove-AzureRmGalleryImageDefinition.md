---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: e6e62fbe52aeb87868c688343ebbaed8f0046891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496325"
---
# <span data-ttu-id="d3823-101">Remove-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="d3823-101">Remove-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="d3823-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3823-102">SYNOPSIS</span></span>
<span data-ttu-id="d3823-103">Löschen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="d3823-103">Delete a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3823-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3823-104">SYNTAX</span></span>

### <span data-ttu-id="d3823-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3823-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3823-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d3823-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3823-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d3823-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3823-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3823-108">DESCRIPTION</span></span>
<span data-ttu-id="d3823-109">Löschen einer Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="d3823-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="d3823-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3823-110">EXAMPLES</span></span>

### <span data-ttu-id="d3823-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3823-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="d3823-112">Entfernen Sie die Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="d3823-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="d3823-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3823-113">PARAMETERS</span></span>

### <span data-ttu-id="d3823-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3823-114">-AsJob</span></span>
<span data-ttu-id="d3823-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d3823-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3823-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3823-116">-DefaultProfile</span></span>
<span data-ttu-id="d3823-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3823-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3823-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d3823-118">-Force</span></span>
<span data-ttu-id="d3823-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d3823-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d3823-120">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="d3823-120">-GalleryName</span></span>
<span data-ttu-id="d3823-121">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="d3823-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="d3823-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d3823-122">-InputObject</span></span>
<span data-ttu-id="d3823-123">Das Bild Definitionsobjekt der PS-Galerie</span><span class="sxs-lookup"><span data-stu-id="d3823-123">The PS Gallery Image Definition Object</span></span>

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

### <span data-ttu-id="d3823-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d3823-124">-Name</span></span>
<span data-ttu-id="d3823-125">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="d3823-125">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="d3823-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3823-126">-ResourceGroupName</span></span>
<span data-ttu-id="d3823-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d3823-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3823-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d3823-128">-ResourceId</span></span>
<span data-ttu-id="d3823-129">Die Ressourcen-ID für die Katalogbild Definition</span><span class="sxs-lookup"><span data-stu-id="d3823-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="d3823-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3823-130">-Confirm</span></span>
<span data-ttu-id="d3823-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3823-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3823-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3823-132">-WhatIf</span></span>
<span data-ttu-id="d3823-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3823-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3823-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3823-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3823-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3823-135">CommonParameters</span></span>
<span data-ttu-id="d3823-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3823-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3823-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3823-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3823-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3823-138">INPUTS</span></span>

### <span data-ttu-id="d3823-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d3823-139">System.String</span></span>

### <span data-ttu-id="d3823-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="d3823-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="d3823-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3823-141">OUTPUTS</span></span>

### <span data-ttu-id="d3823-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d3823-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d3823-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3823-143">NOTES</span></span>

## <span data-ttu-id="d3823-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3823-144">RELATED LINKS</span></span>
