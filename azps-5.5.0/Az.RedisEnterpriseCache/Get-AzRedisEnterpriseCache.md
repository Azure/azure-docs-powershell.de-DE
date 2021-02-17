---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCache.md
ms.openlocfilehash: a6fe478aa8221060974f54e75b63a64edf0beae4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172140"
---
# <span data-ttu-id="050ea-101">Get-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="050ea-101">Get-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="050ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="050ea-102">SYNOPSIS</span></span>
<span data-ttu-id="050ea-103">Ruft Informationen zu einem RedisEnterprise-Cluster und seiner zugehörigen Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="050ea-103">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="050ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="050ea-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCache -ResourceGroupName <String> [-ClusterName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="050ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="050ea-105">DESCRIPTION</span></span>
<span data-ttu-id="050ea-106">Ruft Informationen zu einem RedisEnterprise-Cluster und seiner zugehörigen Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="050ea-106">Gets information about a RedisEnterprise cluster and its associated database</span></span>

## <span data-ttu-id="050ea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="050ea-107">EXAMPLES</span></span>

### <span data-ttu-id="050ea-108">Beispiel 1: Erhalten eines Redis Enterprise-Caches nach Name</span><span class="sxs-lookup"><span data-stu-id="050ea-108">Example 1: Get a Redis Enterprise Cache by name</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup" -Name "MyCache"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="050ea-109">Dieser Befehl ruft den Redis Enterprise-Cache namens "MyCache" ab.</span><span class="sxs-lookup"><span data-stu-id="050ea-109">This command gets the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="050ea-110">Beispiel 2: Jeden Redis -Enterprise-Cache in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="050ea-110">Example 2: Get every Redis Enterprise Cache in a resource group</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCache -ResourceGroupName "MyGroup"

Location Name     Type                            Zone      Database
-------- ----     ----                            ----      --------
East US  MyCache1 Microsoft.Cache/redisEnterprise           {default}
East US  MyCache2 Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="050ea-111">Dieser Befehl ruft jeden Redis Enterprise-Cache in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="050ea-111">This command gets every Redis Enterprise Cache in the specified resource group.</span></span>

## <span data-ttu-id="050ea-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="050ea-112">PARAMETERS</span></span>

### <span data-ttu-id="050ea-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="050ea-113">-ClusterName</span></span>
<span data-ttu-id="050ea-114">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="050ea-114">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="050ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050ea-115">-DefaultProfile</span></span>
<span data-ttu-id="050ea-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="050ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="050ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="050ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="050ea-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="050ea-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="050ea-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="050ea-119">-SubscriptionId</span></span>
<span data-ttu-id="050ea-120">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="050ea-120">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="050ea-121">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="050ea-121">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="050ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050ea-122">CommonParameters</span></span>
<span data-ttu-id="050ea-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="050ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050ea-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="050ea-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050ea-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="050ea-125">INPUTS</span></span>

## <span data-ttu-id="050ea-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="050ea-126">OUTPUTS</span></span>

### <span data-ttu-id="050ea-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="050ea-127">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="050ea-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="050ea-128">NOTES</span></span>

<span data-ttu-id="050ea-129">ALIASE</span><span class="sxs-lookup"><span data-stu-id="050ea-129">ALIASES</span></span>

## <span data-ttu-id="050ea-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="050ea-130">RELATED LINKS</span></span>

