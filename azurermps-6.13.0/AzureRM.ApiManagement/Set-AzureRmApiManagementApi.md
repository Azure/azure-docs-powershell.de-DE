---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 10df1034b414260cb618c7de0b31b8ad93d30d0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501230"
---
# <span data-ttu-id="4d673-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4d673-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="4d673-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d673-102">SYNOPSIS</span></span>
<span data-ttu-id="4d673-103">Ändert eine API.</span><span class="sxs-lookup"><span data-stu-id="4d673-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d673-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d673-104">SYNTAX</span></span>

### <span data-ttu-id="4d673-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d673-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d673-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4d673-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d673-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d673-107">DESCRIPTION</span></span>
<span data-ttu-id="4d673-108">Das Cmdlet " **Satz-AzureRmApiManagementApi** " ändert eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="4d673-108">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="4d673-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d673-109">EXAMPLES</span></span>

### <span data-ttu-id="4d673-110">Beispiel 1 Ändern einer API</span><span class="sxs-lookup"><span data-stu-id="4d673-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="4d673-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d673-111">PARAMETERS</span></span>

### <span data-ttu-id="4d673-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4d673-112">-ApiId</span></span>
<span data-ttu-id="4d673-113">Gibt die ID der zu ändernden API an.</span><span class="sxs-lookup"><span data-stu-id="4d673-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="4d673-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="4d673-114">-AuthorizationScope</span></span>
<span data-ttu-id="4d673-115">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="4d673-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="4d673-116">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4d673-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="4d673-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="4d673-117">-AuthorizationServerId</span></span>
<span data-ttu-id="4d673-118">Gibt den OAuth-autorisierungsserver-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="4d673-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="4d673-119">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4d673-119">The default value is $Null.</span></span>
<span data-ttu-id="4d673-120">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4d673-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="4d673-121">-Context</span><span class="sxs-lookup"><span data-stu-id="4d673-121">-Context</span></span>
<span data-ttu-id="4d673-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4d673-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4d673-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d673-123">-DefaultProfile</span></span>
<span data-ttu-id="4d673-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d673-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d673-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d673-125">-Description</span></span>
<span data-ttu-id="4d673-126">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="4d673-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="4d673-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4d673-127">-InputObject</span></span>
<span data-ttu-id="4d673-128">Instanz von PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="4d673-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="4d673-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4d673-129">This parameter is required.</span></span>

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

### <span data-ttu-id="4d673-130">-Name</span><span class="sxs-lookup"><span data-stu-id="4d673-130">-Name</span></span>
<span data-ttu-id="4d673-131">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="4d673-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="4d673-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d673-132">-PassThru</span></span>
<span data-ttu-id="4d673-133">passthru</span><span class="sxs-lookup"><span data-stu-id="4d673-133">passthru</span></span>

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

### <span data-ttu-id="4d673-134">-Path</span><span class="sxs-lookup"><span data-stu-id="4d673-134">-Path</span></span>
<span data-ttu-id="4d673-135">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt.</span><span class="sxs-lookup"><span data-stu-id="4d673-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="4d673-136">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="4d673-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="4d673-137">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4d673-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="4d673-138">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="4d673-138">-Protocols</span></span>
<span data-ttu-id="4d673-139">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="4d673-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="4d673-140">psdx_paramvalues http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4d673-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="4d673-141">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4d673-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="4d673-142">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4d673-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="4d673-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="4d673-143">-ServiceUrl</span></span>
<span data-ttu-id="4d673-144">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="4d673-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="4d673-145">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="4d673-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="4d673-146">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="4d673-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="4d673-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="4d673-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="4d673-148">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="4d673-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="4d673-149">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4d673-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="4d673-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="4d673-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="4d673-151">Gibt den Namen des Abfragezeichen folgen Parameters für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="4d673-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="4d673-152">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="4d673-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="4d673-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d673-153">CommonParameters</span></span>
<span data-ttu-id="4d673-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d673-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d673-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d673-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d673-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d673-156">INPUTS</span></span>

### <span data-ttu-id="4d673-157">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4d673-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4d673-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4d673-158">System.String</span></span>

### <span data-ttu-id="4d673-159">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4d673-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="4d673-160">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d673-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4d673-161">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="4d673-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="4d673-162">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="4d673-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4d673-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d673-163">OUTPUTS</span></span>

### <span data-ttu-id="4d673-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4d673-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="4d673-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d673-165">NOTES</span></span>

## <span data-ttu-id="4d673-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d673-166">RELATED LINKS</span></span>

[<span data-ttu-id="4d673-167">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4d673-167">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="4d673-168">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4d673-168">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="4d673-169">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4d673-169">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="4d673-170">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4d673-170">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="4d673-171">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="4d673-171">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


