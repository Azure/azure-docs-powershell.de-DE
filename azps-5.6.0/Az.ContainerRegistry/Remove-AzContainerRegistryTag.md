---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 6fbc5b33bb8e9c865b5ea869deed5044ee08198f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920824"
---
# <span data-ttu-id="4131d-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="4131d-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="4131d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4131d-102">SYNOPSIS</span></span>
<span data-ttu-id="4131d-103">Enttag ACR-Tag.</span><span class="sxs-lookup"><span data-stu-id="4131d-103">Untag ACR tag.</span></span>

## <span data-ttu-id="4131d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4131d-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4131d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4131d-105">DESCRIPTION</span></span>
<span data-ttu-id="4131d-106">Enttag ACR-Tag.</span><span class="sxs-lookup"><span data-stu-id="4131d-106">Untag ACR tag.</span></span>
<span data-ttu-id="4131d-107">Um dieses Cmdlet zu verwenden, führen Sie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="4131d-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="4131d-108">zuerst.</span><span class="sxs-lookup"><span data-stu-id="4131d-108">first.</span></span>

## <span data-ttu-id="4131d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4131d-109">EXAMPLES</span></span>

### <span data-ttu-id="4131d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4131d-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="4131d-111">Enttag alpine:tag under registry.</span><span class="sxs-lookup"><span data-stu-id="4131d-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="4131d-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4131d-112">PARAMETERS</span></span>

### <span data-ttu-id="4131d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4131d-113">-DefaultProfile</span></span>
<span data-ttu-id="4131d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4131d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4131d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4131d-115">-Name</span></span>
<span data-ttu-id="4131d-116">Tag.</span><span class="sxs-lookup"><span data-stu-id="4131d-116">Tag.</span></span>

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

### <span data-ttu-id="4131d-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4131d-117">-RegistryName</span></span>
<span data-ttu-id="4131d-118">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="4131d-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="4131d-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="4131d-119">-RepositoryName</span></span>
<span data-ttu-id="4131d-120">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="4131d-120">Repository Name.</span></span>

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

### <span data-ttu-id="4131d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4131d-121">-Confirm</span></span>
<span data-ttu-id="4131d-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4131d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4131d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4131d-123">-WhatIf</span></span>
<span data-ttu-id="4131d-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4131d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4131d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4131d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4131d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4131d-126">CommonParameters</span></span>
<span data-ttu-id="4131d-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4131d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4131d-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4131d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4131d-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4131d-129">INPUTS</span></span>

### <span data-ttu-id="4131d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4131d-130">System.String</span></span>

## <span data-ttu-id="4131d-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4131d-131">OUTPUTS</span></span>

### <span data-ttu-id="4131d-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4131d-132">System.Boolean</span></span>

## <span data-ttu-id="4131d-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4131d-133">NOTES</span></span>

## <span data-ttu-id="4131d-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4131d-134">RELATED LINKS</span></span>
