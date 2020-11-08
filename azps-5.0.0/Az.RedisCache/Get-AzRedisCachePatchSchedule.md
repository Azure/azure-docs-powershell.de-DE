---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177758"
---
# <span data-ttu-id="77749-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="77749-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="77749-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77749-102">SYNOPSIS</span></span>
<span data-ttu-id="77749-103">Ruft einen Patch-Zeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="77749-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="77749-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77749-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77749-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77749-105">DESCRIPTION</span></span>
<span data-ttu-id="77749-106">Das Cmdlet " **Get-AzRedisCachePatchSchedule** " erhält einen Patch-Terminplan für einen Cache im Azure-a/a-Cache.</span><span class="sxs-lookup"><span data-stu-id="77749-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="77749-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77749-107">EXAMPLES</span></span>

### <span data-ttu-id="77749-108">Beispiel 1: Abrufen des Patch-Zeitplans</span><span class="sxs-lookup"><span data-stu-id="77749-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="77749-109">Dieser Befehl ruft den Patch-Zeitplan aus dem Cache mit dem Namen RedisCache06 ab.</span><span class="sxs-lookup"><span data-stu-id="77749-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="77749-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="77749-110">PARAMETERS</span></span>

### <span data-ttu-id="77749-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77749-111">-DefaultProfile</span></span>
<span data-ttu-id="77749-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77749-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77749-113">-Name</span><span class="sxs-lookup"><span data-stu-id="77749-113">-Name</span></span>
<span data-ttu-id="77749-114">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="77749-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="77749-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77749-115">-ResourceGroupName</span></span>
<span data-ttu-id="77749-116">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="77749-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="77749-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77749-117">CommonParameters</span></span>
<span data-ttu-id="77749-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77749-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77749-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77749-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77749-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77749-120">INPUTS</span></span>

### <span data-ttu-id="77749-121">System. String</span><span class="sxs-lookup"><span data-stu-id="77749-121">System.String</span></span>

## <span data-ttu-id="77749-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77749-122">OUTPUTS</span></span>

### <span data-ttu-id="77749-123">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="77749-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="77749-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="77749-124">NOTES</span></span>
* <span data-ttu-id="77749-125">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="77749-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="77749-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77749-126">RELATED LINKS</span></span>

[<span data-ttu-id="77749-127">Neu – AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="77749-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="77749-128">Neu – AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="77749-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="77749-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="77749-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


