---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: ea7be233673bc5b3424c5f1d3eae793c3573641a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935899"
---
# <span data-ttu-id="d4f1d-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d4f1d-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="d4f1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f1d-103">Holen Sie sich die API-Version.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-103">Get the API Release.</span></span>

## <span data-ttu-id="d4f1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4f1d-104">SYNTAX</span></span>

### <span data-ttu-id="d4f1d-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4f1d-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4f1d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4f1d-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4f1d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4f1d-107">DESCRIPTION</span></span>
<span data-ttu-id="d4f1d-108">Das **Get-AzApiManagementApiRelease-Cmdlet** ruft eine oder mehrere Versionen der Azure API-Verwaltungs-API ab.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="d4f1d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4f1d-109">EXAMPLES</span></span>

### <span data-ttu-id="d4f1d-110">Beispiel 1: Abrufen aller Versionen der API</span><span class="sxs-lookup"><span data-stu-id="d4f1d-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="d4f1d-111">Dieser Befehl ruft alle Versionen der `echo-api` API für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="d4f1d-112">Beispiel 2: Abrufen der Versionsinformationen der jeweiligen API-Version</span><span class="sxs-lookup"><span data-stu-id="d4f1d-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="d4f1d-113">Dieser Befehl ruft die Versionsinformationen einer bestimmten API mit der angegebenen releaseId ab.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="d4f1d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d4f1d-114">PARAMETERS</span></span>

### <span data-ttu-id="d4f1d-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d4f1d-115">-ApiId</span></span>
<span data-ttu-id="d4f1d-116">API-Bezeichner, nach dem Sie suchen können.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-116">API identifier to look for.</span></span>
<span data-ttu-id="d4f1d-117">Wenn angegeben, wird versucht, die API über die ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="d4f1d-118">-Context</span><span class="sxs-lookup"><span data-stu-id="d4f1d-118">-Context</span></span>
<span data-ttu-id="d4f1d-119">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d4f1d-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-120">This parameter is required.</span></span>

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

### <span data-ttu-id="d4f1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f1d-121">-DefaultProfile</span></span>
<span data-ttu-id="d4f1d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4f1d-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="d4f1d-123">-ReleaseId</span></span>
<span data-ttu-id="d4f1d-124">Der Bezeichner der Version.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="d4f1d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4f1d-125">-ResourceId</span></span>
<span data-ttu-id="d4f1d-126">Arm Resource Identifier einer Api Release.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="d4f1d-127">Wenn angegeben, wird versucht, die API-Version durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="d4f1d-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-128">This parameter is required.</span></span>

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

### <span data-ttu-id="d4f1d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f1d-129">CommonParameters</span></span>
<span data-ttu-id="d4f1d-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4f1d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f1d-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4f1d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f1d-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4f1d-132">INPUTS</span></span>

### <span data-ttu-id="d4f1d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d4f1d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d4f1d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d4f1d-134">System.String</span></span>

## <span data-ttu-id="d4f1d-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4f1d-135">OUTPUTS</span></span>

### <span data-ttu-id="d4f1d-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d4f1d-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="d4f1d-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d4f1d-137">NOTES</span></span>

## <span data-ttu-id="d4f1d-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d4f1d-138">RELATED LINKS</span></span>

[<span data-ttu-id="d4f1d-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d4f1d-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="d4f1d-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d4f1d-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="d4f1d-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d4f1d-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)