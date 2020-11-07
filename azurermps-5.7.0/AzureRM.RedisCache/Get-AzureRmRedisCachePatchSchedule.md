---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 091d3d52da1319842d221881f03fca2b21353fa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662352"
---
# <span data-ttu-id="73643-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="73643-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="73643-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73643-102">SYNOPSIS</span></span>
<span data-ttu-id="73643-103">Ruft einen Patch-Zeitplan ab.</span><span class="sxs-lookup"><span data-stu-id="73643-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73643-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73643-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73643-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73643-105">DESCRIPTION</span></span>
<span data-ttu-id="73643-106">Das Cmdlet " **Get-AzureRmRedisCachePatchSchedule** " erhält einen Patch-Terminplan für einen Cache im Azure-a/a-Cache.</span><span class="sxs-lookup"><span data-stu-id="73643-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="73643-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73643-107">EXAMPLES</span></span>

### <span data-ttu-id="73643-108">Beispiel 1: Abrufen des Patch-Zeitplans</span><span class="sxs-lookup"><span data-stu-id="73643-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="73643-109">Dieser Befehl ruft den Patch-Zeitplan aus dem Cache mit dem Namen RedisCache06 ab.</span><span class="sxs-lookup"><span data-stu-id="73643-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="73643-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="73643-110">PARAMETERS</span></span>

### <span data-ttu-id="73643-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73643-111">-DefaultProfile</span></span>
<span data-ttu-id="73643-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73643-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73643-113">-Name</span><span class="sxs-lookup"><span data-stu-id="73643-113">-Name</span></span>
<span data-ttu-id="73643-114">Gibt den Namen eines Caches an.</span><span class="sxs-lookup"><span data-stu-id="73643-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="73643-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73643-115">-ResourceGroupName</span></span>
<span data-ttu-id="73643-116">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="73643-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="73643-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73643-117">CommonParameters</span></span>
<span data-ttu-id="73643-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73643-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73643-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73643-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73643-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73643-120">INPUTS</span></span>

### <span data-ttu-id="73643-121">Keine</span><span class="sxs-lookup"><span data-stu-id="73643-121">None</span></span>
<span data-ttu-id="73643-122">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="73643-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="73643-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73643-123">OUTPUTS</span></span>

### <span data-ttu-id="73643-124">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="73643-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="73643-125">Dieses Cmdlet gibt den Patch-Terminplan Eintrag zurück, der für den Cache eingestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="73643-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="73643-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="73643-126">NOTES</span></span>
* <span data-ttu-id="73643-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="73643-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="73643-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73643-128">RELATED LINKS</span></span>

[<span data-ttu-id="73643-129">Neu – AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="73643-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="73643-130">Neu – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="73643-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="73643-131">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="73643-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


