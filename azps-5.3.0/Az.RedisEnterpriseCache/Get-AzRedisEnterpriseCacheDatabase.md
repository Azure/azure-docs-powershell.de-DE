---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 99956b752b71309278af4c1f9b43b8efa9015f21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459595"
---
# <span data-ttu-id="8ed0d-101">Get-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="8ed0d-101">Get-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="8ed0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ed0d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ed0d-103">Ruft Informationen zu einer Datenbank in einem RedisEnterprise-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-103">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="8ed0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ed0d-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8ed0d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ed0d-105">DESCRIPTION</span></span>
<span data-ttu-id="8ed0d-106">Ruft Informationen zu einer Datenbank in einem RedisEnterprise-Cluster ab.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-106">Gets information about a database in a RedisEnterprise cluster.</span></span>

## <span data-ttu-id="8ed0d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8ed0d-107">EXAMPLES</span></span>

### <span data-ttu-id="8ed0d-108">Beispiel 1: Datenbank erhalten</span><span class="sxs-lookup"><span data-stu-id="8ed0d-108">Example 1: Get database</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="8ed0d-109">Dieser Befehl ruft die Datenbank für den Redis Enterprise-Cache namens "MyCache" ab.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-109">This command gets the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="8ed0d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ed0d-110">PARAMETERS</span></span>

### <span data-ttu-id="8ed0d-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8ed0d-111">-ClusterName</span></span>
<span data-ttu-id="8ed0d-112">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-112">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ed0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ed0d-113">-DefaultProfile</span></span>
<span data-ttu-id="8ed0d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ed0d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ed0d-115">-ResourceGroupName</span></span>
<span data-ttu-id="8ed0d-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="8ed0d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ed0d-117">-SubscriptionId</span></span>
<span data-ttu-id="8ed0d-118">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8ed0d-119">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8ed0d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ed0d-120">CommonParameters</span></span>
<span data-ttu-id="8ed0d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ed0d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ed0d-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ed0d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ed0d-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8ed0d-123">INPUTS</span></span>

## <span data-ttu-id="8ed0d-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8ed0d-124">OUTPUTS</span></span>

### <span data-ttu-id="8ed0d-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="8ed0d-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="8ed0d-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8ed0d-126">NOTES</span></span>

<span data-ttu-id="8ed0d-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8ed0d-127">ALIASES</span></span>

## <span data-ttu-id="8ed0d-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8ed0d-128">RELATED LINKS</span></span>

