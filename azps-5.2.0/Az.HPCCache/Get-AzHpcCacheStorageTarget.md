---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291964"
---
# <span data-ttu-id="01d8f-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="01d8f-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="01d8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="01d8f-103">Holen Sie sich die HpC-Cachespeicherziel(en).</span><span class="sxs-lookup"><span data-stu-id="01d8f-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="01d8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01d8f-104">SYNTAX</span></span>

### <span data-ttu-id="01d8f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="01d8f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01d8f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01d8f-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01d8f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01d8f-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01d8f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01d8f-108">DESCRIPTION</span></span>
<span data-ttu-id="01d8f-109">Das **Cmdlet "Get-AzHpcCacheStorageTarget"** ruft Speicherziel(en) ab, die im Cache vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="01d8f-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="01d8f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01d8f-110">EXAMPLES</span></span>

### <span data-ttu-id="01d8f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01d8f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="01d8f-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="01d8f-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="01d8f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01d8f-113">PARAMETERS</span></span>

### <span data-ttu-id="01d8f-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="01d8f-114">-CacheId</span></span>
<span data-ttu-id="01d8f-115">Die Ressourcen-ID des Caches</span><span class="sxs-lookup"><span data-stu-id="01d8f-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="01d8f-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="01d8f-116">-CacheName</span></span>
<span data-ttu-id="01d8f-117">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="01d8f-117">Name of cache.</span></span>

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

### <span data-ttu-id="01d8f-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="01d8f-118">-CacheObject</span></span>
<span data-ttu-id="01d8f-119">Das zu startde Cacheobjekt.</span><span class="sxs-lookup"><span data-stu-id="01d8f-119">The cache object to start.</span></span>

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

### <span data-ttu-id="01d8f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d8f-120">-DefaultProfile</span></span>
<span data-ttu-id="01d8f-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01d8f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d8f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="01d8f-122">-Name</span></span>
<span data-ttu-id="01d8f-123">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="01d8f-123">Name of storage target.</span></span>

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

### <span data-ttu-id="01d8f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01d8f-124">-ResourceGroupName</span></span>
<span data-ttu-id="01d8f-125">Der Name des Ressourcengruppencaches ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="01d8f-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="01d8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d8f-126">CommonParameters</span></span>
<span data-ttu-id="01d8f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d8f-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01d8f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d8f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01d8f-129">INPUTS</span></span>

### <span data-ttu-id="01d8f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="01d8f-130">System.String</span></span>

## <span data-ttu-id="01d8f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01d8f-131">OUTPUTS</span></span>

### <span data-ttu-id="01d8f-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="01d8f-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="01d8f-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01d8f-133">NOTES</span></span>

## <span data-ttu-id="01d8f-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01d8f-134">RELATED LINKS</span></span>
