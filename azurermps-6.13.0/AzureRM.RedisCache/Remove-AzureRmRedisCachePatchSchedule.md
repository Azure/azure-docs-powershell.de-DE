---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 7224e83333b281fac849ee9e5d99a0691aba3ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663643"
---
# <span data-ttu-id="0ac61-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0ac61-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="0ac61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ac61-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac61-103">Entfernt den Patch-Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="0ac61-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ac61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ac61-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ac61-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ac61-105">DESCRIPTION</span></span>
<span data-ttu-id="0ac61-106">Das Cmdlet " **Remove-AzureRmRedisCachePatchSchedule** " entfernt den Patch-Terminplan aus einem Cache im Azure-Klasse-Cache.</span><span class="sxs-lookup"><span data-stu-id="0ac61-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="0ac61-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ac61-107">EXAMPLES</span></span>

### <span data-ttu-id="0ac61-108">Beispiel 1: Entfernen des Patch-Zeitplans</span><span class="sxs-lookup"><span data-stu-id="0ac61-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="0ac61-109">Mit diesem Befehl wird der Patch-Zeitplan aus dem Cache mit dem Namen RedisCache06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="0ac61-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="0ac61-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ac61-110">PARAMETERS</span></span>

### <span data-ttu-id="0ac61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac61-111">-DefaultProfile</span></span>
<span data-ttu-id="0ac61-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ac61-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ac61-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0ac61-113">-Name</span></span>
<span data-ttu-id="0ac61-114">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="0ac61-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="0ac61-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ac61-115">-PassThru</span></span>
<span data-ttu-id="0ac61-116">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="0ac61-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0ac61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac61-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ac61-118">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="0ac61-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="0ac61-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ac61-119">-Confirm</span></span>
<span data-ttu-id="0ac61-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ac61-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ac61-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ac61-121">-WhatIf</span></span>
<span data-ttu-id="0ac61-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ac61-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ac61-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ac61-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ac61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac61-124">CommonParameters</span></span>
<span data-ttu-id="0ac61-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac61-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ac61-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac61-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ac61-127">INPUTS</span></span>

### <span data-ttu-id="0ac61-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0ac61-128">System.String</span></span>

## <span data-ttu-id="0ac61-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ac61-129">OUTPUTS</span></span>

### <span data-ttu-id="0ac61-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ac61-130">System.Boolean</span></span>

## <span data-ttu-id="0ac61-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ac61-131">NOTES</span></span>
* <span data-ttu-id="0ac61-132">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="0ac61-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="0ac61-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ac61-133">RELATED LINKS</span></span>

[<span data-ttu-id="0ac61-134">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0ac61-134">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="0ac61-135">Neu – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0ac61-135">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="0ac61-136">Neu – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="0ac61-136">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


