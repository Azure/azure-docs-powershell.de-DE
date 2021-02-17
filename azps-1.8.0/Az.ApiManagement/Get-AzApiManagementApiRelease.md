---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 4f9e917f17037e5f47b52501007da5556bde1187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401078"
---
# <span data-ttu-id="c2bd8-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c2bd8-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="c2bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="c2bd8-103">Abrufen der API-Version.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-103">Get the API Release.</span></span>

## <span data-ttu-id="c2bd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2bd8-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2bd8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="c2bd8-106">Das **Cmdlet "Get-AzApiManagementApiRelease"** ruft mindestens eine Version der Azure API Management API ab.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="c2bd8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2bd8-107">EXAMPLES</span></span>

### <span data-ttu-id="c2bd8-108">Beispiel 1: Abrufen aller Versionen der API</span><span class="sxs-lookup"><span data-stu-id="c2bd8-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="c2bd8-109">Dieser Befehl ruft alle Versionen der API für `echo-api` den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="c2bd8-110">Beispiel 2: Abrufen der Versionsinformationen zu einer bestimmten API-Version</span><span class="sxs-lookup"><span data-stu-id="c2bd8-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="c2bd8-111">Dieser Befehl ruft die Versionsinformationen einer bestimmten API mit der angegebenen releaseId ab.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="c2bd8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2bd8-112">PARAMETERS</span></span>

### <span data-ttu-id="c2bd8-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c2bd8-113">-ApiId</span></span>
<span data-ttu-id="c2bd8-114">API-ID, nach der sie suchen soll.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-114">API identifier to look for.</span></span>
<span data-ttu-id="c2bd8-115">Wenn diese Angabe angegeben wird, wird versucht, die API nach der ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="c2bd8-116">-Context</span><span class="sxs-lookup"><span data-stu-id="c2bd8-116">-Context</span></span>
<span data-ttu-id="c2bd8-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c2bd8-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c2bd8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2bd8-119">-DefaultProfile</span></span>
<span data-ttu-id="c2bd8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2bd8-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="c2bd8-121">-ReleaseId</span></span>
<span data-ttu-id="c2bd8-122">Der Bezeichner von Release.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="c2bd8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2bd8-123">CommonParameters</span></span>
<span data-ttu-id="c2bd8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2bd8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2bd8-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2bd8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2bd8-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2bd8-126">INPUTS</span></span>

### <span data-ttu-id="c2bd8-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c2bd8-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c2bd8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c2bd8-128">System.String</span></span>

## <span data-ttu-id="c2bd8-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2bd8-129">OUTPUTS</span></span>

### <span data-ttu-id="c2bd8-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c2bd8-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c2bd8-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c2bd8-131">NOTES</span></span>

## <span data-ttu-id="c2bd8-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c2bd8-132">RELATED LINKS</span></span>

[<span data-ttu-id="c2bd8-133">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c2bd8-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="c2bd8-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c2bd8-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="c2bd8-135">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c2bd8-135">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)