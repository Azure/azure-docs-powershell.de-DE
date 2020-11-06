---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: fca64401f4671db63d76d491476f0e276e92055a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498878"
---
# <span data-ttu-id="b609f-101">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b609f-101">Remove-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="b609f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b609f-102">SYNOPSIS</span></span>
<span data-ttu-id="b609f-103">Deaktiviert die Diagnose für einen Azure-a/a-Cache.</span><span class="sxs-lookup"><span data-stu-id="b609f-103">Disables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b609f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b609f-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b609f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b609f-105">DESCRIPTION</span></span>
<span data-ttu-id="b609f-106">Das Cmdlet **Remove-AzureRmRedisCacheDiagnostics** deaktiviert die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="b609f-106">The **Remove-AzureRmRedisCacheDiagnostics** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="b609f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b609f-107">EXAMPLES</span></span>

### <span data-ttu-id="b609f-108">Beispiel 1: Deaktivieren der Diagnose</span><span class="sxs-lookup"><span data-stu-id="b609f-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="b609f-109">Mit diesem Befehl wird die Diagnose für den angegebenen Azure-a/a-Cache deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b609f-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>

<span data-ttu-id="b609f-110">Dadurch wird die Diagnose für alle Azure-a/a-Caches in der gleichen Region für das Abonnement deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b609f-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="b609f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b609f-111">PARAMETERS</span></span>

### <span data-ttu-id="b609f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b609f-112">-DefaultProfile</span></span>
<span data-ttu-id="b609f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b609f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b609f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b609f-114">-Name</span></span>
<span data-ttu-id="b609f-115">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="b609f-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="b609f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b609f-116">-ResourceGroupName</span></span>
<span data-ttu-id="b609f-117">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="b609f-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="b609f-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b609f-118">-Confirm</span></span>
<span data-ttu-id="b609f-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b609f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b609f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b609f-120">-WhatIf</span></span>
<span data-ttu-id="b609f-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b609f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b609f-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b609f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b609f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b609f-123">CommonParameters</span></span>
<span data-ttu-id="b609f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b609f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b609f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b609f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b609f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b609f-126">INPUTS</span></span>

### <span data-ttu-id="b609f-127">Keine</span><span class="sxs-lookup"><span data-stu-id="b609f-127">None</span></span>

## <span data-ttu-id="b609f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b609f-128">OUTPUTS</span></span>

### <span data-ttu-id="b609f-129">Void</span><span class="sxs-lookup"><span data-stu-id="b609f-129">Void</span></span>

## <span data-ttu-id="b609f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b609f-130">NOTES</span></span>
* <span data-ttu-id="b609f-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="b609f-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="b609f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b609f-132">RELATED LINKS</span></span>

[<span data-ttu-id="b609f-133">Satz-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b609f-133">Set-AzureRmRedisCacheDiagnostics</span></span>](./Set-AzureRmRedisCacheDiagnostics.md)


