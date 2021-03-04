---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: def99b11efa5070881cc3226b9ec85449b4cc0b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924195"
---
# <span data-ttu-id="1dd33-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="1dd33-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="1dd33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dd33-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd33-103">Löschen Sie das ACR-Manifest.</span><span class="sxs-lookup"><span data-stu-id="1dd33-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="1dd33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dd33-104">SYNTAX</span></span>

### <span data-ttu-id="1dd33-105">ByManifestParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1dd33-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd33-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dd33-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd33-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dd33-107">DESCRIPTION</span></span>
<span data-ttu-id="1dd33-108">Löschen Sie das ACR-Manifest.</span><span class="sxs-lookup"><span data-stu-id="1dd33-108">Delete ACR manifest.</span></span>
<span data-ttu-id="1dd33-109">Um dieses Cmdlet zu verwenden, führen Sie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="1dd33-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="1dd33-110">zuerst.</span><span class="sxs-lookup"><span data-stu-id="1dd33-110">first.</span></span>

## <span data-ttu-id="1dd33-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1dd33-111">EXAMPLES</span></span>

### <span data-ttu-id="1dd33-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1dd33-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="1dd33-113">Löschen des Manifests sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab für Repositorytest/busybox27 unter Registrierung</span><span class="sxs-lookup"><span data-stu-id="1dd33-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="1dd33-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1dd33-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="1dd33-115">Manifest löschen mit tag latest für repository test/busybox27 under registry</span><span class="sxs-lookup"><span data-stu-id="1dd33-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="1dd33-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1dd33-116">PARAMETERS</span></span>

### <span data-ttu-id="1dd33-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd33-117">-DefaultProfile</span></span>
<span data-ttu-id="1dd33-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dd33-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd33-119">-Manifest</span><span class="sxs-lookup"><span data-stu-id="1dd33-119">-Manifest</span></span>
<span data-ttu-id="1dd33-120">Manifestbezug.</span><span class="sxs-lookup"><span data-stu-id="1dd33-120">Manifest reference.</span></span>

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

### <span data-ttu-id="1dd33-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="1dd33-121">-RegistryName</span></span>
<span data-ttu-id="1dd33-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="1dd33-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="1dd33-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="1dd33-123">-RepositoryName</span></span>
<span data-ttu-id="1dd33-124">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="1dd33-124">Repository Name.</span></span>

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

### <span data-ttu-id="1dd33-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1dd33-125">-Tag</span></span>
<span data-ttu-id="1dd33-126">Tag.</span><span class="sxs-lookup"><span data-stu-id="1dd33-126">Tag.</span></span>

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

### <span data-ttu-id="1dd33-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1dd33-127">-Confirm</span></span>
<span data-ttu-id="1dd33-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1dd33-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd33-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd33-129">-WhatIf</span></span>
<span data-ttu-id="1dd33-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1dd33-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd33-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dd33-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd33-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd33-132">CommonParameters</span></span>
<span data-ttu-id="1dd33-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd33-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd33-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dd33-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd33-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1dd33-135">INPUTS</span></span>

### <span data-ttu-id="1dd33-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1dd33-136">System.String</span></span>

## <span data-ttu-id="1dd33-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1dd33-137">OUTPUTS</span></span>

### <span data-ttu-id="1dd33-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1dd33-138">System.Boolean</span></span>

## <span data-ttu-id="1dd33-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1dd33-139">NOTES</span></span>

## <span data-ttu-id="1dd33-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1dd33-140">RELATED LINKS</span></span>
