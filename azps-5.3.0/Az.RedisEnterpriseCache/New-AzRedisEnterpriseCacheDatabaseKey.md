---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/new-azredisenterprisecachedatabasekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCacheDatabaseKey.md
ms.openlocfilehash: ab5985a7302834f4f7184a43ac2f5ebf795a3d83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459588"
---
# <span data-ttu-id="ef27b-101">New-AzRedisEnterpriseCacheDatabaseKey</span><span class="sxs-lookup"><span data-stu-id="ef27b-101">New-AzRedisEnterpriseCacheDatabaseKey</span></span>

## <span data-ttu-id="ef27b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef27b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef27b-103">Generiert die Zugriffsschlüssel der RedisEnterprise-Datenbank erneut.</span><span class="sxs-lookup"><span data-stu-id="ef27b-103">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="ef27b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef27b-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCacheDatabaseKey -ClusterName <String> -ResourceGroupName <String>
 -KeyType <AccessKeyType> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef27b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef27b-105">DESCRIPTION</span></span>
<span data-ttu-id="ef27b-106">Generiert die Zugriffsschlüssel der RedisEnterprise-Datenbank erneut.</span><span class="sxs-lookup"><span data-stu-id="ef27b-106">Regenerates the RedisEnterprise database's access keys.</span></span>

## <span data-ttu-id="ef27b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef27b-107">EXAMPLES</span></span>

### <span data-ttu-id="ef27b-108">Beispiel 1: Erneut generierten primären Zugriffsschlüssel</span><span class="sxs-lookup"><span data-stu-id="ef27b-108">Example 1: Regenerate primary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Primary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
new-primary-key                              secondary-key

```

<span data-ttu-id="ef27b-109">Mit diesem Befehl wird der primär geheime Zugriffsschlüssel erneut generiert, der zum Authentifizieren von Verbindungen mit der Datenbank des Redis Enterprise Cache mit dem Namen "MyCache" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef27b-109">This command regenerates the primary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="ef27b-110">Beispiel 2: Erneut generierten sekundären Zugriffsschlüssel</span><span class="sxs-lookup"><span data-stu-id="ef27b-110">Example 2: Regenerate secondary access key</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCacheDatabaseKey -Name "MyCache" -ResourceGroupName "MyGroup" -KeyType "Secondary"

PrimaryKey                                   SecondaryKey
----------                                   ------------
primary-key                                  new-secondary-key

```

<span data-ttu-id="ef27b-111">Mit diesem Befehl wird der sekundäre geheime Zugriffsschlüssel erneut generiert, der zum Authentifizieren von Verbindungen mit der Datenbank des Redis Enterprise Cache namens MyCache verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef27b-111">This command regenerates the secondary secret access key used for authenticating connections to the database of the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="ef27b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef27b-112">PARAMETERS</span></span>

### <span data-ttu-id="ef27b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef27b-113">-AsJob</span></span>
<span data-ttu-id="ef27b-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="ef27b-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef27b-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ef27b-115">-ClusterName</span></span>
<span data-ttu-id="ef27b-116">Der Name des RedisEnterprise-Cluster.</span><span class="sxs-lookup"><span data-stu-id="ef27b-116">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="ef27b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef27b-117">-DefaultProfile</span></span>
<span data-ttu-id="ef27b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef27b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef27b-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ef27b-119">-KeyType</span></span>
<span data-ttu-id="ef27b-120">Die Zugriffstaste zum erneuten Generierten.</span><span class="sxs-lookup"><span data-stu-id="ef27b-120">Which access key to regenerate.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.AccessKeyType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef27b-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ef27b-121">-NoWait</span></span>
<span data-ttu-id="ef27b-122">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="ef27b-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef27b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef27b-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef27b-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef27b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef27b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef27b-125">-SubscriptionId</span></span>
<span data-ttu-id="ef27b-126">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="ef27b-126">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef27b-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ef27b-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef27b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef27b-128">-Confirm</span></span>
<span data-ttu-id="ef27b-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef27b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef27b-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ef27b-130">-WhatIf</span></span>
<span data-ttu-id="ef27b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef27b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef27b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef27b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef27b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef27b-133">CommonParameters</span></span>
<span data-ttu-id="ef27b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef27b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef27b-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef27b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef27b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef27b-136">INPUTS</span></span>

## <span data-ttu-id="ef27b-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef27b-137">OUTPUTS</span></span>

### <span data-ttu-id="ef27b-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span><span class="sxs-lookup"><span data-stu-id="ef27b-138">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IAccessKeys</span></span>

## <span data-ttu-id="ef27b-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef27b-139">NOTES</span></span>

<span data-ttu-id="ef27b-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ef27b-140">ALIASES</span></span>

## <span data-ttu-id="ef27b-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef27b-141">RELATED LINKS</span></span>

