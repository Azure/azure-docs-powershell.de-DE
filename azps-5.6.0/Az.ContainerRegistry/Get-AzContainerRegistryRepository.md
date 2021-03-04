---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: efcd7fb518f66c99fab8b4cd456e8f8cea424ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938243"
---
# <span data-ttu-id="5759a-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="5759a-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="5759a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5759a-102">SYNOPSIS</span></span>
<span data-ttu-id="5759a-103">ACR-Repositorys erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="5759a-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="5759a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5759a-104">SYNTAX</span></span>

### <span data-ttu-id="5759a-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5759a-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5759a-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="5759a-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5759a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5759a-107">DESCRIPTION</span></span>
<span data-ttu-id="5759a-108">ACR-Repositorys erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="5759a-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="5759a-109">Liste gibt nur Repositorynamen zurück.</span><span class="sxs-lookup"><span data-stu-id="5759a-109">List returns repository names only.</span></span>

## <span data-ttu-id="5759a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5759a-110">EXAMPLES</span></span>

### <span data-ttu-id="5759a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5759a-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="5759a-112">Listen Sie alle Repositorys in der Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="5759a-112">List all repositories in registry.</span></span>

### <span data-ttu-id="5759a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5759a-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="5759a-114">Listen Sie die ersten drei Repositorys in der Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="5759a-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="5759a-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5759a-115">Example 3</span></span>
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

<span data-ttu-id="5759a-116">Holen Sie sich repository alpine unter registrierung.</span><span class="sxs-lookup"><span data-stu-id="5759a-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="5759a-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5759a-117">PARAMETERS</span></span>

### <span data-ttu-id="5759a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5759a-118">-DefaultProfile</span></span>
<span data-ttu-id="5759a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5759a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5759a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5759a-120">-Name</span></span>
<span data-ttu-id="5759a-121">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="5759a-121">Repository Name.</span></span>

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

### <span data-ttu-id="5759a-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5759a-122">-RegistryName</span></span>
<span data-ttu-id="5759a-123">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="5759a-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="5759a-124">-First</span><span class="sxs-lookup"><span data-stu-id="5759a-124">-First</span></span>
<span data-ttu-id="5759a-125">Erste n Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="5759a-125">First n results.</span></span>

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

### <span data-ttu-id="5759a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5759a-126">CommonParameters</span></span>
<span data-ttu-id="5759a-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5759a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5759a-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5759a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5759a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5759a-129">INPUTS</span></span>

### <span data-ttu-id="5759a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5759a-130">System.String</span></span>

## <span data-ttu-id="5759a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5759a-131">OUTPUTS</span></span>

### <span data-ttu-id="5759a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5759a-132">System.String</span></span>

### <span data-ttu-id="5759a-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="5759a-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="5759a-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5759a-134">NOTES</span></span>

## <span data-ttu-id="5759a-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5759a-135">RELATED LINKS</span></span>
