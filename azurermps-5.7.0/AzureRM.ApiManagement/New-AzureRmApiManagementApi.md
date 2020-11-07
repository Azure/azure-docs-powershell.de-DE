---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 75a6dbf480e8b2f2f3d9f7524db4e57e5ed88f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664700"
---
# <span data-ttu-id="d056c-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d056c-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="d056c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d056c-102">SYNOPSIS</span></span>
<span data-ttu-id="d056c-103">Erstellt eine API.</span><span class="sxs-lookup"><span data-stu-id="d056c-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d056c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d056c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d056c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d056c-105">DESCRIPTION</span></span>
<span data-ttu-id="d056c-106">Das Cmdlet **New-AzureRmApiManagementApi** erstellt eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="d056c-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="d056c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d056c-107">EXAMPLES</span></span>

### <span data-ttu-id="d056c-108">Beispiel 1: Erstellen einer API</span><span class="sxs-lookup"><span data-stu-id="d056c-108">Example 1: Create an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="d056c-109">Dieser Befehl erstellt eine API mit dem Namen EchoApi mit der angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="d056c-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="d056c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d056c-110">PARAMETERS</span></span>

### <span data-ttu-id="d056c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d056c-111">-ApiId</span></span>
<span data-ttu-id="d056c-112">Gibt die ID der zu erstellende API an.</span><span class="sxs-lookup"><span data-stu-id="d056c-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="d056c-113">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet eine ID für Sie.</span><span class="sxs-lookup"><span data-stu-id="d056c-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="d056c-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="d056c-114">-AuthorizationScope</span></span>
<span data-ttu-id="d056c-115">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="d056c-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="d056c-116">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="d056c-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="d056c-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="d056c-117">-AuthorizationServerId</span></span>
<span data-ttu-id="d056c-118">Gibt die OAuth-autorisierungsserver-ID an.</span><span class="sxs-lookup"><span data-stu-id="d056c-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="d056c-119">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="d056c-119">The default value is $Null.</span></span>
<span data-ttu-id="d056c-120">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d056c-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="d056c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="d056c-121">-Context</span></span>
<span data-ttu-id="d056c-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d056c-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d056c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d056c-123">-DefaultProfile</span></span>
<span data-ttu-id="d056c-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d056c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d056c-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d056c-125">-Description</span></span>
<span data-ttu-id="d056c-126">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="d056c-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="d056c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d056c-127">-Name</span></span>
<span data-ttu-id="d056c-128">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="d056c-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="d056c-129">Hierbei handelt es sich um den öffentlichen Namen der API, wie er auf dem Entwickler-und Administratorportal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d056c-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="d056c-130">-Path</span><span class="sxs-lookup"><span data-stu-id="d056c-130">-Path</span></span>
<span data-ttu-id="d056c-131">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt, der dem Feld "URL-Suffix" für WebAPI im Administratorportal entspricht.</span><span class="sxs-lookup"><span data-stu-id="d056c-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="d056c-132">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="d056c-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="d056c-133">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="d056c-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="d056c-134">-ProductIDs</span><span class="sxs-lookup"><span data-stu-id="d056c-134">-ProductIds</span></span>
<span data-ttu-id="d056c-135">Gibt ein Array von Produkt-IDs an, dem die neue API hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d056c-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d056c-136">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="d056c-136">-Protocols</span></span>
<span data-ttu-id="d056c-137">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="d056c-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="d056c-138">Gültige Werte sind http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d056c-138">Valid values are http, https.</span></span>
<span data-ttu-id="d056c-139">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d056c-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="d056c-140">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="d056c-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="d056c-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="d056c-141">-ServiceUrl</span></span>
<span data-ttu-id="d056c-142">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="d056c-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="d056c-143">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d056c-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="d056c-144">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="d056c-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="d056c-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="d056c-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="d056c-146">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="d056c-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="d056c-147">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="d056c-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="d056c-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="d056c-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="d056c-149">Gibt den Abfragezeichenfolgenparameter Namen für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="d056c-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="d056c-150">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="d056c-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="d056c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d056c-151">CommonParameters</span></span>
<span data-ttu-id="d056c-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d056c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d056c-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d056c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d056c-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d056c-154">INPUTS</span></span>

### <span data-ttu-id="d056c-155">Keine</span><span class="sxs-lookup"><span data-stu-id="d056c-155">None</span></span>
<span data-ttu-id="d056c-156">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d056c-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d056c-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d056c-157">OUTPUTS</span></span>

### <span data-ttu-id="d056c-158">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d056c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d056c-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="d056c-159">NOTES</span></span>

## <span data-ttu-id="d056c-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d056c-160">RELATED LINKS</span></span>

[<span data-ttu-id="d056c-161">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d056c-161">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="d056c-162">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d056c-162">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="d056c-163">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d056c-163">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="d056c-164">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d056c-164">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="d056c-165">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d056c-165">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


