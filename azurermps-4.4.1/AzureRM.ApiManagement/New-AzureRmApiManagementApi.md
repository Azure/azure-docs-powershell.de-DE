---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 295551f9d4ddf751980ec81626e3714a37aa47a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498085"
---
# <span data-ttu-id="07dde-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07dde-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="07dde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07dde-102">SYNOPSIS</span></span>
<span data-ttu-id="07dde-103">Erstellt eine API.</span><span class="sxs-lookup"><span data-stu-id="07dde-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07dde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07dde-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07dde-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07dde-105">DESCRIPTION</span></span>
<span data-ttu-id="07dde-106">Das Cmdlet **New-AzureRmApiManagementApi** erstellt eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="07dde-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="07dde-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07dde-107">EXAMPLES</span></span>

### <span data-ttu-id="07dde-108">Beispiel 1: Erstellen einer API</span><span class="sxs-lookup"><span data-stu-id="07dde-108">Example 1: Create an API</span></span>
```
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="07dde-109">Dieser Befehl erstellt eine API mit dem Namen EchoApi mit der angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="07dde-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="07dde-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07dde-110">PARAMETERS</span></span>

### <span data-ttu-id="07dde-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="07dde-111">-ApiId</span></span>
<span data-ttu-id="07dde-112">Gibt die ID der zu erstellende API an.</span><span class="sxs-lookup"><span data-stu-id="07dde-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="07dde-113">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet eine ID für Sie.</span><span class="sxs-lookup"><span data-stu-id="07dde-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="07dde-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="07dde-114">-AuthorizationScope</span></span>
<span data-ttu-id="07dde-115">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="07dde-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="07dde-116">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="07dde-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="07dde-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="07dde-117">-AuthorizationServerId</span></span>
<span data-ttu-id="07dde-118">Gibt die OAuth-autorisierungsserver-ID an.</span><span class="sxs-lookup"><span data-stu-id="07dde-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="07dde-119">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="07dde-119">The default value is $Null.</span></span>
<span data-ttu-id="07dde-120">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="07dde-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="07dde-121">-Context</span><span class="sxs-lookup"><span data-stu-id="07dde-121">-Context</span></span>
<span data-ttu-id="07dde-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="07dde-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07dde-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07dde-123">-Description</span></span>
<span data-ttu-id="07dde-124">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="07dde-124">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="07dde-125">-Name</span><span class="sxs-lookup"><span data-stu-id="07dde-125">-Name</span></span>
<span data-ttu-id="07dde-126">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="07dde-126">Specifies the name of the web API.</span></span>
<span data-ttu-id="07dde-127">Hierbei handelt es sich um den öffentlichen Namen der API, wie er auf dem Entwickler-und Administratorportal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="07dde-127">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="07dde-128">-Path</span><span class="sxs-lookup"><span data-stu-id="07dde-128">-Path</span></span>
<span data-ttu-id="07dde-129">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt, der dem Feld "URL-Suffix" für WebAPI im Administratorportal entspricht.</span><span class="sxs-lookup"><span data-stu-id="07dde-129">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="07dde-130">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="07dde-130">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="07dde-131">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="07dde-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="07dde-132">-ProductIDs</span><span class="sxs-lookup"><span data-stu-id="07dde-132">-ProductIds</span></span>
<span data-ttu-id="07dde-133">Gibt ein Array von Produkt-IDs an, dem die neue API hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="07dde-133">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07dde-134">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="07dde-134">-Protocols</span></span>
<span data-ttu-id="07dde-135">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="07dde-135">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="07dde-136">Gültige Werte sind http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="07dde-136">Valid values are http, https.</span></span>
<span data-ttu-id="07dde-137">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="07dde-137">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="07dde-138">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="07dde-138">The default value is $Null.</span></span>

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

### <span data-ttu-id="07dde-139">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="07dde-139">-ServiceUrl</span></span>
<span data-ttu-id="07dde-140">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="07dde-140">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="07dde-141">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="07dde-141">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="07dde-142">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="07dde-142">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="07dde-143">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="07dde-143">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="07dde-144">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="07dde-144">Specifies the subscription key header name.</span></span>
<span data-ttu-id="07dde-145">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="07dde-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="07dde-146">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="07dde-146">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="07dde-147">Gibt den Abfragezeichenfolgenparameter Namen für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="07dde-147">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="07dde-148">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="07dde-148">The default value is $Null.</span></span>

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

### <span data-ttu-id="07dde-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07dde-149">-DefaultProfile</span></span>
<span data-ttu-id="07dde-150">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07dde-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07dde-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07dde-151">CommonParameters</span></span>
<span data-ttu-id="07dde-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07dde-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07dde-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07dde-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07dde-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07dde-154">INPUTS</span></span>

## <span data-ttu-id="07dde-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07dde-155">OUTPUTS</span></span>

### <span data-ttu-id="07dde-156">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07dde-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="07dde-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="07dde-157">NOTES</span></span>

## <span data-ttu-id="07dde-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07dde-158">RELATED LINKS</span></span>

[<span data-ttu-id="07dde-159">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07dde-159">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="07dde-160">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07dde-160">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="07dde-161">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07dde-161">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="07dde-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07dde-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="07dde-163">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="07dde-163">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


