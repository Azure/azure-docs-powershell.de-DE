---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: d32fe3286a8c6e4b723137f8b20921c79caa45be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935544"
---
# <span data-ttu-id="8a069-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8a069-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="8a069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a069-102">SYNOPSIS</span></span>
<span data-ttu-id="8a069-103">Deaktiviert die Diagnose in einem Azure Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="8a069-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="8a069-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a069-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a069-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a069-105">DESCRIPTION</span></span>
<span data-ttu-id="8a069-106">Das **Cmdlet Remove-AzRedisCacheDiagnostic** deaktiviert die Diagnose in einem Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="8a069-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="8a069-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a069-107">EXAMPLES</span></span>

### <span data-ttu-id="8a069-108">Beispiel 1: Deaktivieren der Diagnose</span><span class="sxs-lookup"><span data-stu-id="8a069-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="8a069-109">Mit diesem Befehl wird die Diagnose für angegebenen Azure Redis Cache deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a069-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="8a069-110">Dadurch wird die Diagnose für alle Azure Redis-Caches in derselben Region für das Abonnement deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a069-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="8a069-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8a069-111">PARAMETERS</span></span>

### <span data-ttu-id="8a069-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a069-112">-DefaultProfile</span></span>
<span data-ttu-id="8a069-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a069-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a069-114">-Name</span><span class="sxs-lookup"><span data-stu-id="8a069-114">-Name</span></span>
<span data-ttu-id="8a069-115">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="8a069-115">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a069-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a069-116">-ResourceGroupName</span></span>
<span data-ttu-id="8a069-117">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="8a069-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="8a069-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a069-118">-Confirm</span></span>
<span data-ttu-id="8a069-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a069-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a069-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a069-120">-WhatIf</span></span>
<span data-ttu-id="8a069-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a069-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a069-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a069-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a069-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a069-123">CommonParameters</span></span>
<span data-ttu-id="8a069-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a069-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a069-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a069-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a069-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a069-126">INPUTS</span></span>

### <span data-ttu-id="8a069-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8a069-127">System.String</span></span>

## <span data-ttu-id="8a069-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a069-128">OUTPUTS</span></span>

### <span data-ttu-id="8a069-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="8a069-129">System.Void</span></span>

## <span data-ttu-id="8a069-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8a069-130">NOTES</span></span>
* <span data-ttu-id="8a069-131">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="8a069-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8a069-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8a069-132">RELATED LINKS</span></span>

[<span data-ttu-id="8a069-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8a069-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


