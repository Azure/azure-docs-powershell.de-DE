---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291970"
---
# <span data-ttu-id="31681-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="31681-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="31681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31681-102">SYNOPSIS</span></span>
<span data-ttu-id="31681-103">Ruft einen(n) Cache(en) ab.</span><span class="sxs-lookup"><span data-stu-id="31681-103">Gets a cache(s).</span></span>

## <span data-ttu-id="31681-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31681-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31681-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31681-105">DESCRIPTION</span></span>
<span data-ttu-id="31681-106">Das **Cmdlet "Get-AzHpcCache"** ruft einen einzelnen Cache, cache(s) in einer bestimmten Ressourcengruppe oder eine abonnementweite Liste von Caches ab.</span><span class="sxs-lookup"><span data-stu-id="31681-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="31681-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="31681-107">EXAMPLES</span></span>

### <span data-ttu-id="31681-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="31681-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="31681-109">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="31681-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="31681-110">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="31681-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="31681-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31681-111">PARAMETERS</span></span>

### <span data-ttu-id="31681-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31681-112">-DefaultProfile</span></span>
<span data-ttu-id="31681-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31681-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31681-114">-Name</span><span class="sxs-lookup"><span data-stu-id="31681-114">-Name</span></span>
<span data-ttu-id="31681-115">Name eines bestimmten Caches.</span><span class="sxs-lookup"><span data-stu-id="31681-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="31681-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31681-116">-ResourceGroupName</span></span>
<span data-ttu-id="31681-117">Name der Ressourcengruppe, unter der Sie den Cache(n) auflisten möchten.</span><span class="sxs-lookup"><span data-stu-id="31681-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="31681-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31681-118">CommonParameters</span></span>
<span data-ttu-id="31681-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31681-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31681-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31681-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31681-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="31681-121">INPUTS</span></span>

### <span data-ttu-id="31681-122">System.String</span><span class="sxs-lookup"><span data-stu-id="31681-122">System.String</span></span>

## <span data-ttu-id="31681-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="31681-123">OUTPUTS</span></span>

### <span data-ttu-id="31681-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="31681-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="31681-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="31681-125">NOTES</span></span>

## <span data-ttu-id="31681-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="31681-126">RELATED LINKS</span></span>
