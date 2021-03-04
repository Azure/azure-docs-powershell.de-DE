---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 6fb1e00f74bcd170d8117e4e37655da6c275a62f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937003"
---
# <span data-ttu-id="fd781-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="fd781-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="fd781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd781-102">SYNOPSIS</span></span>
<span data-ttu-id="fd781-103">Holen Sie sich hpC-Cachespeicherziel(en).</span><span class="sxs-lookup"><span data-stu-id="fd781-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="fd781-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd781-104">SYNTAX</span></span>

### <span data-ttu-id="fd781-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd781-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd781-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd781-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd781-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd781-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd781-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd781-108">DESCRIPTION</span></span>
<span data-ttu-id="fd781-109">Das **Get-AzHpcCacheStorageTarget-Cmdlet** ruft Speicherziel(en) ab, die im Cache vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fd781-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="fd781-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd781-110">EXAMPLES</span></span>

### <span data-ttu-id="fd781-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd781-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="fd781-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fd781-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="fd781-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fd781-113">PARAMETERS</span></span>

### <span data-ttu-id="fd781-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="fd781-114">-CacheId</span></span>
<span data-ttu-id="fd781-115">Die Ressourcen-ID des Caches</span><span class="sxs-lookup"><span data-stu-id="fd781-115">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd781-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="fd781-116">-CacheName</span></span>
<span data-ttu-id="fd781-117">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="fd781-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd781-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="fd781-118">-CacheObject</span></span>
<span data-ttu-id="fd781-119">Das zu startende Cacheobjekt.</span><span class="sxs-lookup"><span data-stu-id="fd781-119">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd781-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd781-120">-DefaultProfile</span></span>
<span data-ttu-id="fd781-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd781-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd781-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fd781-122">-Name</span></span>
<span data-ttu-id="fd781-123">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="fd781-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd781-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd781-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd781-125">Der Name des Ressourcengruppencaches befindet sich in.</span><span class="sxs-lookup"><span data-stu-id="fd781-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd781-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd781-126">CommonParameters</span></span>
<span data-ttu-id="fd781-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd781-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd781-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd781-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd781-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd781-129">INPUTS</span></span>

### <span data-ttu-id="fd781-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fd781-130">System.String</span></span>

## <span data-ttu-id="fd781-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd781-131">OUTPUTS</span></span>

### <span data-ttu-id="fd781-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="fd781-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="fd781-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fd781-133">NOTES</span></span>

## <span data-ttu-id="fd781-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fd781-134">RELATED LINKS</span></span>
