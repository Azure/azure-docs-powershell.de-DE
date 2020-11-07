---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 2601635bb3fc9ac1f6886adcb2cbb971a3cf0d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664128"
---
# <span data-ttu-id="e9328-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e9328-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="e9328-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9328-102">SYNOPSIS</span></span>
<span data-ttu-id="e9328-103">Erstellt eine API.</span><span class="sxs-lookup"><span data-stu-id="e9328-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9328-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9328-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9328-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9328-105">DESCRIPTION</span></span>
<span data-ttu-id="e9328-106">Das Cmdlet **New-AzureRmApiManagementApi** erstellt eine Azure API-Verwaltungs-API.</span><span class="sxs-lookup"><span data-stu-id="e9328-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="e9328-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9328-107">EXAMPLES</span></span>

### <span data-ttu-id="e9328-108">Beispiel 1: Erstellen einer API</span><span class="sxs-lookup"><span data-stu-id="e9328-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="e9328-109">Dieser Befehl erstellt eine API mit dem Namen EchoApi mit der angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="e9328-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="e9328-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9328-110">PARAMETERS</span></span>

### <span data-ttu-id="e9328-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e9328-111">-ApiId</span></span>
<span data-ttu-id="e9328-112">Gibt die ID der zu erstellende API an.</span><span class="sxs-lookup"><span data-stu-id="e9328-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="e9328-113">Wenn Sie diesen Parameter nicht angeben, generiert dieses Cmdlet eine ID für Sie.</span><span class="sxs-lookup"><span data-stu-id="e9328-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="e9328-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="e9328-114">-AuthorizationScope</span></span>
<span data-ttu-id="e9328-115">Gibt den OAuth-Vorgangsbereich an.</span><span class="sxs-lookup"><span data-stu-id="e9328-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="e9328-116">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="e9328-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="e9328-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="e9328-117">-AuthorizationServerId</span></span>
<span data-ttu-id="e9328-118">Gibt die OAuth-autorisierungsserver-ID an.</span><span class="sxs-lookup"><span data-stu-id="e9328-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="e9328-119">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="e9328-119">The default value is $Null.</span></span>
<span data-ttu-id="e9328-120">Sie müssen diesen Parameter angeben, wenn *AuthorizationScope* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e9328-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="e9328-121">-Context</span><span class="sxs-lookup"><span data-stu-id="e9328-121">-Context</span></span>
<span data-ttu-id="e9328-122">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e9328-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e9328-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9328-123">-DefaultProfile</span></span>
<span data-ttu-id="e9328-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9328-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9328-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9328-125">-Description</span></span>
<span data-ttu-id="e9328-126">Gibt eine Beschreibung für die Web-API an.</span><span class="sxs-lookup"><span data-stu-id="e9328-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="e9328-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e9328-127">-Name</span></span>
<span data-ttu-id="e9328-128">Gibt den Namen der Web-API an.</span><span class="sxs-lookup"><span data-stu-id="e9328-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="e9328-129">Hierbei handelt es sich um den öffentlichen Namen der API, wie er auf dem Entwickler-und Administratorportal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e9328-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="e9328-130">-Path</span><span class="sxs-lookup"><span data-stu-id="e9328-130">-Path</span></span>
<span data-ttu-id="e9328-131">Gibt den WebAPI-Pfad an, bei dem es sich um den letzten Teil der öffentlichen URL der API handelt, der dem Feld "URL-Suffix" für WebAPI im Administratorportal entspricht.</span><span class="sxs-lookup"><span data-stu-id="e9328-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="e9328-132">Diese URL wird von API-Consumern verwendet, um Anforderungen an den Webdienst zu senden, und muss ein bis 400 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="e9328-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="e9328-133">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="e9328-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="e9328-134">-ProductIDs</span><span class="sxs-lookup"><span data-stu-id="e9328-134">-ProductIds</span></span>
<span data-ttu-id="e9328-135">Gibt ein Array von Produkt-IDs an, dem die neue API hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9328-135">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="e9328-136">-Protokolle</span><span class="sxs-lookup"><span data-stu-id="e9328-136">-Protocols</span></span>
<span data-ttu-id="e9328-137">Gibt ein Array von Web-API-Protokollen an.</span><span class="sxs-lookup"><span data-stu-id="e9328-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="e9328-138">Gültige Werte sind http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e9328-138">Valid values are http, https.</span></span>
<span data-ttu-id="e9328-139">Hierbei handelt es sich um die Webprotokolle, über die die API zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e9328-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="e9328-140">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="e9328-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="e9328-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="e9328-141">-ServiceUrl</span></span>
<span data-ttu-id="e9328-142">Gibt die URL des Webdiensts an, der die API verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="e9328-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="e9328-143">Diese URL wird nur von der Azure-API-Verwaltung verwendet und nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="e9328-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="e9328-144">Die URL muss ein bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="e9328-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="e9328-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="e9328-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="e9328-146">Gibt den Namen des Abonnementschlüssel Headers an.</span><span class="sxs-lookup"><span data-stu-id="e9328-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="e9328-147">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="e9328-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="e9328-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="e9328-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="e9328-149">Gibt den Abfragezeichenfolgenparameter Namen für den Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="e9328-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="e9328-150">Der Standardwert ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="e9328-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="e9328-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9328-151">CommonParameters</span></span>
<span data-ttu-id="e9328-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9328-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9328-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9328-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9328-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9328-154">INPUTS</span></span>

### <span data-ttu-id="e9328-155">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e9328-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e9328-156">System. String</span><span class="sxs-lookup"><span data-stu-id="e9328-156">System.String</span></span>

### <span data-ttu-id="e9328-157">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="e9328-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="e9328-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="e9328-158">System.String[]</span></span>

## <span data-ttu-id="e9328-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9328-159">OUTPUTS</span></span>

### <span data-ttu-id="e9328-160">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e9328-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e9328-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9328-161">NOTES</span></span>

## <span data-ttu-id="e9328-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9328-162">RELATED LINKS</span></span>

[<span data-ttu-id="e9328-163">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e9328-163">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="e9328-164">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e9328-164">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="e9328-165">Importieren-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e9328-165">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="e9328-166">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e9328-166">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="e9328-167">Satz-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e9328-167">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


