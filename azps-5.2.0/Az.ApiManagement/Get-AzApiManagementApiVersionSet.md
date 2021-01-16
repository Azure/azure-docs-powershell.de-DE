---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: e6b9122481e5e506fc02a13a61b7ebeb71372e96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366160"
---
# <span data-ttu-id="3ff32-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3ff32-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="3ff32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff32-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff32-103">Details zu den API-Versionssätzen abrufen</span><span class="sxs-lookup"><span data-stu-id="3ff32-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="3ff32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ff32-104">SYNTAX</span></span>

### <span data-ttu-id="3ff32-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ff32-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff32-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff32-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ff32-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ff32-107">DESCRIPTION</span></span>
<span data-ttu-id="3ff32-108">Das **Cmdlet "Get-AzApiManagementApiVersionSet"** ruft die Details der in einem API-Verwaltungskontext konfigurierten API-Versionssätze ab.</span><span class="sxs-lookup"><span data-stu-id="3ff32-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="3ff32-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ff32-109">EXAMPLES</span></span>

### <span data-ttu-id="3ff32-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ff32-110">Example 1</span></span>

### <span data-ttu-id="3ff32-111">Beispiel 2: Abrufen aller API-Versionssätze</span><span class="sxs-lookup"><span data-stu-id="3ff32-111">Example 2: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="3ff32-112">Dieser Befehl ruft alle API-Versionssätze für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="3ff32-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="3ff32-113">Beispiel 3: Abrufen einer NACH-ID festgelegten API-Version</span><span class="sxs-lookup"><span data-stu-id="3ff32-113">Example 3: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="3ff32-114">Dieser Befehl ruft den API-Versionssatz mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="3ff32-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="3ff32-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ff32-115">PARAMETERS</span></span>

### <span data-ttu-id="3ff32-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="3ff32-116">-ApiVersionSetId</span></span>
<span data-ttu-id="3ff32-117">API-ID, nach der sie suchen soll.</span><span class="sxs-lookup"><span data-stu-id="3ff32-117">API identifier to look for.</span></span>
<span data-ttu-id="3ff32-118">Wenn diese Angabe angegeben wird, wird versucht, die API nach der ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3ff32-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="3ff32-119">-Context</span><span class="sxs-lookup"><span data-stu-id="3ff32-119">-Context</span></span>
<span data-ttu-id="3ff32-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3ff32-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3ff32-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ff32-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ff32-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff32-122">-DefaultProfile</span></span>
<span data-ttu-id="3ff32-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ff32-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ff32-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff32-124">-ResourceId</span></span>
<span data-ttu-id="3ff32-125">Arm Resource Identifier des ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="3ff32-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="3ff32-126">Bei Angabe wird versucht, "apiVersionSet" durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="3ff32-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="3ff32-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ff32-127">This parameter is required.</span></span>

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

### <span data-ttu-id="3ff32-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff32-128">CommonParameters</span></span>
<span data-ttu-id="3ff32-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff32-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff32-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ff32-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff32-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ff32-131">INPUTS</span></span>

### <span data-ttu-id="3ff32-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3ff32-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3ff32-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3ff32-133">System.String</span></span>

## <span data-ttu-id="3ff32-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ff32-134">OUTPUTS</span></span>

### <span data-ttu-id="3ff32-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3ff32-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="3ff32-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ff32-136">NOTES</span></span>

## <span data-ttu-id="3ff32-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ff32-137">RELATED LINKS</span></span>

[<span data-ttu-id="3ff32-138">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3ff32-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="3ff32-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="3ff32-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="3ff32-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3ff32-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
