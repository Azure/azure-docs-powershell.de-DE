---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: dab4333907d50853474ff795d33263846af249b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500437"
---
# <span data-ttu-id="2dd6e-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2dd6e-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="2dd6e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2dd6e-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd6e-103">Entfernt den Patch-Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dd6e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dd6e-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dd6e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dd6e-105">DESCRIPTION</span></span>
<span data-ttu-id="2dd6e-106">Das Cmdlet " **Remove-AzureRmRedisCachePatchSchedule** " entfernt den Patch-Terminplan aus einem Cache im Azure-Klasse-Cache.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="2dd6e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2dd6e-107">EXAMPLES</span></span>

### <span data-ttu-id="2dd6e-108">Beispiel 1: Entfernen des Patch-Zeitplans</span><span class="sxs-lookup"><span data-stu-id="2dd6e-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="2dd6e-109">Mit diesem Befehl wird der Patch-Zeitplan aus dem Cache mit dem Namen RedisCache06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="2dd6e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dd6e-110">PARAMETERS</span></span>

### <span data-ttu-id="2dd6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd6e-111">-DefaultProfile</span></span>
<span data-ttu-id="2dd6e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd6e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2dd6e-113">-Name</span></span>
<span data-ttu-id="2dd6e-114">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-114">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd6e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dd6e-115">-PassThru</span></span>
<span data-ttu-id="2dd6e-116">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="2dd6e-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2dd6e-118">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-118">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd6e-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2dd6e-119">-Confirm</span></span>
<span data-ttu-id="2dd6e-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd6e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd6e-121">-WhatIf</span></span>
<span data-ttu-id="2dd6e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd6e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd6e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd6e-124">CommonParameters</span></span>
<span data-ttu-id="2dd6e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd6e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dd6e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd6e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2dd6e-127">INPUTS</span></span>

### <span data-ttu-id="2dd6e-128">Keine</span><span class="sxs-lookup"><span data-stu-id="2dd6e-128">None</span></span>
<span data-ttu-id="2dd6e-129">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="2dd6e-129">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="2dd6e-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2dd6e-130">OUTPUTS</span></span>

### <span data-ttu-id="2dd6e-131">Keine</span><span class="sxs-lookup"><span data-stu-id="2dd6e-131">None</span></span>

## <span data-ttu-id="2dd6e-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2dd6e-132">NOTES</span></span>
* <span data-ttu-id="2dd6e-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="2dd6e-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="2dd6e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2dd6e-134">RELATED LINKS</span></span>

[<span data-ttu-id="2dd6e-135">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2dd6e-135">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="2dd6e-136">Neu – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="2dd6e-136">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="2dd6e-137">Neu – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="2dd6e-137">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


