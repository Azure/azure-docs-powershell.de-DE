---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 16fea88f5a5a1ad8a0e39f62b26d918ca7a64dbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650397"
---
# <span data-ttu-id="d7e50-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d7e50-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="d7e50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7e50-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e50-103">Abrufen der Details der API-Versionssätze</span><span class="sxs-lookup"><span data-stu-id="d7e50-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="d7e50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7e50-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7e50-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7e50-105">DESCRIPTION</span></span>
<span data-ttu-id="d7e50-106">Das Cmdlet " **Get-AzApiManagementApiVersionSet** " Ruft die Details der API-Versionssätze ab, die in einem API-Verwaltungskontext konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="d7e50-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="d7e50-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7e50-107">EXAMPLES</span></span>

### <span data-ttu-id="d7e50-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d7e50-108">Example 1</span></span>

### <span data-ttu-id="d7e50-109">Beispiel 1: Abrufen aller API-Versionssätze</span><span class="sxs-lookup"><span data-stu-id="d7e50-109">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="d7e50-110">Dieser Befehl ruft alle API-Versionssätze für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="d7e50-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="d7e50-111">Beispiel 2: Abrufen einer API-Version, die von ID gesetzt wird</span><span class="sxs-lookup"><span data-stu-id="d7e50-111">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="d7e50-112">Dieser Befehl ruft die API-Version ab, die mit der angegebenen ID festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d7e50-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="d7e50-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7e50-113">PARAMETERS</span></span>

### <span data-ttu-id="d7e50-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="d7e50-114">-ApiVersionSetId</span></span>
<span data-ttu-id="d7e50-115">Der API-Bezeichner, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7e50-115">API identifier to look for.</span></span>
<span data-ttu-id="d7e50-116">Wenn angegeben, wird versucht, die API mithilfe der ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d7e50-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="d7e50-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d7e50-117">-Context</span></span>
<span data-ttu-id="d7e50-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d7e50-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d7e50-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d7e50-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e50-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e50-120">-DefaultProfile</span></span>
<span data-ttu-id="d7e50-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7e50-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7e50-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e50-122">CommonParameters</span></span>
<span data-ttu-id="d7e50-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e50-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e50-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e50-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e50-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7e50-125">INPUTS</span></span>

### <span data-ttu-id="d7e50-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d7e50-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7e50-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d7e50-127">System.String</span></span>

## <span data-ttu-id="d7e50-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7e50-128">OUTPUTS</span></span>

### <span data-ttu-id="d7e50-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d7e50-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="d7e50-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7e50-130">NOTES</span></span>

## <span data-ttu-id="d7e50-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7e50-131">RELATED LINKS</span></span>

[<span data-ttu-id="d7e50-132">Neu – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d7e50-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="d7e50-133">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="d7e50-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="d7e50-134">Satz-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d7e50-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)
