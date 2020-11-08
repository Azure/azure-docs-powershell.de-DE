---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009324"
---
# <span data-ttu-id="f8fc3-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f8fc3-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="f8fc3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fc3-103">Löschen einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="f8fc3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8fc3-104">SYNTAX</span></span>

### <span data-ttu-id="f8fc3-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8fc3-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8fc3-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f8fc3-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8fc3-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f8fc3-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8fc3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8fc3-108">DESCRIPTION</span></span>
<span data-ttu-id="f8fc3-109">Löschen einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="f8fc3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8fc3-110">EXAMPLES</span></span>

### <span data-ttu-id="f8fc3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8fc3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="f8fc3-112">Löschen Sie die angegebene Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="f8fc3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8fc3-113">PARAMETERS</span></span>

### <span data-ttu-id="f8fc3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8fc3-114">-AsJob</span></span>
<span data-ttu-id="f8fc3-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f8fc3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8fc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fc3-116">-DefaultProfile</span></span>
<span data-ttu-id="f8fc3-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8fc3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f8fc3-118">-Force</span></span>
<span data-ttu-id="f8fc3-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f8fc3-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f8fc3-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="f8fc3-121">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="f8fc3-122">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="f8fc3-122">-GalleryName</span></span>
<span data-ttu-id="f8fc3-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="f8fc3-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8fc3-124">-InputObject</span></span>
<span data-ttu-id="f8fc3-125">Das Version-Objekt des PS Gallery-Bilds</span><span class="sxs-lookup"><span data-stu-id="f8fc3-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="f8fc3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f8fc3-126">-Name</span></span>
<span data-ttu-id="f8fc3-127">Der Name der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="f8fc3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fc3-128">-ResourceGroupName</span></span>
<span data-ttu-id="f8fc3-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="f8fc3-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f8fc3-130">-ResourceId</span></span>
<span data-ttu-id="f8fc3-131">Die Ressourcen-ID für die Version des Galeriebilds</span><span class="sxs-lookup"><span data-stu-id="f8fc3-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="f8fc3-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8fc3-132">-Confirm</span></span>
<span data-ttu-id="f8fc3-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8fc3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8fc3-134">-WhatIf</span></span>
<span data-ttu-id="f8fc3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8fc3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8fc3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fc3-137">CommonParameters</span></span>
<span data-ttu-id="f8fc3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8fc3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fc3-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8fc3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fc3-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8fc3-140">INPUTS</span></span>

### <span data-ttu-id="f8fc3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f8fc3-141">System.String</span></span>

### <span data-ttu-id="f8fc3-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f8fc3-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="f8fc3-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8fc3-143">OUTPUTS</span></span>

### <span data-ttu-id="f8fc3-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f8fc3-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f8fc3-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8fc3-145">NOTES</span></span>

## <span data-ttu-id="f8fc3-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8fc3-146">RELATED LINKS</span></span>
