---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 37308ab02db132e03cf4f44536bc44d0d6845a86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938224"
---
# <span data-ttu-id="d9ce7-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="d9ce7-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="d9ce7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ce7-103">ACR-Tag erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="d9ce7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9ce7-104">SYNTAX</span></span>

### <span data-ttu-id="d9ce7-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9ce7-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9ce7-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9ce7-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9ce7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9ce7-107">DESCRIPTION</span></span>
<span data-ttu-id="d9ce7-108">ACR-Tag erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-108">Get or list ACR tag.</span></span>
<span data-ttu-id="d9ce7-109">Um dieses Cmdlet zu verwenden, führen Sie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="d9ce7-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="d9ce7-110">zuerst.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-110">first.</span></span>

## <span data-ttu-id="d9ce7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9ce7-111">EXAMPLES</span></span>

### <span data-ttu-id="d9ce7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9ce7-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="d9ce7-113">Listentags für repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="d9ce7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d9ce7-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="d9ce7-115">Holen Sie sich tag latest für repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="d9ce7-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d9ce7-116">PARAMETERS</span></span>

### <span data-ttu-id="d9ce7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ce7-117">-DefaultProfile</span></span>
<span data-ttu-id="d9ce7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9ce7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d9ce7-119">-Name</span></span>
<span data-ttu-id="d9ce7-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-120">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ce7-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d9ce7-121">-RegistryName</span></span>
<span data-ttu-id="d9ce7-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="d9ce7-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="d9ce7-123">-RepositoryName</span></span>
<span data-ttu-id="d9ce7-124">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-124">Repository Name.</span></span>

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

### <span data-ttu-id="d9ce7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ce7-125">CommonParameters</span></span>
<span data-ttu-id="d9ce7-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ce7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ce7-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9ce7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ce7-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9ce7-128">INPUTS</span></span>

### <span data-ttu-id="d9ce7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d9ce7-129">System.String</span></span>

## <span data-ttu-id="d9ce7-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9ce7-130">OUTPUTS</span></span>

### <span data-ttu-id="d9ce7-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="d9ce7-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="d9ce7-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="d9ce7-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="d9ce7-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d9ce7-133">NOTES</span></span>

## <span data-ttu-id="d9ce7-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d9ce7-134">RELATED LINKS</span></span>
