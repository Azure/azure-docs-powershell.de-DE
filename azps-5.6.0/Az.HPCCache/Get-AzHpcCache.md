---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: c88e7d2b930eb7d04760f963a5ab8ea60ab8d455
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948664"
---
# <span data-ttu-id="fea48-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="fea48-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="fea48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea48-102">SYNOPSIS</span></span>
<span data-ttu-id="fea48-103">Ruft einen Cache(n) ab.</span><span class="sxs-lookup"><span data-stu-id="fea48-103">Gets a cache(s).</span></span>

## <span data-ttu-id="fea48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fea48-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fea48-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fea48-105">DESCRIPTION</span></span>
<span data-ttu-id="fea48-106">Das **Get-AzHpcCache-Cmdlet** ruft einen einzelnen Cache, cache(n) in einer bestimmten Ressourcengruppe oder eine abonnementweite Liste von Caches ab.</span><span class="sxs-lookup"><span data-stu-id="fea48-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="fea48-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fea48-107">EXAMPLES</span></span>

### <span data-ttu-id="fea48-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fea48-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="fea48-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fea48-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="fea48-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fea48-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="fea48-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fea48-111">PARAMETERS</span></span>

### <span data-ttu-id="fea48-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea48-112">-DefaultProfile</span></span>
<span data-ttu-id="fea48-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fea48-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea48-114">-Name</span><span class="sxs-lookup"><span data-stu-id="fea48-114">-Name</span></span>
<span data-ttu-id="fea48-115">Name eines bestimmten Caches.</span><span class="sxs-lookup"><span data-stu-id="fea48-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea48-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea48-116">-ResourceGroupName</span></span>
<span data-ttu-id="fea48-117">Name der Ressourcengruppe, unter der Sie cache(n) auflisten möchten.</span><span class="sxs-lookup"><span data-stu-id="fea48-117">Name of resource group under which you want to list cache(s).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea48-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea48-118">CommonParameters</span></span>
<span data-ttu-id="fea48-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fea48-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea48-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fea48-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea48-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fea48-121">INPUTS</span></span>

### <span data-ttu-id="fea48-122">System.String</span><span class="sxs-lookup"><span data-stu-id="fea48-122">System.String</span></span>

## <span data-ttu-id="fea48-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fea48-123">OUTPUTS</span></span>

### <span data-ttu-id="fea48-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="fea48-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="fea48-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fea48-125">NOTES</span></span>

## <span data-ttu-id="fea48-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fea48-126">RELATED LINKS</span></span>
