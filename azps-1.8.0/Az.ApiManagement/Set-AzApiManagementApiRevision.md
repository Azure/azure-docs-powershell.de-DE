---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: 8b2e29da3c3f6140cbab422e74d09656c921c16c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821019"
---
# <span data-ttu-id="39317-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="39317-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="39317-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39317-102">SYNOPSIS</span></span>
<span data-ttu-id="39317-103">Ändert eine API-Revision</span><span class="sxs-lookup"><span data-stu-id="39317-103">Modifies an API Revision</span></span>

## <span data-ttu-id="39317-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39317-104">SYNTAX</span></span>

### <span data-ttu-id="39317-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="39317-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39317-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="39317-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39317-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39317-107">DESCRIPTION</span></span>
<span data-ttu-id="39317-108">Das Cmdlet " **Satz-AzApiManagementApiRevision** " ändert eine Azure API Management-API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="39317-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="39317-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39317-109">EXAMPLES</span></span>

### <span data-ttu-id="39317-110">Beispiel 1 Ändern einer API-Revision</span><span class="sxs-lookup"><span data-stu-id="39317-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="39317-111">Das Cmdlet aktualisiert die `2` Revision der API `echo-api` mit einer neuen Beschreibung, einem neuen Protokoll und einem Pfad.</span><span class="sxs-lookup"><span data-stu-id="39317-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="39317-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="39317-112">PARAMETERS</span></span>

### <span data-ttu-id="39317-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="39317-113">-ApiId</span></span>
<span data-ttu-id="39317-114">Bezeichner der vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="39317-114">Identifier of existing API.</span></span>
<span data-ttu-id="39317-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39317-115">This parameter is required.</span></span>

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

### <span data-ttu-id="39317-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="39317-116">-ApiRevision</span></span>
<span data-ttu-id="39317-117">Bezeichner der vorhandenen API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="39317-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="39317-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39317-118">This parameter is required.</span></span>

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

### <span data-ttu-id="39317-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="39317-119">-AuthorizationScope</span></span>
<span data-ttu-id="39317-120">OAuth-Vorgangsbereich</span><span class="sxs-lookup"><span data-stu-id="39317-120">OAuth operations scope.</span></span>
<span data-ttu-id="39317-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="39317-121">This parameter is optional.</span></span>
<span data-ttu-id="39317-122">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="39317-122">Default value is $null.</span></span>

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

### <span data-ttu-id="39317-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="39317-123">-AuthorizationServerId</span></span>
<span data-ttu-id="39317-124">OAuth-autorisierungsserver-ID.</span><span class="sxs-lookup"><span data-stu-id="39317-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="39317-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="39317-125">This parameter is optional.</span></span>
<span data-ttu-id="39317-126">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="39317-126">Default value is $null.</span></span>
<span data-ttu-id="39317-127">Muss angegeben werden, wenn AuthorizationScope angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="39317-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="39317-128">-Context</span><span class="sxs-lookup"><span data-stu-id="39317-128">-Context</span></span>
<span data-ttu-id="39317-129">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="39317-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="39317-130">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39317-130">This parameter is required.</span></span>

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

### <span data-ttu-id="39317-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39317-131">-DefaultProfile</span></span>
<span data-ttu-id="39317-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39317-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39317-133">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39317-133">-Description</span></span>
<span data-ttu-id="39317-134">Web-API-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="39317-134">Web API description.</span></span>
<span data-ttu-id="39317-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="39317-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="39317-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39317-136">-InputObject</span></span>
<span data-ttu-id="39317-137">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="39317-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="39317-138">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39317-138">This parameter is required.</span></span>

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

### <span data-ttu-id="39317-139">-Name</span><span class="sxs-lookup"><span data-stu-id="39317-139">-Name</span></span>
<span data-ttu-id="39317-140">Web-API-Name.</span><span class="sxs-lookup"><span data-stu-id="39317-140">Web API name.</span></span>
<span data-ttu-id="39317-141">Öffentlicher Name der API, wie er auf dem Entwickler-und Administratorportal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="39317-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="39317-142">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39317-142">This parameter is required.</span></span>

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

