---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: adbfd3515763427118fb7876fadd247d4240fd97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820635"
---
# <span data-ttu-id="3c525-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3c525-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="3c525-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c525-102">SYNOPSIS</span></span>
<span data-ttu-id="3c525-103">Löschen einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3c525-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="3c525-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c525-104">SYNTAX</span></span>

### <span data-ttu-id="3c525-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c525-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c525-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3c525-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c525-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3c525-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c525-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c525-108">DESCRIPTION</span></span>
<span data-ttu-id="3c525-109">Löschen einer Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3c525-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="3c525-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c525-110">EXAMPLES</span></span>

### <span data-ttu-id="3c525-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c525-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="3c525-112">Löschen Sie die angegebene Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3c525-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="3c525-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c525-113">PARAMETERS</span></span>

### <span data-ttu-id="3c525-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c525-114">-AsJob</span></span>
<span data-ttu-id="3c525-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3c525-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c525-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c525-116">-DefaultProfile</span></span>
<span data-ttu-id="3c525-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c525-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c525-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3c525-118">-Force</span></span>
<span data-ttu-id="3c525-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3c525-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c525-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3c525-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="3c525-121">Der Name der Katalogbild Definition.</span><span class="sxs-lookup"><span data-stu-id="3c525-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="3c525-122">-Galeriename</span><span class="sxs-lookup"><span data-stu-id="3c525-122">-GalleryName</span></span>
<span data-ttu-id="3c525-123">Der Name des Katalogs.</span><span class="sxs-lookup"><span data-stu-id="3c525-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="3c525-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3c525-124">-InputObject</span></span>
<span data-ttu-id="3c525-125">Das Version-Objekt des PS Gallery-Bilds</span><span class="sxs-lookup"><span data-stu-id="3c525-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="3c525-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3c525-126">-Name</span></span>
<span data-ttu-id="3c525-127">Der Name der Galeriebild Version.</span><span class="sxs-lookup"><span data-stu-id="3c525-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="3c525-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c525-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c525-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3c525-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3c525-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3c525-130">-ResourceId</span></span>
<span data-ttu-id="3c525-131">Die Ressourcen-ID für die Version des Galeriebilds</span><span class="sxs-lookup"><span data-stu-id="3c525-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="3c525-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c525-132">-Confirm</span></span>
<span data-ttu-id="3c525-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c525-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c525-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c525-134">-WhatIf</span></span>
<span data-ttu-id="3c525-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c525-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c525-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c525-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c525-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c525-137">CommonParameters</span></span>
<span data-ttu-id="3c525-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c525-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c525-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c525-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c525-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c525-140">INPUTS</span></span>

### <span data-ttu-id="3c525-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3c525-141">System.String</span></span>

### <span data-ttu-id="3c525-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3c525-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="3c525-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c525-143">OUTPUTS</span></span>

### <span data-ttu-id="3c525-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3c525-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3c525-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c525-145">NOTES</span></span>

## <span data-ttu-id="3c525-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c525-146">RELATED LINKS</span></span>
