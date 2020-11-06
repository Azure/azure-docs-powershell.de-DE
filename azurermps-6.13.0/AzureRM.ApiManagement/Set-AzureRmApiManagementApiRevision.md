---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501229"
---
# <span data-ttu-id="7683f-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7683f-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="7683f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7683f-102">SYNOPSIS</span></span>
<span data-ttu-id="7683f-103">Ändert eine API-Revision</span><span class="sxs-lookup"><span data-stu-id="7683f-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7683f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7683f-104">SYNTAX</span></span>

### <span data-ttu-id="7683f-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7683f-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7683f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7683f-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7683f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7683f-107">DESCRIPTION</span></span>
<span data-ttu-id="7683f-108">Das Cmdlet " **Satz-AzureRmApiManagementApiRevision** " ändert eine Azure API Management-API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="7683f-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="7683f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7683f-109">EXAMPLES</span></span>

### <span data-ttu-id="7683f-110">Beispiel 1 Ändern einer API-Revision</span><span class="sxs-lookup"><span data-stu-id="7683f-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="7683f-111">Das Cmdlet aktualisiert die `2` Revision der API `echo-api` mit einer neuen Beschreibung, einem neuen Protokoll und einem Pfad.</span><span class="sxs-lookup"><span data-stu-id="7683f-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="7683f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7683f-112">PARAMETERS</span></span>

### <span data-ttu-id="7683f-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7683f-113">-ApiId</span></span>
<span data-ttu-id="7683f-114">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="7683f-114">Identifier of existing API.</span></span>
<span data-ttu-id="7683f-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7683f-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7683f-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7683f-116">-ApiRevision</span></span>
<span data-ttu-id="7683f-117">Bezeichner der vorhandenen API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="7683f-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="7683f-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7683f-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7683f-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="7683f-119">-AuthorizationScope</span></span>
<span data-ttu-id="7683f-120">OAuth-Vorgangsbereich</span><span class="sxs-lookup"><span data-stu-id="7683f-120">OAuth operations scope.</span></span>
<span data-ttu-id="7683f-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7683f-121">This parameter is optional.</span></span>
<span data-ttu-id="7683f-122">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7683f-122">Default value is $null.</span></span>

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

### <span data-ttu-id="7683f-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="7683f-123">-AuthorizationServerId</span></span>
<span data-ttu-id="7683f-124">OAuth-autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="7683f-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="7683f-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7683f-125">This parameter is optional.</span></span>
<span data-ttu-id="7683f-126">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7683f-126">Default value is $null.</span></span>
<span data-ttu-id="7683f-127">Muss angegeben werden, wenn AuthorizationScope angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7683f-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="7683f-128">-Context</span><span class="sxs-lookup"><span data-stu-id="7683f-128">-Context</span></span>
<span data-ttu-id="7683f-129">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7683f-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7683f-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7683f-130">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7683f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7683f-131">-DefaultProfile</span></span>
<span data-ttu-id="7683f-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7683f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7683f-133">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7683f-133">-Description</span></span>
<span data-ttu-id="7683f-134">Web-API-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="7683f-134">Web API description.</span></span>
<span data-ttu-id="7683f-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7683f-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="7683f-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7683f-136">-InputObject</span></span>
<span data-ttu-id="7683f-137">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="7683f-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="7683f-138">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7683f-138">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7683f-139">-Name</span><span class="sxs-lookup"><span data-stu-id="7683f-139">-Name</span></span>
<span data-ttu-id="7683f-140">Web-API-Name.</span><span class="sxs-lookup"><span data-stu-id="7683f-140">Web API name.</span></span>
<span data-ttu-id="7683f-141">Öffentlicher Name der API, wie er auf dem Entwickler-und Administratorportal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7683f-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="7683f-142">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7683f-142">This parameter is required.</span></span>

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

### <span data-ttu-id="7683f-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7683f-143">-PassThru</span></span>
<span data-ttu-id="7683f-144">Wenn angegeben, wird eine Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi-Typs, die die festgelegte API darstellt.</span><span class="sxs-lookup"><span data-stu-id="7683f-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7683f-145">-Path</span><span class="sxs-lookup"><span data-stu-id="7683f-145">-Path</span></span>
<span data-ttu-id="7683f-146">Web-API-Pfad.</span><span class="sxs-lookup"><span data-stu-id="7683f-146">Web API Path.</span></span>
<span data-ttu-id="7683f-147">Der letzte Teil der öffentlichen URL der API.</span><span class="sxs-lookup"><span data-stu-id="7683f-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="7683f-148">Diese URL wird von API-Consumern zum Senden von Anforderungen an den Webdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="7683f-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="7683f-149">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="7683f-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="7683f-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7683f-150">This parameter is optional.</span></span>
<span data-ttu-id="7683f-151">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7683f-151">Default value is $null.</span></span>

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

### <span data-ttu-id="7683f-152">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="7683f-152">-Protocols</span></span>
<span data-ttu-id="7683f-153">Web-API-Protokolle (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="7683f-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="7683f-154">Protokolle, über die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7683f-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="7683f-155">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7683f-155">This parameter is required.</span></span>
<span data-ttu-id="7683f-156">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7683f-156">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7683f-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="7683f-157">-ServiceUrl</span></span>
<span data-ttu-id="7683f-158">Eine URL des Webdiensts, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="7683f-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="7683f-159">Diese URL wird nur von der Azure-API-Verwaltung verwendet und wird nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="7683f-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="7683f-160">Muss 1 bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="7683f-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="7683f-161">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7683f-161">This parameter is required.</span></span>

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

### <span data-ttu-id="7683f-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="7683f-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="7683f-163">Name des Abonnementschlüssel Headers.</span><span class="sxs-lookup"><span data-stu-id="7683f-163">Subscription key header name.</span></span>
<span data-ttu-id="7683f-164">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7683f-164">This parameter is optional.</span></span>
<span data-ttu-id="7683f-165">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7683f-165">Default value is $null.</span></span>

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

### <span data-ttu-id="7683f-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="7683f-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="7683f-167">Parameter Name der Abfragezeichenfolge für den Abonnementschlüssel</span><span class="sxs-lookup"><span data-stu-id="7683f-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="7683f-168">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7683f-168">This parameter is optional.</span></span>
<span data-ttu-id="7683f-169">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7683f-169">Default value is $null.</span></span>

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

### <span data-ttu-id="7683f-170">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7683f-170">-Confirm</span></span>
<span data-ttu-id="7683f-171">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7683f-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7683f-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7683f-172">-WhatIf</span></span>
<span data-ttu-id="7683f-173">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7683f-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7683f-174">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7683f-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7683f-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7683f-175">CommonParameters</span></span>
<span data-ttu-id="7683f-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7683f-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7683f-177">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7683f-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7683f-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7683f-178">INPUTS</span></span>

### <span data-ttu-id="7683f-179">System. String</span><span class="sxs-lookup"><span data-stu-id="7683f-179">System.String</span></span>

### <span data-ttu-id="7683f-180">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7683f-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7683f-181">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7683f-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="7683f-182">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7683f-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7683f-183">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="7683f-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="7683f-184">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="7683f-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7683f-185">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7683f-185">OUTPUTS</span></span>

### <span data-ttu-id="7683f-186">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7683f-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7683f-187">Notizen</span><span class="sxs-lookup"><span data-stu-id="7683f-187">NOTES</span></span>

## <span data-ttu-id="7683f-188">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7683f-188">RELATED LINKS</span></span>

[<span data-ttu-id="7683f-189">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7683f-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="7683f-190">Neu – AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7683f-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="7683f-191">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="7683f-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
