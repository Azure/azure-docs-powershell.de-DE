---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167399"
---
# <span data-ttu-id="919d7-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="919d7-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="919d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="919d7-102">SYNOPSIS</span></span>
<span data-ttu-id="919d7-103">Deaktiviert die Diagnose für einen Azure-a/a-Cache.</span><span class="sxs-lookup"><span data-stu-id="919d7-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="919d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="919d7-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="919d7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="919d7-105">DESCRIPTION</span></span>
<span data-ttu-id="919d7-106">Das Cmdlet **Remove-AzRedisCacheDiagnostic** deaktiviert die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="919d7-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="919d7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="919d7-107">EXAMPLES</span></span>

### <span data-ttu-id="919d7-108">Beispiel 1: Deaktivieren der Diagnose</span><span class="sxs-lookup"><span data-stu-id="919d7-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="919d7-109">Mit diesem Befehl wird die Diagnose für den angegebenen Azure-a/a-Cache deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="919d7-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="919d7-110">Dadurch wird die Diagnose für alle Azure-a/a-Caches in der gleichen Region für das Abonnement deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="919d7-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="919d7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="919d7-111">PARAMETERS</span></span>

### <span data-ttu-id="919d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919d7-112">-DefaultProfile</span></span>
<span data-ttu-id="919d7-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="919d7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="919d7-114">-Name</span><span class="sxs-lookup"><span data-stu-id="919d7-114">-Name</span></span>
<span data-ttu-id="919d7-115">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="919d7-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="919d7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="919d7-116">-ResourceGroupName</span></span>
<span data-ttu-id="919d7-117">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="919d7-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="919d7-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="919d7-118">-Confirm</span></span>
<span data-ttu-id="919d7-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="919d7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="919d7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="919d7-120">-WhatIf</span></span>
<span data-ttu-id="919d7-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="919d7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="919d7-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="919d7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="919d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919d7-123">CommonParameters</span></span>
<span data-ttu-id="919d7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919d7-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="919d7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919d7-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="919d7-126">INPUTS</span></span>

### <span data-ttu-id="919d7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="919d7-127">System.String</span></span>

## <span data-ttu-id="919d7-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="919d7-128">OUTPUTS</span></span>

### <span data-ttu-id="919d7-129">System. void</span><span class="sxs-lookup"><span data-stu-id="919d7-129">System.Void</span></span>

## <span data-ttu-id="919d7-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="919d7-130">NOTES</span></span>
* <span data-ttu-id="919d7-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="919d7-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="919d7-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="919d7-132">RELATED LINKS</span></span>

[<span data-ttu-id="919d7-133">Satz-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="919d7-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


