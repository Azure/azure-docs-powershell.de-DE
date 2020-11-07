---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821028"
---
# <span data-ttu-id="2f006-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f006-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="2f006-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f006-102">SYNOPSIS</span></span>
<span data-ttu-id="2f006-103">Ändert eine API.</span><span class="sxs-lookup"><span data-stu-id="2f006-103">Modifies an API.</span></span>

## <span data-ttu-id="2f006-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f006-104">SYNTAX</span></span>

### <span data-ttu-id="2f006-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f006-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f006-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f006-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f006-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f006-107">DESCRIPTION</span></span>
<span data-ttu-id="2f006-108">Das Cmdlet " **Satz-AzApiManagementApi** " ändert eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="2f006-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="2f006-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f006-109">EXAMPLES</span></span>

### <span data-ttu-id="2f006-110">Beispiel 1 Ändern einer API</span><span class="sxs-lookup"><span data-stu-id="2f006-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="2f006-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f006-111">PARAMETERS</span></span>

### <span data-ttu-id="2f006-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2f006-112">-ApiId</span></span>
<span data-ttu-id="2f006-113">Gibt die ID der zu ändernden API an.</span><span class="sxs-lookup"><span data-stu-id="2f006-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="2f006-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2f006-114">-AuthorizationScope</span></span>
<span data-ttu-id="2f006-115">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="2f006-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2f006-116">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="2f006-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="2f006-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="2f006-117">-AuthorizationServerId</span></span>
<span data-ttu-id="2f006-118">Gibt den OAuth-autorisierungsserver-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="2f006-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="2f006-119">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="2f006-119">The default value is $Null.</span></span>
<span data-ttu-id="2f006-120">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2f006-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="2f006-121">-Context</span><span class="sxs-lookup"><span data-stu-id="2f006-121">-Context</span></span>
<span data-ttu-id="2f006-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2f006-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2f006-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f006-123">-DefaultProfile</span></span>
<span data-ttu-id="2f006-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f006-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f006-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f006-125">-Description</span></span>
<span data-ttu-id="2f006-126">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="2f006-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="2f006-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f006-127">-InputObject</span></span>
<span data-ttu-id="2f006-128">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="2f006-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="2f006-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f006-129">This parameter is required.</span></span>

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

### <span data-ttu-id="2f006-130">-Name</span><span class="sxs-lookup"><span data-stu-id="2f006-130">-Name</span></span>
<span data-ttu-id="2f006-131">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="2f006-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="2f006-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f006-132">-PassThru</span></span>
<span data-ttu-id="2f006-133">passthru</span><span class="sxs-lookup"><span data-stu-id="2f006-133">passthru</span></span>

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

### <span data-ttu-id="2f006-134">-Path</span><span class="sxs-lookup"><span data-stu-id="2f006-134">-Path</span></span>
<span data-ttu-id="2f006-135">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt.</span><span class="sxs-lookup"><span data-stu-id="2f006-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="2f006-136">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="2f006-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2f006-137">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="2f006-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="2f006-138">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="2f006-138">-Protocols</span></span>
<span data-ttu-id="2f006-139">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="2f006-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2f006-140">psdx_paramvalues http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2f006-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="2f006-141">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2f006-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2f006-142">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="2f006-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="2f006-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2f006-143">-ServiceUrl</span></span>
<span data-ttu-id="2f006-144">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="2f006-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2f006-145">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="2f006-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2f006-146">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="2f006-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="2f006-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="2f006-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2f006-148">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="2f006-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="2f006-149">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="2f006-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="2f006-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2f006-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2f006-151">Gibt den Namen des Abfragezeichen folgen Parameters für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="2f006-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="2f006-152">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="2f006-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="2f006-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f006-153">CommonParameters</span></span>
<span data-ttu-id="2f006-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f006-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f006-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f006-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f006-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f006-156">INPUTS</span></span>

### <span data-ttu-id="2f006-157">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2f006-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2f006-158">System. String</span><span class="sxs-lookup"><span data-stu-id="2f006-158">System.String</span></span>

### <span data-ttu-id="2f006-159">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f006-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="2f006-160">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="2f006-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="2f006-161">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2f006-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f006-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f006-162">OUTPUTS</span></span>

### <span data-ttu-id="2f006-163">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f006-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2f006-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f006-164">NOTES</span></span>

## <span data-ttu-id="2f006-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f006-165">RELATED LINKS</span></span>

[<span data-ttu-id="2f006-166">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f006-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="2f006-167">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f006-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="2f006-168">Importieren-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f006-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="2f006-169">Neu – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f006-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="2f006-170">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2f006-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


