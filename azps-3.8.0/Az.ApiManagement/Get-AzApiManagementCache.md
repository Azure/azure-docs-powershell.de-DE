---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 757332267d2db2f797bb2f7ca2a39dbb32ee06c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996644"
---
# <span data-ttu-id="ffb04-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ffb04-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="ffb04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffb04-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb04-103">Rufen Sie die Details des Caches ab.</span><span class="sxs-lookup"><span data-stu-id="ffb04-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="ffb04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffb04-104">SYNTAX</span></span>

### <span data-ttu-id="ffb04-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ffb04-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffb04-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffb04-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffb04-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffb04-107">DESCRIPTION</span></span>
<span data-ttu-id="ffb04-108">Rufen Sie die Details des im API-Verwaltungsdienst konfigurierten Caches ab.</span><span class="sxs-lookup"><span data-stu-id="ffb04-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="ffb04-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffb04-109">EXAMPLES</span></span>

### <span data-ttu-id="ffb04-110">Beispiel 1: Abrufen aller Caches</span><span class="sxs-lookup"><span data-stu-id="ffb04-110">Example 1: Get all Caches</span></span>
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

<span data-ttu-id="ffb04-111">Ruft eine Liste aller Caches ab, die im API-Verwaltungsdienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="ffb04-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="ffb04-112">Beispiel 2: Abrufen des vom Bezeichner westus angegebenen Caches</span><span class="sxs-lookup"><span data-stu-id="ffb04-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
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

<span data-ttu-id="ffb04-113">Abrufen der Details des angegebenen Caches, der für westus konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="ffb04-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="ffb04-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffb04-114">PARAMETERS</span></span>

### <span data-ttu-id="ffb04-115">-Cache-Nr</span><span class="sxs-lookup"><span data-stu-id="ffb04-115">-CacheId</span></span>
<span data-ttu-id="ffb04-116">Bezeichner eines Caches.</span><span class="sxs-lookup"><span data-stu-id="ffb04-116">Identifier of a cache.</span></span>
<span data-ttu-id="ffb04-117">Wenn angegeben, wird versucht, den Cache nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="ffb04-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="ffb04-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ffb04-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="ffb04-119">-Context</span><span class="sxs-lookup"><span data-stu-id="ffb04-119">-Context</span></span>
<span data-ttu-id="ffb04-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ffb04-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ffb04-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ffb04-121">This parameter is required.</span></span>

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

### <span data-ttu-id="ffb04-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb04-122">-DefaultProfile</span></span>
<span data-ttu-id="ffb04-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffb04-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffb04-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ffb04-124">-ResourceId</span></span>
<span data-ttu-id="ffb04-125">Arm-Ressourcenbezeichner eines Caches</span><span class="sxs-lookup"><span data-stu-id="ffb04-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="ffb04-126">Wenn angegeben, wird versucht, den Cache nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="ffb04-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="ffb04-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ffb04-127">This parameter is required.</span></span>

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

### <span data-ttu-id="ffb04-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb04-128">CommonParameters</span></span>
<span data-ttu-id="ffb04-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb04-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb04-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffb04-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb04-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffb04-131">INPUTS</span></span>

### <span data-ttu-id="ffb04-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ffb04-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ffb04-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ffb04-133">System.String</span></span>

## <span data-ttu-id="ffb04-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffb04-134">OUTPUTS</span></span>

### <span data-ttu-id="ffb04-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ffb04-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="ffb04-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffb04-136">NOTES</span></span>

## <span data-ttu-id="ffb04-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffb04-137">RELATED LINKS</span></span>

[<span data-ttu-id="ffb04-138">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ffb04-138">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="ffb04-139">Satz-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ffb04-139">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="ffb04-140">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="ffb04-140">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)