### <span data-ttu-id="39317-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39317-143">-PassThru</span></span>
<span data-ttu-id="39317-144">Wenn angegeben, wird eine Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi-Typs, die die festgelegte API darstellt.</span><span class="sxs-lookup"><span data-stu-id="39317-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="39317-145">-Path</span><span class="sxs-lookup"><span data-stu-id="39317-145">-Path</span></span>
<span data-ttu-id="39317-146">Web-API-Pfad.</span><span class="sxs-lookup"><span data-stu-id="39317-146">Web API Path.</span></span>
<span data-ttu-id="39317-147">Der letzte Teil der öffentlichen URL der API.</span><span class="sxs-lookup"><span data-stu-id="39317-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="39317-148">Diese URL wird von API-Consumern zum Senden von Anforderungen an den Webdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="39317-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="39317-149">Muss 1 bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="39317-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="39317-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="39317-150">This parameter is optional.</span></span>
<span data-ttu-id="39317-151">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="39317-151">Default value is $null.</span></span>

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

### <span data-ttu-id="39317-152">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="39317-152">-Protocols</span></span>
<span data-ttu-id="39317-153">Web-API-Protokolle (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="39317-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="39317-154">Protokolle, über die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="39317-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="39317-155">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39317-155">This parameter is required.</span></span>
<span data-ttu-id="39317-156">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="39317-156">Default value is $null.</span></span>

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

### <span data-ttu-id="39317-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="39317-157">-ServiceUrl</span></span>
<span data-ttu-id="39317-158">Eine URL des Webdiensts, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="39317-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="39317-159">Diese URL wird nur von der Azure-API-Verwaltung verwendet und wird nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="39317-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="39317-160">Muss 1 bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="39317-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="39317-161">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39317-161">This parameter is required.</span></span>

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

### <span data-ttu-id="39317-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="39317-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="39317-163">Name des Abonnementschlüssel Headers.</span><span class="sxs-lookup"><span data-stu-id="39317-163">Subscription key header name.</span></span>
<span data-ttu-id="39317-164">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="39317-164">This parameter is optional.</span></span>
<span data-ttu-id="39317-165">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="39317-165">Default value is $null.</span></span>

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

### <span data-ttu-id="39317-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="39317-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="39317-167">Parameter Name der Abfragezeichenfolge für den Abonnementschlüssel</span><span class="sxs-lookup"><span data-stu-id="39317-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="39317-168">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="39317-168">This parameter is optional.</span></span>
<span data-ttu-id="39317-169">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="39317-169">Default value is $null.</span></span>

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

### <span data-ttu-id="39317-170">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39317-170">-Confirm</span></span>
<span data-ttu-id="39317-171">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39317-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39317-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39317-172">-WhatIf</span></span>
<span data-ttu-id="39317-173">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39317-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39317-174">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39317-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39317-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39317-175">CommonParameters</span></span>
<span data-ttu-id="39317-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39317-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39317-177">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39317-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39317-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39317-178">INPUTS</span></span>

### <span data-ttu-id="39317-179">System. String</span><span class="sxs-lookup"><span data-stu-id="39317-179">System.String</span></span>

### <span data-ttu-id="39317-180">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="39317-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="39317-181">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="39317-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="39317-182">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="39317-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="39317-183">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="39317-183">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39317-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39317-184">OUTPUTS</span></span>

### <span data-ttu-id="39317-185">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="39317-185">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="39317-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="39317-186">NOTES</span></span>

## <span data-ttu-id="39317-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39317-187">RELATED LINKS</span></span>

[<span data-ttu-id="39317-188">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="39317-188">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="39317-189">Neu – AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="39317-189">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="39317-190">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="39317-190">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)