---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: a37073de6a7960ae1ab90746372179db8e9d9386
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166348"
---
# <span data-ttu-id="6df6f-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="6df6f-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="6df6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6df6f-102">SYNOPSIS</span></span>
<span data-ttu-id="6df6f-103">Löschen Sie das ACR-Manifest.</span><span class="sxs-lookup"><span data-stu-id="6df6f-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="6df6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6df6f-104">SYNTAX</span></span>

### <span data-ttu-id="6df6f-105">ByManifestParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6df6f-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6df6f-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="6df6f-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6df6f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6df6f-107">DESCRIPTION</span></span>
<span data-ttu-id="6df6f-108">Löschen Sie das ACR-Manifest.</span><span class="sxs-lookup"><span data-stu-id="6df6f-108">Delete ACR manifest.</span></span>
<span data-ttu-id="6df6f-109">Um dieses Cmdlet zu verwenden, führen Sie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="6df6f-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="6df6f-110">aus.</span><span class="sxs-lookup"><span data-stu-id="6df6f-110">first.</span></span>

## <span data-ttu-id="6df6f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6df6f-111">EXAMPLES</span></span>

### <span data-ttu-id="6df6f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6df6f-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="6df6f-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span><span class="sxs-lookup"><span data-stu-id="6df6f-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="6df6f-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6df6f-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="6df6f-115">Delete manifest with tag latest for repository test/busybox27 under registry</span><span class="sxs-lookup"><span data-stu-id="6df6f-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="6df6f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6df6f-116">PARAMETERS</span></span>

### <span data-ttu-id="6df6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df6f-117">-DefaultProfile</span></span>
<span data-ttu-id="6df6f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6df6f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6df6f-119">-Manifest</span><span class="sxs-lookup"><span data-stu-id="6df6f-119">-Manifest</span></span>
<span data-ttu-id="6df6f-120">Manifestverweis.</span><span class="sxs-lookup"><span data-stu-id="6df6f-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df6f-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6df6f-121">-RegistryName</span></span>
<span data-ttu-id="6df6f-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="6df6f-122">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df6f-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="6df6f-123">-RepositoryName</span></span>
<span data-ttu-id="6df6f-124">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="6df6f-124">Repository Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df6f-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="6df6f-125">-Tag</span></span>
<span data-ttu-id="6df6f-126">Tag.</span><span class="sxs-lookup"><span data-stu-id="6df6f-126">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df6f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6df6f-127">-Confirm</span></span>
<span data-ttu-id="6df6f-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6df6f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6df6f-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6df6f-129">-WhatIf</span></span>
<span data-ttu-id="6df6f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6df6f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6df6f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6df6f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6df6f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df6f-132">CommonParameters</span></span>
<span data-ttu-id="6df6f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df6f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df6f-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6df6f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df6f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6df6f-135">INPUTS</span></span>

### <span data-ttu-id="6df6f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6df6f-136">System.String</span></span>

## <span data-ttu-id="6df6f-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6df6f-137">OUTPUTS</span></span>

### <span data-ttu-id="6df6f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6df6f-138">System.Boolean</span></span>

## <span data-ttu-id="6df6f-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6df6f-139">NOTES</span></span>

## <span data-ttu-id="6df6f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6df6f-140">RELATED LINKS</span></span>
