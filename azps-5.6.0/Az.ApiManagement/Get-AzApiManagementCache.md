---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 53a164b2cd3421898974f7f5f1c2fd2b7ed51c21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921536"
---
# <span data-ttu-id="ff7df-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff7df-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="ff7df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff7df-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7df-103">Hier erhalten Sie die Details des Caches.</span><span class="sxs-lookup"><span data-stu-id="ff7df-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="ff7df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff7df-104">SYNTAX</span></span>

### <span data-ttu-id="ff7df-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff7df-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff7df-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff7df-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff7df-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff7df-107">DESCRIPTION</span></span>
<span data-ttu-id="ff7df-108">Hier erhalten Sie die Details des im Api-Verwaltungsdienst konfigurierten Caches.</span><span class="sxs-lookup"><span data-stu-id="ff7df-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="ff7df-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ff7df-109">EXAMPLES</span></span>

### <span data-ttu-id="ff7df-110">Beispiel 1: Alle Caches erhalten</span><span class="sxs-lookup"><span data-stu-id="ff7df-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="ff7df-111">Ruft eine Liste aller im Api-Verwaltungsdienst konfigurierten Caches ab.</span><span class="sxs-lookup"><span data-stu-id="ff7df-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="ff7df-112">Beispiel 2: Vom Bezeichner westus angegebenen Cache erhalten</span><span class="sxs-lookup"><span data-stu-id="ff7df-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="ff7df-113">Hier erhalten Sie die Details des angegebenen Caches, der für westus konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="ff7df-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="ff7df-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ff7df-114">PARAMETERS</span></span>

### <span data-ttu-id="ff7df-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="ff7df-115">-CacheId</span></span>
<span data-ttu-id="ff7df-116">Bezeichner eines Caches.</span><span class="sxs-lookup"><span data-stu-id="ff7df-116">Identifier of a cache.</span></span>
<span data-ttu-id="ff7df-117">Wenn angegeben, wird versucht, den Cache durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="ff7df-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="ff7df-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ff7df-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff7df-119">-Context</span><span class="sxs-lookup"><span data-stu-id="ff7df-119">-Context</span></span>
<span data-ttu-id="ff7df-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ff7df-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ff7df-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ff7df-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7df-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7df-122">-DefaultProfile</span></span>
<span data-ttu-id="ff7df-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff7df-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff7df-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff7df-124">-ResourceId</span></span>
<span data-ttu-id="ff7df-125">Arm Resource Identifier eines Caches.</span><span class="sxs-lookup"><span data-stu-id="ff7df-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="ff7df-126">Wenn angegeben, wird versucht, den Cache durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="ff7df-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="ff7df-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ff7df-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7df-128">CommonParameters</span></span>
<span data-ttu-id="ff7df-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff7df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7df-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff7df-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7df-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ff7df-131">INPUTS</span></span>

### <span data-ttu-id="ff7df-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ff7df-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ff7df-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ff7df-133">System.String</span></span>

## <span data-ttu-id="ff7df-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ff7df-134">OUTPUTS</span></span>

### <span data-ttu-id="ff7df-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff7df-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="ff7df-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ff7df-136">NOTES</span></span>

## <span data-ttu-id="ff7df-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ff7df-137">RELATED LINKS</span></span>

[<span data-ttu-id="ff7df-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff7df-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="ff7df-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff7df-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="ff7df-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ff7df-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
