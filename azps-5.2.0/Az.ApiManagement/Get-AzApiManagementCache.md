---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: fee978a1500c0fc472ec8015a3e8dbbbdc8015bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294640"
---
# <span data-ttu-id="a1a54-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a1a54-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="a1a54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1a54-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a54-103">Hier finden Sie die Details des Caches.</span><span class="sxs-lookup"><span data-stu-id="a1a54-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="a1a54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1a54-104">SYNTAX</span></span>

### <span data-ttu-id="a1a54-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1a54-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1a54-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1a54-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1a54-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1a54-107">DESCRIPTION</span></span>
<span data-ttu-id="a1a54-108">Erfahren Sie mehr über den im Api-Verwaltungsdienst konfigurierten Cache.</span><span class="sxs-lookup"><span data-stu-id="a1a54-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="a1a54-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a1a54-109">EXAMPLES</span></span>

### <span data-ttu-id="a1a54-110">Beispiel 1: Alle Caches erhalten</span><span class="sxs-lookup"><span data-stu-id="a1a54-110">Example 1: Get all Caches</span></span>
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

<span data-ttu-id="a1a54-111">Ruft eine Liste aller im Api-Verwaltungsdienst konfigurierten Caches ab.</span><span class="sxs-lookup"><span data-stu-id="a1a54-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="a1a54-112">Beispiel 2: Den Cache erhalten, der durch den Bezeichner "westus" angegeben wurde</span><span class="sxs-lookup"><span data-stu-id="a1a54-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
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

<span data-ttu-id="a1a54-113">Details zum angegebenen Cache, der für WestUs konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="a1a54-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="a1a54-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1a54-114">PARAMETERS</span></span>

### <span data-ttu-id="a1a54-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="a1a54-115">-CacheId</span></span>
<span data-ttu-id="a1a54-116">Bezeichner eines Caches.</span><span class="sxs-lookup"><span data-stu-id="a1a54-116">Identifier of a cache.</span></span>
<span data-ttu-id="a1a54-117">Wenn diese Angabe angegeben ist, wird versucht, den Cache nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="a1a54-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="a1a54-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a1a54-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1a54-119">-Context</span><span class="sxs-lookup"><span data-stu-id="a1a54-119">-Context</span></span>
<span data-ttu-id="a1a54-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a1a54-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a1a54-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1a54-121">This parameter is required.</span></span>

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

### <span data-ttu-id="a1a54-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a54-122">-DefaultProfile</span></span>
<span data-ttu-id="a1a54-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1a54-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1a54-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1a54-124">-ResourceId</span></span>
<span data-ttu-id="a1a54-125">Arm Resource Identifier eines Caches.</span><span class="sxs-lookup"><span data-stu-id="a1a54-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="a1a54-126">Wenn diese Angabe angegeben ist, wird versucht, den Cache nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="a1a54-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="a1a54-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1a54-127">This parameter is required.</span></span>

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

### <span data-ttu-id="a1a54-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a54-128">CommonParameters</span></span>
<span data-ttu-id="a1a54-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a54-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a54-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1a54-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a54-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a1a54-131">INPUTS</span></span>

### <span data-ttu-id="a1a54-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1a54-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1a54-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a1a54-133">System.String</span></span>

## <span data-ttu-id="a1a54-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a1a54-134">OUTPUTS</span></span>

### <span data-ttu-id="a1a54-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a1a54-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="a1a54-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a1a54-136">NOTES</span></span>

## <span data-ttu-id="a1a54-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a1a54-137">RELATED LINKS</span></span>

[<span data-ttu-id="a1a54-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a1a54-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="a1a54-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a1a54-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="a1a54-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a1a54-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
