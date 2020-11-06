---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: ea99137cdd97963bd3d16c9bf0d9b81012e3352b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503417"
---
# <span data-ttu-id="52f21-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="52f21-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="52f21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52f21-102">SYNOPSIS</span></span>
<span data-ttu-id="52f21-103">Aktiviert die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="52f21-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52f21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52f21-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52f21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52f21-105">DESCRIPTION</span></span>
<span data-ttu-id="52f21-106">Das Cmdlet " **Satz-AzureRmRedisCacheDiagnostics** " ermöglicht die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="52f21-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="52f21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52f21-107">EXAMPLES</span></span>

### <span data-ttu-id="52f21-108">Beispiel 1: Aktivieren der Diagnose</span><span class="sxs-lookup"><span data-stu-id="52f21-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="52f21-109">Dieser Befehl aktiviert die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="52f21-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="52f21-110">Mit diesem Befehl wird die Diagnose aktiviert, oder das Speicherkonto für alle Azure-a/a-Caches in der gleichen Region für das Abonnement wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="52f21-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="52f21-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="52f21-111">PARAMETERS</span></span>

### <span data-ttu-id="52f21-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f21-112">-DefaultProfile</span></span>
<span data-ttu-id="52f21-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52f21-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52f21-114">-Name</span><span class="sxs-lookup"><span data-stu-id="52f21-114">-Name</span></span>
<span data-ttu-id="52f21-115">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="52f21-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="52f21-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f21-116">-ResourceGroupName</span></span>
<span data-ttu-id="52f21-117">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="52f21-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="52f21-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="52f21-118">-StorageAccountId</span></span>
<span data-ttu-id="52f21-119">Gibt die Ressourcen-ID des speicherkontos an, mit dem die Diagnosedaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="52f21-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="52f21-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52f21-120">-Confirm</span></span>
<span data-ttu-id="52f21-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52f21-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f21-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f21-122">-WhatIf</span></span>
<span data-ttu-id="52f21-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52f21-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52f21-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52f21-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f21-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f21-125">CommonParameters</span></span>
<span data-ttu-id="52f21-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f21-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f21-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f21-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f21-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52f21-128">INPUTS</span></span>

### <span data-ttu-id="52f21-129">System. String</span><span class="sxs-lookup"><span data-stu-id="52f21-129">System.String</span></span>

## <span data-ttu-id="52f21-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52f21-130">OUTPUTS</span></span>

### <span data-ttu-id="52f21-131">System. void</span><span class="sxs-lookup"><span data-stu-id="52f21-131">System.Void</span></span>

## <span data-ttu-id="52f21-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="52f21-132">NOTES</span></span>
* <span data-ttu-id="52f21-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="52f21-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="52f21-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52f21-134">RELATED LINKS</span></span>

[<span data-ttu-id="52f21-135">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="52f21-135">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


