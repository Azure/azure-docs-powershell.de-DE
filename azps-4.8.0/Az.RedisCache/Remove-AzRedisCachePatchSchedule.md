---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166160"
---
# <span data-ttu-id="65e56-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="65e56-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="65e56-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65e56-102">SYNOPSIS</span></span>
<span data-ttu-id="65e56-103">Entfernt den Patch-Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="65e56-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="65e56-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65e56-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65e56-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65e56-105">DESCRIPTION</span></span>
<span data-ttu-id="65e56-106">Das Cmdlet " **Remove-AzRedisCachePatchSchedule** " entfernt den Patch-Terminplan aus einem Cache im Azure-Klasse-Cache.</span><span class="sxs-lookup"><span data-stu-id="65e56-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="65e56-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65e56-107">EXAMPLES</span></span>

### <span data-ttu-id="65e56-108">Beispiel 1: Entfernen des Patch-Zeitplans</span><span class="sxs-lookup"><span data-stu-id="65e56-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="65e56-109">Mit diesem Befehl wird der Patch-Zeitplan aus dem Cache mit dem Namen RedisCache06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="65e56-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="65e56-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65e56-110">PARAMETERS</span></span>

### <span data-ttu-id="65e56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e56-111">-DefaultProfile</span></span>
<span data-ttu-id="65e56-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65e56-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65e56-113">-Name</span><span class="sxs-lookup"><span data-stu-id="65e56-113">-Name</span></span>
<span data-ttu-id="65e56-114">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="65e56-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="65e56-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65e56-115">-PassThru</span></span>
<span data-ttu-id="65e56-116">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="65e56-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="65e56-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e56-117">-ResourceGroupName</span></span>
<span data-ttu-id="65e56-118">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="65e56-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="65e56-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65e56-119">-Confirm</span></span>
<span data-ttu-id="65e56-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65e56-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65e56-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65e56-121">-WhatIf</span></span>
<span data-ttu-id="65e56-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65e56-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65e56-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65e56-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65e56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e56-124">CommonParameters</span></span>
<span data-ttu-id="65e56-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e56-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e56-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e56-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65e56-127">INPUTS</span></span>

### <span data-ttu-id="65e56-128">System. String</span><span class="sxs-lookup"><span data-stu-id="65e56-128">System.String</span></span>

## <span data-ttu-id="65e56-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65e56-129">OUTPUTS</span></span>

### <span data-ttu-id="65e56-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65e56-130">System.Boolean</span></span>

## <span data-ttu-id="65e56-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="65e56-131">NOTES</span></span>
* <span data-ttu-id="65e56-132">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="65e56-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="65e56-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65e56-133">RELATED LINKS</span></span>

[<span data-ttu-id="65e56-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="65e56-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="65e56-135">Neu – AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="65e56-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="65e56-136">Neu – AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="65e56-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


