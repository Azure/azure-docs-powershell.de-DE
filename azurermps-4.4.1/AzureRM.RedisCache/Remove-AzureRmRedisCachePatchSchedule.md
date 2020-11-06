---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 768b37444155829ba33a5996fb969c21f85ca797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478978"
---
# <span data-ttu-id="0e6f3-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0e6f3-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="0e6f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6f3-103">Entfernt den Patch-Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e6f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e6f3-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e6f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e6f3-105">DESCRIPTION</span></span>
<span data-ttu-id="0e6f3-106">Das Cmdlet " **Remove-AzureRmRedisCachePatchSchedule** " entfernt den Patch-Terminplan aus einem Cache im Azure-Klasse-Cache.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="0e6f3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e6f3-107">EXAMPLES</span></span>

### <span data-ttu-id="0e6f3-108">Beispiel 1: Entfernen des Patch-Zeitplans</span><span class="sxs-lookup"><span data-stu-id="0e6f3-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="0e6f3-109">Mit diesem Befehl wird der Patch-Zeitplan aus dem Cache mit dem Namen RedisCache06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="0e6f3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e6f3-110">PARAMETERS</span></span>

### <span data-ttu-id="0e6f3-111">-Name</span><span class="sxs-lookup"><span data-stu-id="0e6f3-111">-Name</span></span>
<span data-ttu-id="0e6f3-112">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="0e6f3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6f3-113">-ResourceGroupName</span></span>
<span data-ttu-id="0e6f3-114">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="0e6f3-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e6f3-115">-Confirm</span></span>
<span data-ttu-id="0e6f3-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e6f3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e6f3-117">-WhatIf</span></span>
<span data-ttu-id="0e6f3-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e6f3-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e6f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6f3-120">-DefaultProfile</span></span>
<span data-ttu-id="0e6f3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e6f3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6f3-122">CommonParameters</span></span>
<span data-ttu-id="0e6f3-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6f3-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e6f3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6f3-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e6f3-125">INPUTS</span></span>

### <span data-ttu-id="0e6f3-126">Keine</span><span class="sxs-lookup"><span data-stu-id="0e6f3-126">None</span></span>
<span data-ttu-id="0e6f3-127">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="0e6f3-127">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0e6f3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e6f3-128">OUTPUTS</span></span>

### <span data-ttu-id="0e6f3-129">Keine</span><span class="sxs-lookup"><span data-stu-id="0e6f3-129">None</span></span>

## <span data-ttu-id="0e6f3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e6f3-130">NOTES</span></span>
* <span data-ttu-id="0e6f3-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="0e6f3-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="0e6f3-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e6f3-132">RELATED LINKS</span></span>

[<span data-ttu-id="0e6f3-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0e6f3-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="0e6f3-134">Neu – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="0e6f3-134">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="0e6f3-135">Neu – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="0e6f3-135">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


