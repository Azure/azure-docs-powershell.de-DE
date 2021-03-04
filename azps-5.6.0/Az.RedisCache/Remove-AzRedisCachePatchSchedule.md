---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 42f91d45bf93f453e4c6368abaabcb64f9234771
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943937"
---
# <span data-ttu-id="f117f-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f117f-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="f117f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f117f-102">SYNOPSIS</span></span>
<span data-ttu-id="f117f-103">Entfernt den Patchzeitplan.</span><span class="sxs-lookup"><span data-stu-id="f117f-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="f117f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f117f-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f117f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f117f-105">DESCRIPTION</span></span>
<span data-ttu-id="f117f-106">Das **Cmdlet Remove-AzRedisCachePatchSchedule** entfernt den Patchzeitplan aus einem Cache in Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="f117f-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="f117f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f117f-107">EXAMPLES</span></span>

### <span data-ttu-id="f117f-108">Beispiel 1: Entfernen des Patchzeitplans</span><span class="sxs-lookup"><span data-stu-id="f117f-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="f117f-109">Mit diesem Befehl wird der Patchzeitplan aus dem Cache mit dem Namen RedisCache06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="f117f-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="f117f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f117f-110">PARAMETERS</span></span>

### <span data-ttu-id="f117f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f117f-111">-DefaultProfile</span></span>
<span data-ttu-id="f117f-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f117f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f117f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f117f-113">-Name</span></span>
<span data-ttu-id="f117f-114">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="f117f-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="f117f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f117f-115">-PassThru</span></span>
<span data-ttu-id="f117f-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f117f-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f117f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f117f-117">-ResourceGroupName</span></span>
<span data-ttu-id="f117f-118">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="f117f-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="f117f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f117f-119">-Confirm</span></span>
<span data-ttu-id="f117f-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f117f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f117f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f117f-121">-WhatIf</span></span>
<span data-ttu-id="f117f-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f117f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f117f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f117f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f117f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f117f-124">CommonParameters</span></span>
<span data-ttu-id="f117f-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f117f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f117f-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f117f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f117f-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f117f-127">INPUTS</span></span>

### <span data-ttu-id="f117f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f117f-128">System.String</span></span>

## <span data-ttu-id="f117f-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f117f-129">OUTPUTS</span></span>

### <span data-ttu-id="f117f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f117f-130">System.Boolean</span></span>

## <span data-ttu-id="f117f-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f117f-131">NOTES</span></span>
* <span data-ttu-id="f117f-132">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="f117f-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f117f-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f117f-133">RELATED LINKS</span></span>

[<span data-ttu-id="f117f-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f117f-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="f117f-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f117f-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="f117f-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f117f-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


