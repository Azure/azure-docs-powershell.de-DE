---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150993"
---
# <span data-ttu-id="4b886-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="4b886-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="4b886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b886-102">SYNOPSIS</span></span>
<span data-ttu-id="4b886-103">Ruft den Status des Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="4b886-103">Gets the status of operation.</span></span>

## <span data-ttu-id="4b886-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b886-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4b886-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b886-105">DESCRIPTION</span></span>
<span data-ttu-id="4b886-106">Ruft den Status des Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="4b886-106">Gets the status of operation.</span></span>

## <span data-ttu-id="4b886-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b886-107">EXAMPLES</span></span>

### <span data-ttu-id="4b886-108">Beispiel 1: Status des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="4b886-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="4b886-109">Dieser Befehl ruft den Status eines Vorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="4b886-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="4b886-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b886-110">PARAMETERS</span></span>

### <span data-ttu-id="4b886-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b886-111">-DefaultProfile</span></span>
<span data-ttu-id="4b886-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b886-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b886-113">-Location</span><span class="sxs-lookup"><span data-stu-id="4b886-113">-Location</span></span>
<span data-ttu-id="4b886-114">Der Bereich, in dem sich der Vorgang befindet.</span><span class="sxs-lookup"><span data-stu-id="4b886-114">The region the operation is in.</span></span>

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

### <span data-ttu-id="4b886-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4b886-115">-OperationId</span></span>
<span data-ttu-id="4b886-116">Der eindeutige Bezeichner des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4b886-116">The operation's unique identifier.</span></span>

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

### <span data-ttu-id="4b886-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b886-117">-SubscriptionId</span></span>
<span data-ttu-id="4b886-118">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="4b886-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4b886-119">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="4b886-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4b886-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b886-120">CommonParameters</span></span>
<span data-ttu-id="4b886-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b886-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b886-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b886-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b886-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b886-123">INPUTS</span></span>

## <span data-ttu-id="4b886-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b886-124">OUTPUTS</span></span>

### <span data-ttu-id="4b886-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="4b886-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="4b886-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b886-126">NOTES</span></span>

<span data-ttu-id="4b886-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4b886-127">ALIASES</span></span>

## <span data-ttu-id="4b886-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b886-128">RELATED LINKS</span></span>

