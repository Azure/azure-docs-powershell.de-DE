---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171911"
---
# <span data-ttu-id="78a7d-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="78a7d-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="78a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="78a7d-103">Abrufen von Details zur Diagnose, die auf Dienst- oder Apiebene konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="78a7d-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="78a7d-104">Diagnosefunktionen werden zum Protokollieren von Anforderungen/Antworten vom Api-Verwaltungsgateway verwendet.</span><span class="sxs-lookup"><span data-stu-id="78a7d-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="78a7d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78a7d-105">SYNTAX</span></span>

### <span data-ttu-id="78a7d-106">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="78a7d-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78a7d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a7d-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78a7d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78a7d-108">DESCRIPTION</span></span>
<span data-ttu-id="78a7d-109">Die **Get-AzApiManagementDiagnostic** ruft Details der im Api-Verwaltungsdienst konfigurierten Diagnose in einem bestimmten Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="78a7d-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="78a7d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78a7d-110">EXAMPLES</span></span>

### <span data-ttu-id="78a7d-111">Beispiel 1: Alle Diagnosefunktionen werden im Mandantenbereich konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="78a7d-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="78a7d-112">Mit diesem Befehl werden alle Diagnosen im Api-Verwaltungsdienst konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="78a7d-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="78a7d-113">Beispiel 2: Abrufen aller im Bereich "API" konfigurierten Diagnosen</span><span class="sxs-lookup"><span data-stu-id="78a7d-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="78a7d-114">Mit diesem Befehl werden alle Diagnosen im Bereich `echo-api` "API" konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="78a7d-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="78a7d-115">Beispiel 3: Abrufen der API-Bereichsdiagnose, die durch eine ID angegeben ist</span><span class="sxs-lookup"><span data-stu-id="78a7d-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="78a7d-116">Mit diesem Befehl wird `applicationinsights` die Diagnose in api `echo-api` konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="78a7d-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="78a7d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78a7d-117">PARAMETERS</span></span>

### <span data-ttu-id="78a7d-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="78a7d-118">-ApiId</span></span>
<span data-ttu-id="78a7d-119">Bezeichner einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="78a7d-119">Identifier of existing API.</span></span>
<span data-ttu-id="78a7d-120">Wenn diese Angabe angegeben wird, wird die DIAGNOSE im API-Bereich zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="78a7d-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="78a7d-121">Diese Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78a7d-121">This parameters is required.</span></span>

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

### <span data-ttu-id="78a7d-122">-Context</span><span class="sxs-lookup"><span data-stu-id="78a7d-122">-Context</span></span>
<span data-ttu-id="78a7d-123">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="78a7d-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="78a7d-124">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78a7d-124">This parameter is required.</span></span>

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

### <span data-ttu-id="78a7d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a7d-125">-DefaultProfile</span></span>
<span data-ttu-id="78a7d-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78a7d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78a7d-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="78a7d-127">-DiagnosticId</span></span>
<span data-ttu-id="78a7d-128">Bezeichner eines vorhandenen Diagnosetools.</span><span class="sxs-lookup"><span data-stu-id="78a7d-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="78a7d-129">Wenn diese Angabe angegeben wird, wird eine Richtlinie für den Produktbereich zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="78a7d-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="78a7d-130">Diese Parameter sind optional.</span><span class="sxs-lookup"><span data-stu-id="78a7d-130">This parameters is optional.</span></span>

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

### <span data-ttu-id="78a7d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78a7d-131">-ResourceId</span></span>
<span data-ttu-id="78a7d-132">Arm Resource Identifier eines Diagnose- oder Api-Diagnose-</span><span class="sxs-lookup"><span data-stu-id="78a7d-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="78a7d-133">Wenn angegeben, wird versucht, die Diagnose nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="78a7d-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="78a7d-134">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78a7d-134">This parameter is required.</span></span>

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

### <span data-ttu-id="78a7d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a7d-135">CommonParameters</span></span>
<span data-ttu-id="78a7d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a7d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a7d-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78a7d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a7d-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78a7d-138">INPUTS</span></span>

### <span data-ttu-id="78a7d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="78a7d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="78a7d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="78a7d-140">System.String</span></span>

## <span data-ttu-id="78a7d-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78a7d-141">OUTPUTS</span></span>

### <span data-ttu-id="78a7d-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="78a7d-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="78a7d-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="78a7d-143">NOTES</span></span>

## <span data-ttu-id="78a7d-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="78a7d-144">RELATED LINKS</span></span>
