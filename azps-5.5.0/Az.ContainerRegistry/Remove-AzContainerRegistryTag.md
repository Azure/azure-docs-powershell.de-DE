---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 7e6528630c731b15f906d79de45bc50f94b2a715
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166329"
---
# <span data-ttu-id="59289-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="59289-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="59289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59289-102">SYNOPSIS</span></span>
<span data-ttu-id="59289-103">Markierung eines #A0 wieder auf.</span><span class="sxs-lookup"><span data-stu-id="59289-103">Untag ACR tag.</span></span>

## <span data-ttu-id="59289-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59289-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59289-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59289-105">DESCRIPTION</span></span>
<span data-ttu-id="59289-106">Markierung eines #A0 wieder auf.</span><span class="sxs-lookup"><span data-stu-id="59289-106">Untag ACR tag.</span></span>
<span data-ttu-id="59289-107">Um dieses Cmdlet zu verwenden, führen Sie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="59289-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="59289-108">aus.</span><span class="sxs-lookup"><span data-stu-id="59289-108">first.</span></span>

## <span data-ttu-id="59289-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59289-109">EXAMPLES</span></span>

### <span data-ttu-id="59289-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59289-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="59289-111">Markierung "alpine:tag" in der Registrierung entfernen.</span><span class="sxs-lookup"><span data-stu-id="59289-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="59289-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59289-112">PARAMETERS</span></span>

### <span data-ttu-id="59289-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59289-113">-DefaultProfile</span></span>
<span data-ttu-id="59289-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59289-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59289-115">-Name</span><span class="sxs-lookup"><span data-stu-id="59289-115">-Name</span></span>
<span data-ttu-id="59289-116">Tag.</span><span class="sxs-lookup"><span data-stu-id="59289-116">Tag.</span></span>

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

### <span data-ttu-id="59289-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="59289-117">-RegistryName</span></span>
<span data-ttu-id="59289-118">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="59289-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="59289-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="59289-119">-RepositoryName</span></span>
<span data-ttu-id="59289-120">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="59289-120">Repository Name.</span></span>

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

### <span data-ttu-id="59289-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59289-121">-Confirm</span></span>
<span data-ttu-id="59289-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59289-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59289-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="59289-123">-WhatIf</span></span>
<span data-ttu-id="59289-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59289-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59289-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59289-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59289-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59289-126">CommonParameters</span></span>
<span data-ttu-id="59289-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59289-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59289-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59289-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59289-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59289-129">INPUTS</span></span>

### <span data-ttu-id="59289-130">System.String</span><span class="sxs-lookup"><span data-stu-id="59289-130">System.String</span></span>

## <span data-ttu-id="59289-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59289-131">OUTPUTS</span></span>

### <span data-ttu-id="59289-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="59289-132">System.Boolean</span></span>

## <span data-ttu-id="59289-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59289-133">NOTES</span></span>

## <span data-ttu-id="59289-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59289-134">RELATED LINKS</span></span>
