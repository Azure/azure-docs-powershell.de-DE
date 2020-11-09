---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302641"
---
# <span data-ttu-id="34987-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="34987-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="34987-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34987-102">SYNOPSIS</span></span>
<span data-ttu-id="34987-103">Entfernt den Patch-Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="34987-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="34987-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34987-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34987-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34987-105">DESCRIPTION</span></span>
<span data-ttu-id="34987-106">Das Cmdlet " **Remove-AzRedisCachePatchSchedule** " entfernt den Patch-Terminplan aus einem Cache im Azure-Klasse-Cache.</span><span class="sxs-lookup"><span data-stu-id="34987-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="34987-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34987-107">EXAMPLES</span></span>

### <span data-ttu-id="34987-108">Beispiel 1: Entfernen des Patch-Zeitplans</span><span class="sxs-lookup"><span data-stu-id="34987-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="34987-109">Mit diesem Befehl wird der Patch-Zeitplan aus dem Cache mit dem Namen RedisCache06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="34987-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="34987-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="34987-110">PARAMETERS</span></span>

### <span data-ttu-id="34987-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34987-111">-DefaultProfile</span></span>
<span data-ttu-id="34987-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34987-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34987-113">-Name</span><span class="sxs-lookup"><span data-stu-id="34987-113">-Name</span></span>
<span data-ttu-id="34987-114">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="34987-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="34987-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34987-115">-PassThru</span></span>
<span data-ttu-id="34987-116">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="34987-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="34987-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34987-117">-ResourceGroupName</span></span>
<span data-ttu-id="34987-118">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="34987-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="34987-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34987-119">-Confirm</span></span>
<span data-ttu-id="34987-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34987-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34987-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34987-121">-WhatIf</span></span>
<span data-ttu-id="34987-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34987-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34987-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34987-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34987-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34987-124">CommonParameters</span></span>
<span data-ttu-id="34987-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34987-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34987-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34987-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34987-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34987-127">INPUTS</span></span>

### <span data-ttu-id="34987-128">System. String</span><span class="sxs-lookup"><span data-stu-id="34987-128">System.String</span></span>

## <span data-ttu-id="34987-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34987-129">OUTPUTS</span></span>

### <span data-ttu-id="34987-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34987-130">System.Boolean</span></span>

## <span data-ttu-id="34987-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="34987-131">NOTES</span></span>
* <span data-ttu-id="34987-132">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="34987-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="34987-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34987-133">RELATED LINKS</span></span>

[<span data-ttu-id="34987-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="34987-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="34987-135">Neu – AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="34987-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="34987-136">Neu – AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="34987-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


