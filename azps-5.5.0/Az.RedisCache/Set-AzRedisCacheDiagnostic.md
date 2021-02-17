---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153785"
---
# <span data-ttu-id="25fc3-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="25fc3-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="25fc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="25fc3-103">Ermöglicht Diagnosen für einen Azure Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="25fc3-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="25fc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25fc3-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25fc3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="25fc3-106">Das **Cmdlet "Set-AzRedisCacheDiagnostic"** ermöglicht die Diagnose für einen Azure Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="25fc3-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="25fc3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="25fc3-108">Beispiel 1: Aktivieren der Diagnose</span><span class="sxs-lookup"><span data-stu-id="25fc3-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="25fc3-109">Dieser Befehl ermöglicht die Diagnose für einen Azure Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="25fc3-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="25fc3-110">Dieser Befehl aktiviert die Diagnose oder aktualisiert das Speicherkonto für alle Azure Redis Caches in derselben Region für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25fc3-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="25fc3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25fc3-111">PARAMETERS</span></span>

### <span data-ttu-id="25fc3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fc3-112">-DefaultProfile</span></span>
<span data-ttu-id="25fc3-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25fc3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25fc3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="25fc3-114">-Name</span></span>
<span data-ttu-id="25fc3-115">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="25fc3-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="25fc3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25fc3-116">-ResourceGroupName</span></span>
<span data-ttu-id="25fc3-117">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="25fc3-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="25fc3-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="25fc3-118">-StorageAccountId</span></span>
<span data-ttu-id="25fc3-119">Gibt die Ressourcen-ID des Speicherkontos an, das zum Speichern der Diagnosedaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="25fc3-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="25fc3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25fc3-120">-Confirm</span></span>
<span data-ttu-id="25fc3-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25fc3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25fc3-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="25fc3-122">-WhatIf</span></span>
<span data-ttu-id="25fc3-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25fc3-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25fc3-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25fc3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25fc3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fc3-125">CommonParameters</span></span>
<span data-ttu-id="25fc3-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25fc3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fc3-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25fc3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fc3-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25fc3-128">INPUTS</span></span>

### <span data-ttu-id="25fc3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="25fc3-129">System.String</span></span>

## <span data-ttu-id="25fc3-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25fc3-130">OUTPUTS</span></span>

### <span data-ttu-id="25fc3-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="25fc3-131">System.Void</span></span>

## <span data-ttu-id="25fc3-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25fc3-132">NOTES</span></span>
* <span data-ttu-id="25fc3-133">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="25fc3-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="25fc3-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25fc3-134">RELATED LINKS</span></span>

[<span data-ttu-id="25fc3-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="25fc3-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


