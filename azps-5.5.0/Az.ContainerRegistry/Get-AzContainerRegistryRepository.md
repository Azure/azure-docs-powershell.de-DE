---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: 7da65515138ff6afa97e6c05f9baa764d6ab920c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164145"
---
# <span data-ttu-id="5ad8d-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="5ad8d-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="5ad8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ad8d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad8d-103">Erhalten oder auflisten Sie ACR-Repositorys.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="5ad8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ad8d-104">SYNTAX</span></span>

### <span data-ttu-id="5ad8d-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ad8d-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ad8d-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ad8d-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ad8d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ad8d-107">DESCRIPTION</span></span>
<span data-ttu-id="5ad8d-108">Erhalten oder auflisten Sie ACR-Repositorys.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="5ad8d-109">Die Liste gibt nur Repositorynamen zurück.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-109">List returns repository names only.</span></span>

## <span data-ttu-id="5ad8d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ad8d-110">EXAMPLES</span></span>

### <span data-ttu-id="5ad8d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5ad8d-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="5ad8d-112">Listet alle Repositorys in der Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-112">List all repositories in registry.</span></span>

### <span data-ttu-id="5ad8d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5ad8d-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="5ad8d-114">Listen Sie die ersten drei Repositorys in der Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="5ad8d-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5ad8d-115">Example 3</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -Name alpine

Registry             : registry.azurecr.io
ImageName            : alpine
CreatedTime          : 2020-10-13T05:45:25.5896115Z
LastUpdateTime       : 2021-01-04T08:31:46.2406505Z
ManifestCount        : 7
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="5ad8d-116">Holen Sie sich das Repository alpine unter registrierung.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="5ad8d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ad8d-117">PARAMETERS</span></span>

### <span data-ttu-id="5ad8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad8d-118">-DefaultProfile</span></span>
<span data-ttu-id="5ad8d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ad8d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5ad8d-120">-Name</span></span>
<span data-ttu-id="5ad8d-121">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-121">Repository Name.</span></span>

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

### <span data-ttu-id="5ad8d-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5ad8d-122">-RegistryName</span></span>
<span data-ttu-id="5ad8d-123">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="5ad8d-124">-First</span><span class="sxs-lookup"><span data-stu-id="5ad8d-124">-First</span></span>
<span data-ttu-id="5ad8d-125">Erste n Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-125">First n results.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad8d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad8d-126">CommonParameters</span></span>
<span data-ttu-id="5ad8d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ad8d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad8d-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ad8d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad8d-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ad8d-129">INPUTS</span></span>

### <span data-ttu-id="5ad8d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5ad8d-130">System.String</span></span>

## <span data-ttu-id="5ad8d-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ad8d-131">OUTPUTS</span></span>

### <span data-ttu-id="5ad8d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5ad8d-132">System.String</span></span>

### <span data-ttu-id="5ad8d-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="5ad8d-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="5ad8d-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5ad8d-134">NOTES</span></span>

## <span data-ttu-id="5ad8d-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5ad8d-135">RELATED LINKS</span></span>
