---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 2fa58235c0ba18042fde13ce9f8d3fb396940d07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164148"
---
# <span data-ttu-id="192a7-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="192a7-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="192a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="192a7-102">SYNOPSIS</span></span>
<span data-ttu-id="192a7-103">Erstellen oder Auflisten des ACR-Manifests.</span><span class="sxs-lookup"><span data-stu-id="192a7-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="192a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="192a7-104">SYNTAX</span></span>

### <span data-ttu-id="192a7-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="192a7-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="192a7-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="192a7-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="192a7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="192a7-107">DESCRIPTION</span></span>
<span data-ttu-id="192a7-108">Erstellen oder Auflisten des ACR-Manifests.</span><span class="sxs-lookup"><span data-stu-id="192a7-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="192a7-109">Um dieses Cmdlet zu verwenden, führen Sie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="192a7-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="192a7-110">aus.</span><span class="sxs-lookup"><span data-stu-id="192a7-110">first.</span></span>

## <span data-ttu-id="192a7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="192a7-111">EXAMPLES</span></span>

### <span data-ttu-id="192a7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="192a7-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="192a7-113">Listenmanifeste für repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="192a7-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="192a7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="192a7-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="192a7-115">Manifeste sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 für Repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="192a7-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="192a7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="192a7-116">PARAMETERS</span></span>

### <span data-ttu-id="192a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192a7-117">-DefaultProfile</span></span>
<span data-ttu-id="192a7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="192a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="192a7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="192a7-119">-Name</span></span>
<span data-ttu-id="192a7-120">Manifestverweis.</span><span class="sxs-lookup"><span data-stu-id="192a7-120">Manifest reference.</span></span>

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

### <span data-ttu-id="192a7-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="192a7-121">-RegistryName</span></span>
<span data-ttu-id="192a7-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="192a7-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="192a7-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="192a7-123">-RepositoryName</span></span>
<span data-ttu-id="192a7-124">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="192a7-124">Repository Name.</span></span>

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

### <span data-ttu-id="192a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192a7-125">CommonParameters</span></span>
<span data-ttu-id="192a7-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="192a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192a7-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="192a7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192a7-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="192a7-128">INPUTS</span></span>

### <span data-ttu-id="192a7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="192a7-129">System.String</span></span>

## <span data-ttu-id="192a7-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="192a7-130">OUTPUTS</span></span>

### <span data-ttu-id="192a7-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="192a7-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="192a7-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span><span class="sxs-lookup"><span data-stu-id="192a7-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="192a7-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="192a7-133">NOTES</span></span>

## <span data-ttu-id="192a7-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="192a7-134">RELATED LINKS</span></span>
