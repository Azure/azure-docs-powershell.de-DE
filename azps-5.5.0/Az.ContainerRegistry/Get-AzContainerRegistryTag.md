---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 88bf3648f416efa69576c6b09a0d59f0d0d0fa76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148708"
---
# <span data-ttu-id="93fef-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="93fef-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="93fef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93fef-102">SYNOPSIS</span></span>
<span data-ttu-id="93fef-103">"ACR-Tag", oder listen Sie es auf.</span><span class="sxs-lookup"><span data-stu-id="93fef-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="93fef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93fef-104">SYNTAX</span></span>

### <span data-ttu-id="93fef-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="93fef-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93fef-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="93fef-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93fef-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93fef-107">DESCRIPTION</span></span>
<span data-ttu-id="93fef-108">"ACR-Tag", oder listen Sie es auf.</span><span class="sxs-lookup"><span data-stu-id="93fef-108">Get or list ACR tag.</span></span>
<span data-ttu-id="93fef-109">Um dieses Cmdlet zu verwenden, führen Sie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="93fef-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="93fef-110">aus.</span><span class="sxs-lookup"><span data-stu-id="93fef-110">first.</span></span>

## <span data-ttu-id="93fef-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93fef-111">EXAMPLES</span></span>

### <span data-ttu-id="93fef-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93fef-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="93fef-113">Listentags für repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="93fef-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="93fef-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="93fef-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="93fef-115">Holen Sie sich das neueste Tag für repository alpine unter registrierung.</span><span class="sxs-lookup"><span data-stu-id="93fef-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="93fef-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93fef-116">PARAMETERS</span></span>

### <span data-ttu-id="93fef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fef-117">-DefaultProfile</span></span>
<span data-ttu-id="93fef-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93fef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93fef-119">-Name</span><span class="sxs-lookup"><span data-stu-id="93fef-119">-Name</span></span>
<span data-ttu-id="93fef-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="93fef-120">Tag.</span></span>

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

### <span data-ttu-id="93fef-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="93fef-121">-RegistryName</span></span>
<span data-ttu-id="93fef-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="93fef-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="93fef-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="93fef-123">-RepositoryName</span></span>
<span data-ttu-id="93fef-124">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="93fef-124">Repository Name.</span></span>

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

### <span data-ttu-id="93fef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fef-125">CommonParameters</span></span>
<span data-ttu-id="93fef-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93fef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fef-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93fef-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fef-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93fef-128">INPUTS</span></span>

### <span data-ttu-id="93fef-129">System.String</span><span class="sxs-lookup"><span data-stu-id="93fef-129">System.String</span></span>

## <span data-ttu-id="93fef-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93fef-130">OUTPUTS</span></span>

### <span data-ttu-id="93fef-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="93fef-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="93fef-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="93fef-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="93fef-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="93fef-133">NOTES</span></span>

## <span data-ttu-id="93fef-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="93fef-134">RELATED LINKS</span></span>
