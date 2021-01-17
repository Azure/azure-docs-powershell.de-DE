---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306835"
---
# <span data-ttu-id="e1a24-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="e1a24-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="e1a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1a24-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a24-103">Erstellt eine neue Überarbeitung einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="e1a24-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="e1a24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1a24-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1a24-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1a24-105">DESCRIPTION</span></span>

<span data-ttu-id="e1a24-106">Das **Cmdlet "New-AzApiManagementApiRevision"** erstellt eine API-Revision für eine vorhandene API im API-Verwaltungskontext.</span><span class="sxs-lookup"><span data-stu-id="e1a24-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="e1a24-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1a24-107">EXAMPLES</span></span>

### <span data-ttu-id="e1a24-108">Beispiel 1: Erstellen einer leeren API-Überarbeitung für eine API</span><span class="sxs-lookup"><span data-stu-id="e1a24-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="e1a24-109">Mit diesem Befehl wird eine API-Überarbeitung `2` der `echo-api` API erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1a24-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="e1a24-110">Beispiel 2: Erstellen einer API-Überarbeitung aus einer vorhandenen API und Kopieren aller Vorgänge, Tags und Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e1a24-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="e1a24-111">Mit diesem Befehl wird eine API-Überarbeitung `5` der `echo-api` API erstellt.</span><span class="sxs-lookup"><span data-stu-id="e1a24-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="e1a24-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1a24-112">PARAMETERS</span></span>

### <span data-ttu-id="e1a24-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e1a24-113">-ApiId</span></span>
<span data-ttu-id="e1a24-114">Bezeichner für API, deren Revision erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1a24-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="e1a24-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e1a24-115">-ApiRevision</span></span>
<span data-ttu-id="e1a24-116">Revisions-ID der API.</span><span class="sxs-lookup"><span data-stu-id="e1a24-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="e1a24-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="e1a24-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="e1a24-118">Api-Revisionsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="e1a24-118">Api Revision Description.</span></span> <span data-ttu-id="e1a24-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e1a24-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e1a24-120">-Context</span><span class="sxs-lookup"><span data-stu-id="e1a24-120">-Context</span></span>
<span data-ttu-id="e1a24-121">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e1a24-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e1a24-122">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e1a24-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1a24-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a24-123">-DefaultProfile</span></span>
<span data-ttu-id="e1a24-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1a24-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1a24-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="e1a24-125">-ServiceUrl</span></span>
<span data-ttu-id="e1a24-126">Eine URL des Webdiensts, der die API im Back-End-Dienst verfügbar gibt.</span><span class="sxs-lookup"><span data-stu-id="e1a24-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="e1a24-127">Diese URL wird nur von Azure API Management verwendet und nicht öffentlich gemacht.</span><span class="sxs-lookup"><span data-stu-id="e1a24-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="e1a24-128">Muss 1 bis 2.000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="e1a24-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="e1a24-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e1a24-129">This parameter is required.</span></span>

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

### <span data-ttu-id="e1a24-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="e1a24-130">-SourceApiRevision</span></span>
<span data-ttu-id="e1a24-131">Api-Revisions-ID der Quell-API.</span><span class="sxs-lookup"><span data-stu-id="e1a24-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="e1a24-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e1a24-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="e1a24-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1a24-133">-Confirm</span></span>
<span data-ttu-id="e1a24-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1a24-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a24-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e1a24-135">-WhatIf</span></span>
<span data-ttu-id="e1a24-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1a24-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1a24-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1a24-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a24-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a24-138">CommonParameters</span></span>
<span data-ttu-id="e1a24-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1a24-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a24-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1a24-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a24-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1a24-141">INPUTS</span></span>

### <span data-ttu-id="e1a24-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e1a24-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e1a24-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e1a24-143">System.String</span></span>

## <span data-ttu-id="e1a24-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1a24-144">OUTPUTS</span></span>

### <span data-ttu-id="e1a24-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1a24-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e1a24-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1a24-146">NOTES</span></span>

## <span data-ttu-id="e1a24-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1a24-147">RELATED LINKS</span></span>

[<span data-ttu-id="e1a24-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1a24-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="e1a24-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1a24-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e1a24-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1a24-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
