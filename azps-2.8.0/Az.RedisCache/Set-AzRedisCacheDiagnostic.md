---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 813988d0d5d2a2ed9099167c19d3eca74397ee5b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823612"
---
# <span data-ttu-id="2e4ff-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2e4ff-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="2e4ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4ff-103">Aktiviert die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="2e4ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e4ff-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e4ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e4ff-105">DESCRIPTION</span></span>
<span data-ttu-id="2e4ff-106">Das Cmdlet " **Satz-AzRedisCacheDiagnostic** " ermöglicht die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="2e4ff-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e4ff-107">EXAMPLES</span></span>

### <span data-ttu-id="2e4ff-108">Beispiel 1: Aktivieren der Diagnose</span><span class="sxs-lookup"><span data-stu-id="2e4ff-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="2e4ff-109">Dieser Befehl aktiviert die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="2e4ff-110">Mit diesem Befehl wird die Diagnose aktiviert, oder das Speicherkonto für alle Azure-a/a-Caches in der gleichen Region für das Abonnement wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="2e4ff-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e4ff-111">PARAMETERS</span></span>

### <span data-ttu-id="2e4ff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4ff-112">-DefaultProfile</span></span>
<span data-ttu-id="2e4ff-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e4ff-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2e4ff-114">-Name</span></span>
<span data-ttu-id="2e4ff-115">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="2e4ff-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e4ff-116">-ResourceGroupName</span></span>
<span data-ttu-id="2e4ff-117">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="2e4ff-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2e4ff-118">-StorageAccountId</span></span>
<span data-ttu-id="2e4ff-119">Gibt die Ressourcen-ID des speicherkontos an, mit dem die Diagnosedaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="2e4ff-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e4ff-120">-Confirm</span></span>
<span data-ttu-id="2e4ff-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e4ff-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e4ff-122">-WhatIf</span></span>
<span data-ttu-id="2e4ff-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e4ff-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e4ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4ff-125">CommonParameters</span></span>
<span data-ttu-id="2e4ff-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e4ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4ff-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e4ff-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4ff-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e4ff-128">INPUTS</span></span>

### <span data-ttu-id="2e4ff-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2e4ff-129">System.String</span></span>

## <span data-ttu-id="2e4ff-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e4ff-130">OUTPUTS</span></span>

### <span data-ttu-id="2e4ff-131">System. void</span><span class="sxs-lookup"><span data-stu-id="2e4ff-131">System.Void</span></span>

## <span data-ttu-id="2e4ff-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e4ff-132">NOTES</span></span>
* <span data-ttu-id="2e4ff-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="2e4ff-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="2e4ff-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e4ff-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e4ff-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2e4ff-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


