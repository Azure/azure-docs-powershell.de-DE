---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: b04977869364f43644556b9ef6bf16ac68d01f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662624"
---
# <span data-ttu-id="3b3ae-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="3b3ae-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="3b3ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b3ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3ae-103">Fügt einen Patch-Zeitplan hinzu.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b3ae-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b3ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b3ae-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3ae-106">Mit dem Cmdlet " **New-AzureRmRedisCachePatchSchedule** " wird ein Patch-Zeitplan zu einem Cache im Azure-Schlüssel-a-Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="3b3ae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b3ae-107">EXAMPLES</span></span>

### <span data-ttu-id="3b3ae-108">Beispiel 1: Erstellen und Hinzufügen eines Patch-Zeitplans für einen Cache</span><span class="sxs-lookup"><span data-stu-id="3b3ae-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="3b3ae-109">Mit diesem Befehl wird dem Cache mit dem Namen RedisCache06 ein Patch-Zeitplan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="3b3ae-110">Der Parameter Entries nimmt als Wert einen Befehl auf, der zum Erstellen eines Zeitplans **New-AzureRmRedisCacheScheduleEntry** verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="3b3ae-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b3ae-111">PARAMETERS</span></span>

### <span data-ttu-id="3b3ae-112">-Einträge</span><span class="sxs-lookup"><span data-stu-id="3b3ae-112">-Entries</span></span>
<span data-ttu-id="3b3ae-113">Gibt ein Array von Zeitplänen an, die von diesem Cmdlet für einen Cache festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-113">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="3b3ae-114">Verwenden Sie das New-AzureRmRedisCacheScheduleEntry-Cmdlet, um ein **PSScheduleEntry** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-114">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ae-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3b3ae-115">-Name</span></span>
<span data-ttu-id="3b3ae-116">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-116">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="3b3ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b3ae-118">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="3b3ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3ae-119">-DefaultProfile</span></span>
<span data-ttu-id="3b3ae-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3ae-121">CommonParameters</span></span>
<span data-ttu-id="3b3ae-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3ae-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3ae-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3ae-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b3ae-124">INPUTS</span></span>

### <span data-ttu-id="3b3ae-125">Keine</span><span class="sxs-lookup"><span data-stu-id="3b3ae-125">None</span></span>
<span data-ttu-id="3b3ae-126">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-126">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3b3ae-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b3ae-127">OUTPUTS</span></span>

### <span data-ttu-id="3b3ae-128">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="3b3ae-128">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="3b3ae-129">Dieses Cmdlet gibt den Patch-Terminplan Eintrag zurück, der für den Cache eingestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3b3ae-129">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="3b3ae-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b3ae-130">NOTES</span></span>
* <span data-ttu-id="3b3ae-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="3b3ae-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="3b3ae-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b3ae-132">RELATED LINKS</span></span>

[<span data-ttu-id="3b3ae-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="3b3ae-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="3b3ae-134">Neu – AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="3b3ae-134">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="3b3ae-135">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="3b3ae-135">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


