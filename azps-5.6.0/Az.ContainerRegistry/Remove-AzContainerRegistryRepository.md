---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: 1c0ad2ae46987a526be4e8fda110dada914bd27e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930339"
---
# <span data-ttu-id="3e6d8-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="3e6d8-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="3e6d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6d8-103">Löschen Sie das Repository aus ACR.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="3e6d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e6d8-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e6d8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e6d8-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6d8-106">Löschen Sie das Repository aus ACR.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="3e6d8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e6d8-107">EXAMPLES</span></span>

### <span data-ttu-id="3e6d8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e6d8-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="3e6d8-109">Löschen Sie repository test/busybox15 unter registrierung.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="3e6d8-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3e6d8-110">PARAMETERS</span></span>

### <span data-ttu-id="3e6d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6d8-111">-DefaultProfile</span></span>
<span data-ttu-id="3e6d8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e6d8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3e6d8-113">-Name</span></span>
<span data-ttu-id="3e6d8-114">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-114">Repository Name.</span></span>

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

### <span data-ttu-id="3e6d8-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3e6d8-115">-RegistryName</span></span>
<span data-ttu-id="3e6d8-116">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="3e6d8-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3e6d8-117">-Confirm</span></span>
<span data-ttu-id="3e6d8-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e6d8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e6d8-119">-WhatIf</span></span>
<span data-ttu-id="3e6d8-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e6d8-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e6d8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6d8-122">CommonParameters</span></span>
<span data-ttu-id="3e6d8-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6d8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6d8-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e6d8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6d8-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e6d8-125">INPUTS</span></span>

### <span data-ttu-id="3e6d8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="3e6d8-126">System.String</span></span>

## <span data-ttu-id="3e6d8-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e6d8-127">OUTPUTS</span></span>

### <span data-ttu-id="3e6d8-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="3e6d8-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="3e6d8-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3e6d8-129">NOTES</span></span>

## <span data-ttu-id="3e6d8-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3e6d8-130">RELATED LINKS</span></span>
