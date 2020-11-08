---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 2b87f3b0716c95f27a78c2a0f59168f133ade015
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996649"
---
# <span data-ttu-id="debf3-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="debf3-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="debf3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="debf3-102">SYNOPSIS</span></span>
<span data-ttu-id="debf3-103">Abrufen der Details der API-Versionssätze</span><span class="sxs-lookup"><span data-stu-id="debf3-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="debf3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="debf3-104">SYNTAX</span></span>

### <span data-ttu-id="debf3-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="debf3-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="debf3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="debf3-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="debf3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="debf3-107">DESCRIPTION</span></span>
<span data-ttu-id="debf3-108">Das Cmdlet " **Get-AzApiManagementApiVersionSet** " Ruft die Details der API-Versionssätze ab, die in einem API-Verwaltungskontext konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="debf3-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="debf3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="debf3-109">EXAMPLES</span></span>

### <span data-ttu-id="debf3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="debf3-110">Example 1</span></span>

### <span data-ttu-id="debf3-111">Beispiel 1: Abrufen aller API-Versionssätze</span><span class="sxs-lookup"><span data-stu-id="debf3-111">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="debf3-112">Dieser Befehl ruft alle API-Versionssätze für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="debf3-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="debf3-113">Beispiel 2: Abrufen einer API-Version, die von ID gesetzt wird</span><span class="sxs-lookup"><span data-stu-id="debf3-113">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="debf3-114">Dieser Befehl ruft die API-Version ab, die mit der angegebenen ID festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="debf3-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="debf3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="debf3-115">PARAMETERS</span></span>

### <span data-ttu-id="debf3-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="debf3-116">-ApiVersionSetId</span></span>
<span data-ttu-id="debf3-117">Der API-Bezeichner, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="debf3-117">API identifier to look for.</span></span>
<span data-ttu-id="debf3-118">Wenn angegeben, wird versucht, die API mithilfe der ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="debf3-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="debf3-119">-Context</span><span class="sxs-lookup"><span data-stu-id="debf3-119">-Context</span></span>
<span data-ttu-id="debf3-120">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="debf3-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="debf3-121">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="debf3-121">This parameter is required.</span></span>

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

### <span data-ttu-id="debf3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debf3-122">-DefaultProfile</span></span>
<span data-ttu-id="debf3-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="debf3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="debf3-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="debf3-124">-ResourceId</span></span>
<span data-ttu-id="debf3-125">Arm-Ressourcenbezeichner des ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="debf3-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="debf3-126">Wenn angegeben, wird versucht, apiVersionSet anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="debf3-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="debf3-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="debf3-127">This parameter is required.</span></span>

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

### <span data-ttu-id="debf3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debf3-128">CommonParameters</span></span>
<span data-ttu-id="debf3-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="debf3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debf3-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="debf3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debf3-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="debf3-131">INPUTS</span></span>

### <span data-ttu-id="debf3-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="debf3-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="debf3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="debf3-133">System.String</span></span>

## <span data-ttu-id="debf3-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="debf3-134">OUTPUTS</span></span>

### <span data-ttu-id="debf3-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="debf3-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="debf3-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="debf3-136">NOTES</span></span>

## <span data-ttu-id="debf3-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="debf3-137">RELATED LINKS</span></span>

[<span data-ttu-id="debf3-138">Neu – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="debf3-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="debf3-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="debf3-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="debf3-140">Satz-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="debf3-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)
