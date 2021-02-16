---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153065"
---
# <span data-ttu-id="fcecd-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="fcecd-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="fcecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcecd-102">SYNOPSIS</span></span>
<span data-ttu-id="fcecd-103">Ruft einen(n) Cache(en) ab.</span><span class="sxs-lookup"><span data-stu-id="fcecd-103">Gets a cache(s).</span></span>

## <span data-ttu-id="fcecd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcecd-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcecd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcecd-105">DESCRIPTION</span></span>
<span data-ttu-id="fcecd-106">Das **Cmdlet "Get-AzHpcCache"** ruft einen einzelnen Cache, cache(s) in einer bestimmten Ressourcengruppe oder eine abonnementweite Liste von Caches ab.</span><span class="sxs-lookup"><span data-stu-id="fcecd-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="fcecd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcecd-107">EXAMPLES</span></span>

### <span data-ttu-id="fcecd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcecd-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="fcecd-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fcecd-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="fcecd-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fcecd-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="fcecd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcecd-111">PARAMETERS</span></span>

### <span data-ttu-id="fcecd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcecd-112">-DefaultProfile</span></span>
<span data-ttu-id="fcecd-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcecd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcecd-114">-Name</span><span class="sxs-lookup"><span data-stu-id="fcecd-114">-Name</span></span>
<span data-ttu-id="fcecd-115">Name eines bestimmten Caches.</span><span class="sxs-lookup"><span data-stu-id="fcecd-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="fcecd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcecd-116">-ResourceGroupName</span></span>
<span data-ttu-id="fcecd-117">Name der Ressourcengruppe, unter der Sie den Cache(n) auflisten möchten.</span><span class="sxs-lookup"><span data-stu-id="fcecd-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="fcecd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcecd-118">CommonParameters</span></span>
<span data-ttu-id="fcecd-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcecd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcecd-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcecd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcecd-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcecd-121">INPUTS</span></span>

### <span data-ttu-id="fcecd-122">System.String</span><span class="sxs-lookup"><span data-stu-id="fcecd-122">System.String</span></span>

## <span data-ttu-id="fcecd-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcecd-123">OUTPUTS</span></span>

### <span data-ttu-id="fcecd-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="fcecd-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="fcecd-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fcecd-125">NOTES</span></span>

## <span data-ttu-id="fcecd-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fcecd-126">RELATED LINKS</span></span>
