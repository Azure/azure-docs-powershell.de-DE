---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503965"
---
# <span data-ttu-id="cabec-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cabec-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="cabec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cabec-102">SYNOPSIS</span></span>
<span data-ttu-id="cabec-103">Aktiviert die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="cabec-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cabec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cabec-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cabec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cabec-105">DESCRIPTION</span></span>
<span data-ttu-id="cabec-106">Das Cmdlet " **Satz-AzureRmRedisCacheDiagnostics** " ermöglicht die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="cabec-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="cabec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cabec-107">EXAMPLES</span></span>

### <span data-ttu-id="cabec-108">Beispiel 1: Aktivieren der Diagnose</span><span class="sxs-lookup"><span data-stu-id="cabec-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="cabec-109">Dieser Befehl aktiviert die Diagnose für einen Azure-a-a-Cache.</span><span class="sxs-lookup"><span data-stu-id="cabec-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="cabec-110">Mit diesem Befehl wird die Diagnose aktiviert, oder das Speicherkonto für alle Azure-a/a-Caches in der gleichen Region für das Abonnement wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cabec-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="cabec-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cabec-111">PARAMETERS</span></span>

### <span data-ttu-id="cabec-112">-Name</span><span class="sxs-lookup"><span data-stu-id="cabec-112">-Name</span></span>
<span data-ttu-id="cabec-113">Gibt den Namen des Caches an.</span><span class="sxs-lookup"><span data-stu-id="cabec-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="cabec-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cabec-114">-ResourceGroupName</span></span>
<span data-ttu-id="cabec-115">Gibt den Namen der Ressourcengruppe an, die den Cache enthält.</span><span class="sxs-lookup"><span data-stu-id="cabec-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="cabec-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cabec-116">-StorageAccountId</span></span>
<span data-ttu-id="cabec-117">Gibt die Ressourcen-ID des speicherkontos an, mit dem die Diagnosedaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="cabec-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="cabec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabec-118">-DefaultProfile</span></span>
<span data-ttu-id="cabec-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cabec-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cabec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabec-120">CommonParameters</span></span>
<span data-ttu-id="cabec-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabec-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cabec-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabec-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cabec-123">INPUTS</span></span>

### <span data-ttu-id="cabec-124">Keine</span><span class="sxs-lookup"><span data-stu-id="cabec-124">None</span></span>

## <span data-ttu-id="cabec-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cabec-125">OUTPUTS</span></span>

### <span data-ttu-id="cabec-126">Void</span><span class="sxs-lookup"><span data-stu-id="cabec-126">Void</span></span>

## <span data-ttu-id="cabec-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="cabec-127">NOTES</span></span>
* <span data-ttu-id="cabec-128">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website</span><span class="sxs-lookup"><span data-stu-id="cabec-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="cabec-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cabec-129">RELATED LINKS</span></span>

[<span data-ttu-id="cabec-130">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cabec-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


