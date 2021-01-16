---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382457"
---
# <span data-ttu-id="0d80e-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0d80e-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="0d80e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d80e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d80e-103">Erstellt einen API-Verwaltungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="0d80e-103">Creates an API management operation.</span></span>

## <span data-ttu-id="0d80e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d80e-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d80e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d80e-105">DESCRIPTION</span></span>
<span data-ttu-id="0d80e-106">Das **Cmdlet "New-AzApiManagementOperation"** erstellt einen API-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0d80e-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="0d80e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d80e-107">EXAMPLES</span></span>

### <span data-ttu-id="0d80e-108">Beispiel 1: Erstellen eines API-Verwaltungsvorgangs</span><span class="sxs-lookup"><span data-stu-id="0d80e-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="0d80e-109">Dieser Befehl erstellt einen API-Verwaltungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="0d80e-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="0d80e-110">Beispiel 2: Erstellen eines API-Verwaltungsvorgangs mit Anforderungs- und Antwortdetails</span><span class="sxs-lookup"><span data-stu-id="0d80e-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="0d80e-111">In diesem Beispiel wird ein API-Verwaltungsvorgang mit Anforderungs- und Antwortdetails erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d80e-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="0d80e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d80e-112">PARAMETERS</span></span>

### <span data-ttu-id="0d80e-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0d80e-113">-ApiId</span></span>
<span data-ttu-id="0d80e-114">Gibt den Bezeichner des API-Verwaltungsvorgangs an.</span><span class="sxs-lookup"><span data-stu-id="0d80e-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="0d80e-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="0d80e-115">-ApiRevision</span></span>
<span data-ttu-id="0d80e-116">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="0d80e-116">Identifier of API Revision.</span></span> <span data-ttu-id="0d80e-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0d80e-117">This parameter is optional.</span></span> <span data-ttu-id="0d80e-118">Wenn dieser Vorgang nicht angegeben wird, wird er an die derzeit aktive API-Überarbeitung angefügt.</span><span class="sxs-lookup"><span data-stu-id="0d80e-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="0d80e-119">-Context</span><span class="sxs-lookup"><span data-stu-id="0d80e-119">-Context</span></span>
<span data-ttu-id="0d80e-120">Gibt die Instanz des **"PsApiManagementContext"-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="0d80e-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0d80e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d80e-121">-DefaultProfile</span></span>
<span data-ttu-id="0d80e-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d80e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d80e-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d80e-123">-Description</span></span>
<span data-ttu-id="0d80e-124">Gibt die Beschreibung des neuen API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="0d80e-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="0d80e-125">-Methode</span><span class="sxs-lookup"><span data-stu-id="0d80e-125">-Method</span></span>
<span data-ttu-id="0d80e-126">Gibt die HTTP-Methode des neuen API-Verwaltungsvorgangs an.</span><span class="sxs-lookup"><span data-stu-id="0d80e-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="0d80e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0d80e-127">-Name</span></span>
<span data-ttu-id="0d80e-128">Gibt den Anzeigenamen eines neuen API-Verwaltungsvorgangs an.</span><span class="sxs-lookup"><span data-stu-id="0d80e-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="0d80e-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0d80e-129">-OperationId</span></span>
<span data-ttu-id="0d80e-130">Gibt den Bezeichner des API-Verwaltungsvorgangs an.</span><span class="sxs-lookup"><span data-stu-id="0d80e-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="0d80e-131">-Request</span><span class="sxs-lookup"><span data-stu-id="0d80e-131">-Request</span></span>
<span data-ttu-id="0d80e-132">Gibt die Details des API-Verwaltungsvorgangs an.</span><span class="sxs-lookup"><span data-stu-id="0d80e-132">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d80e-133">-Responses</span><span class="sxs-lookup"><span data-stu-id="0d80e-133">-Responses</span></span>
<span data-ttu-id="0d80e-134">Gibt ein Array möglicher Reaktionen auf DEN API-Verwaltungsvorgang an.</span><span class="sxs-lookup"><span data-stu-id="0d80e-134">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d80e-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="0d80e-135">-TemplateParameters</span></span>
<span data-ttu-id="0d80e-136">Gibt ein Array von Parametern an, das im Parameter *"UrlTemplate" definiert ist.*</span><span class="sxs-lookup"><span data-stu-id="0d80e-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="0d80e-137">Wenn Sie diesen Parameter nicht angeben, wird ein Standardwert generiert, der auf *"UrlTemplate" basiert.*</span><span class="sxs-lookup"><span data-stu-id="0d80e-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d80e-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="0d80e-138">-UrlTemplate</span></span>
<span data-ttu-id="0d80e-139">Gibt die Vorlage "URL" an.</span><span class="sxs-lookup"><span data-stu-id="0d80e-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="0d80e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d80e-140">CommonParameters</span></span>
<span data-ttu-id="0d80e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d80e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d80e-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d80e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d80e-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d80e-143">INPUTS</span></span>

### <span data-ttu-id="0d80e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0d80e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0d80e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="0d80e-145">System.String</span></span>

### <span data-ttu-id="0d80e-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span><span class="sxs-lookup"><span data-stu-id="0d80e-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="0d80e-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="0d80e-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="0d80e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span><span class="sxs-lookup"><span data-stu-id="0d80e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="0d80e-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d80e-149">OUTPUTS</span></span>

### <span data-ttu-id="0d80e-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0d80e-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="0d80e-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0d80e-151">NOTES</span></span>

## <span data-ttu-id="0d80e-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0d80e-152">RELATED LINKS</span></span>

[<span data-ttu-id="0d80e-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0d80e-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="0d80e-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0d80e-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="0d80e-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0d80e-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


