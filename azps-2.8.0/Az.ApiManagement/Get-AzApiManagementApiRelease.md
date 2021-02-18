---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: bb27324c2c8524f36d9f3362dee8968fbfb0cc8c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409782"
---
# <span data-ttu-id="8da42-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8da42-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="8da42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da42-102">SYNOPSIS</span></span>
<span data-ttu-id="8da42-103">Abrufen der API-Version.</span><span class="sxs-lookup"><span data-stu-id="8da42-103">Get the API Release.</span></span>

## <span data-ttu-id="8da42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8da42-104">SYNTAX</span></span>

### <span data-ttu-id="8da42-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8da42-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8da42-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da42-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8da42-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8da42-107">DESCRIPTION</span></span>
<span data-ttu-id="8da42-108">Das **Cmdlet "Get-AzApiManagementApiRelease"** ruft mindestens eine Version der Azure API Management API ab.</span><span class="sxs-lookup"><span data-stu-id="8da42-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="8da42-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8da42-109">EXAMPLES</span></span>

### <span data-ttu-id="8da42-110">Beispiel 1: Abrufen aller Versionen der API</span><span class="sxs-lookup"><span data-stu-id="8da42-110">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contoso
```

<span data-ttu-id="8da42-111">Dieser Befehl ruft alle Versionen der API für `echo-api` den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="8da42-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="8da42-112">Beispiel 2: Abrufen der Versionsinformationen zu einer bestimmten API-Version</span><span class="sxs-lookup"><span data-stu-id="8da42-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="8da42-113">Dieser Befehl ruft die Versionsinformationen einer bestimmten API mit der angegebenen releaseId ab.</span><span class="sxs-lookup"><span data-stu-id="8da42-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="8da42-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8da42-114">PARAMETERS</span></span>

### <span data-ttu-id="8da42-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8da42-115">-ApiId</span></span>
<span data-ttu-id="8da42-116">API-ID, nach der sie suchen soll.</span><span class="sxs-lookup"><span data-stu-id="8da42-116">API identifier to look for.</span></span>
<span data-ttu-id="8da42-117">Wenn diese Angabe angegeben wird, wird versucht, die API nach der ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8da42-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da42-118">-Context</span><span class="sxs-lookup"><span data-stu-id="8da42-118">-Context</span></span>
<span data-ttu-id="8da42-119">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8da42-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8da42-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8da42-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8da42-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da42-121">-DefaultProfile</span></span>
<span data-ttu-id="8da42-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8da42-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8da42-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="8da42-123">-ReleaseId</span></span>
<span data-ttu-id="8da42-124">Der Bezeichner von Release.</span><span class="sxs-lookup"><span data-stu-id="8da42-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8da42-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8da42-125">-ResourceId</span></span>
<span data-ttu-id="8da42-126">Arm Resource Identifier einer API-Version.</span><span class="sxs-lookup"><span data-stu-id="8da42-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="8da42-127">Wenn angegeben, wird versucht, die API Release durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="8da42-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="8da42-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8da42-128">This parameter is required.</span></span>

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

### <span data-ttu-id="8da42-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da42-129">CommonParameters</span></span>
<span data-ttu-id="8da42-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da42-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da42-131">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8da42-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da42-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8da42-132">INPUTS</span></span>

### <span data-ttu-id="8da42-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8da42-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8da42-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8da42-134">System.String</span></span>

## <span data-ttu-id="8da42-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8da42-135">OUTPUTS</span></span>

### <span data-ttu-id="8da42-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8da42-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="8da42-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8da42-137">NOTES</span></span>

## <span data-ttu-id="8da42-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8da42-138">RELATED LINKS</span></span>

[<span data-ttu-id="8da42-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8da42-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="8da42-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8da42-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="8da42-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="8da42-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)