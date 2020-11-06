---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 6ab29738f181f6fece9d3b4cd679496a9add9bc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499101"
---
# <span data-ttu-id="677a4-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="677a4-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="677a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="677a4-102">SYNOPSIS</span></span>
<span data-ttu-id="677a4-103">Ändert eine API.</span><span class="sxs-lookup"><span data-stu-id="677a4-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="677a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="677a4-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="677a4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="677a4-105">DESCRIPTION</span></span>
<span data-ttu-id="677a4-106">Das Cmdlet " **Satz-AzureRmApiManagementApi** " ändert eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="677a4-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="677a4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="677a4-107">EXAMPLES</span></span>

### <span data-ttu-id="677a4-108">Beispiel 1 Ändern einer API</span><span class="sxs-lookup"><span data-stu-id="677a4-108">Example 1 Modify an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="677a4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="677a4-109">PARAMETERS</span></span>

### <span data-ttu-id="677a4-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="677a4-110">-ApiId</span></span>
<span data-ttu-id="677a4-111">Gibt die ID der zu ändernden API an.</span><span class="sxs-lookup"><span data-stu-id="677a4-111">Specifies the ID of the API to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="677a4-112">-AuthorizationScope</span></span>
<span data-ttu-id="677a4-113">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="677a4-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="677a4-114">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="677a4-114">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="677a4-115">-AuthorizationServerId</span></span>
<span data-ttu-id="677a4-116">Gibt den OAuth-autorisierungsserver-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="677a4-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="677a4-117">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="677a4-117">The default value is $Null.</span></span>
<span data-ttu-id="677a4-118">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="677a4-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-119">-Context</span><span class="sxs-lookup"><span data-stu-id="677a4-119">-Context</span></span>
<span data-ttu-id="677a4-120">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="677a4-120">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677a4-121">-DefaultProfile</span></span>
<span data-ttu-id="677a4-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="677a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="677a4-123">-Description</span></span>
<span data-ttu-id="677a4-124">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="677a4-124">Specifies a description for the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="677a4-125">-Name</span></span>
<span data-ttu-id="677a4-126">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="677a4-126">Specifies the name of the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="677a4-127">-PassThru</span></span>
<span data-ttu-id="677a4-128">passthru</span><span class="sxs-lookup"><span data-stu-id="677a4-128">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-129">-Path</span><span class="sxs-lookup"><span data-stu-id="677a4-129">-Path</span></span>
<span data-ttu-id="677a4-130">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt.</span><span class="sxs-lookup"><span data-stu-id="677a4-130">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="677a4-131">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="677a4-131">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="677a4-132">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="677a4-132">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-133">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="677a4-133">-Protocols</span></span>
<span data-ttu-id="677a4-134">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="677a4-134">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="677a4-135">psdx_paramvalues http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="677a4-135">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="677a4-136">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="677a4-136">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="677a4-137">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="677a4-137">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-138">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="677a4-138">-ServiceUrl</span></span>
<span data-ttu-id="677a4-139">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="677a4-139">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="677a4-140">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="677a4-140">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="677a4-141">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="677a4-141">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-142">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="677a4-142">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="677a4-143">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="677a4-143">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="677a4-144">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="677a4-144">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-145">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="677a4-145">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="677a4-146">Gibt den Namen des Abfragezeichen folgen Parameters für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="677a4-146">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="677a4-147">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="677a4-147">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="677a4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677a4-148">CommonParameters</span></span>
<span data-ttu-id="677a4-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677a4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677a4-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="677a4-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677a4-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="677a4-151">INPUTS</span></span>

### <span data-ttu-id="677a4-152">Keine</span><span class="sxs-lookup"><span data-stu-id="677a4-152">None</span></span>
<span data-ttu-id="677a4-153">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="677a4-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="677a4-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="677a4-154">OUTPUTS</span></span>

### <span data-ttu-id="677a4-155">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="677a4-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="677a4-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="677a4-156">NOTES</span></span>

## <span data-ttu-id="677a4-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="677a4-157">RELATED LINKS</span></span>

[<span data-ttu-id="677a4-158">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="677a4-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="677a4-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="677a4-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="677a4-160">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="677a4-160">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="677a4-161">Neu – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="677a4-161">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="677a4-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="677a4-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


