---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ff635c55600c6528ecad537b74a843e2d1da830e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943883"
---
# <span data-ttu-id="54fa4-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="54fa4-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="54fa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="54fa4-103">Ruft die Zugriffstasten für die RedisEnterprise-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="54fa4-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="54fa4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54fa4-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54fa4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54fa4-105">DESCRIPTION</span></span>
<span data-ttu-id="54fa4-106">Ruft die Zugriffstasten für die RedisEnterprise-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="54fa4-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="54fa4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54fa4-107">EXAMPLES</span></span>

### <span data-ttu-id="54fa4-108">Beispiel 1: Erhalten von Datenbankzugriffsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="54fa4-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="54fa4-109">Dieser Befehl ruft die geheimen Zugriffstasten ab, die zum Authentifizieren von Verbindungen mit der Datenbank des Redis Enterprise Cache namens MyCache verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54fa4-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="54fa4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54fa4-110">PARAMETERS</span></span>

### <span data-ttu-id="54fa4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="54fa4-111">-ClusterName</span></span>
<span data-ttu-id="54fa4-112">Der Name des RedisEnterprise-Clusters.</span><span class="sxs-lookup"><span data-stu-id="54fa4-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="54fa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fa4-113">-DefaultProfile</span></span>
<span data-ttu-id="54fa4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54fa4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54fa4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fa4-115">-ResourceGroupName</span></span>
<span data-ttu-id="54fa4-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54fa4-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="54fa4-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54fa4-117">-SubscriptionId</span></span>
<span data-ttu-id="54fa4-118">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="54fa4-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="54fa4-119">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="54fa4-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="54fa4-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54fa4-120">-Confirm</span></span>
<span data-ttu-id="54fa4-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54fa4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fa4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fa4-122">-WhatIf</span></span>
<span data-ttu-id="54fa4-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54fa4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fa4-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54fa4-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fa4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fa4-125">CommonParameters</span></span>
<span data-ttu-id="54fa4-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54fa4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fa4-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54fa4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fa4-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54fa4-128">INPUTS</span></span>

## <span data-ttu-id="54fa4-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54fa4-129">OUTPUTS</span></span>

### <span data-ttu-id="54fa4-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="54fa4-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="54fa4-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="54fa4-131">NOTES</span></span>

<span data-ttu-id="54fa4-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="54fa4-132">ALIASES</span></span>

## <span data-ttu-id="54fa4-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="54fa4-133">RELATED LINKS</span></span>

