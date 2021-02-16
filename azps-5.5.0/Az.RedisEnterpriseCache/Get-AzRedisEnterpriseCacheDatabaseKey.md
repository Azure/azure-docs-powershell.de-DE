---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: e602cb4fc86ede6a4e1f7cc894c1825fd1d560fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151009"
---
# <span data-ttu-id="b5f2d-101">Get-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="b5f2d-101">Get-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="b5f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f2d-103">Ruft die Zugriffstasten für die Datenbank "RedisEnterprise" ab.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-103">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="b5f2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5f2d-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5f2d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f2d-106">Ruft die Zugriffstasten für die Datenbank "RedisEnterprise" ab.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-106">Retrieves the access keys for the RedisEnterprise database.</span></span>

## <span data-ttu-id="b5f2d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5f2d-107">EXAMPLES</span></span>

### <span data-ttu-id="b5f2d-108">Beispiel 1: Erhalten von Datenbankzugriffsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="b5f2d-108">Example 1: Get database access keys</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  secondary-key

```

<span data-ttu-id="b5f2d-109">Dieser Befehl ruft die geheimen Zugriffstasten ab, die zum Authentifizieren von Verbindungen mit der Datenbank des Redis Enterprise Cache mit dem Namen "MyCache" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-109">This command gets the secret access keys used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="b5f2d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5f2d-110">PARAMETERS</span></span>

### <span data-ttu-id="b5f2d-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b5f2d-111">-ClusterName</span></span>
<span data-ttu-id="b5f2d-112">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-112">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="b5f2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f2d-113">-DefaultProfile</span></span>
<span data-ttu-id="b5f2d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5f2d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f2d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b5f2d-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="b5f2d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5f2d-117">-SubscriptionId</span></span>
<span data-ttu-id="b5f2d-118">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b5f2d-119">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b5f2d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5f2d-120">-Confirm</span></span>
<span data-ttu-id="b5f2d-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f2d-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b5f2d-122">-WhatIf</span></span>
<span data-ttu-id="b5f2d-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5f2d-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f2d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f2d-125">CommonParameters</span></span>
<span data-ttu-id="b5f2d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f2d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f2d-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5f2d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f2d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5f2d-128">INPUTS</span></span>

## <span data-ttu-id="b5f2d-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5f2d-129">OUTPUTS</span></span>

### <span data-ttu-id="b5f2d-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="b5f2d-130">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="b5f2d-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b5f2d-131">NOTES</span></span>

<span data-ttu-id="b5f2d-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b5f2d-132">ALIASES</span></span>

## <span data-ttu-id="b5f2d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b5f2d-133">RELATED LINKS</span></span>

