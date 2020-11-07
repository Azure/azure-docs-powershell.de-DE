---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c338cd8b2ea3ce2a464a7975ecac959bc1e52140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663398"
---
# <span data-ttu-id="2e0d0-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2e0d0-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2e0d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e0d0-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0d0-103">Erstellt einen OpenID Connect-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e0d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e0d0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e0d0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e0d0-105">DESCRIPTION</span></span>
<span data-ttu-id="2e0d0-106">Das Cmdlet **New-AzureRmApiManagementOpenIdConnectProvider** erstellt einen OpenID Connect-Anbieter in Azure API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="2e0d0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e0d0-107">EXAMPLES</span></span>

### <span data-ttu-id="2e0d0-108">Beispiel 1: Erstellen eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="2e0d0-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="2e0d0-109">Dieser Befehl erstellt einen OpenID Connect- **Anbieter** namens Contoso OpenID Connect-Anbieter</span><span class="sxs-lookup"><span data-stu-id="2e0d0-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="2e0d0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e0d0-110">PARAMETERS</span></span>

### <span data-ttu-id="2e0d0-111">-ClientID</span><span class="sxs-lookup"><span data-stu-id="2e0d0-111">-ClientId</span></span>
<span data-ttu-id="2e0d0-112">Gibt die Client-ID der Entwicklerkonsole an.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="2e0d0-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="2e0d0-113">-ClientSecret</span></span>
<span data-ttu-id="2e0d0-114">Gibt den Client Schlüssel der Entwicklerkonsole an.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="2e0d0-115">-Context</span><span class="sxs-lookup"><span data-stu-id="2e0d0-115">-Context</span></span>
<span data-ttu-id="2e0d0-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e0d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0d0-117">-DefaultProfile</span></span>
<span data-ttu-id="2e0d0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e0d0-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e0d0-119">-Description</span></span>
<span data-ttu-id="2e0d0-120">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-120">Specifies a description.</span></span>

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

### <span data-ttu-id="2e0d0-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="2e0d0-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="2e0d0-122">Gibt einen Metadaten-Endpunkt-URI des Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="2e0d0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2e0d0-123">-Name</span></span>
<span data-ttu-id="2e0d0-124">Gibt einen Anzeigenamen für den Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="2e0d0-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="2e0d0-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="2e0d0-126">Gibt eine ID für den Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="2e0d0-127">Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="2e0d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0d0-128">CommonParameters</span></span>
<span data-ttu-id="2e0d0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e0d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0d0-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e0d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0d0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e0d0-131">INPUTS</span></span>

### <span data-ttu-id="2e0d0-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e0d0-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e0d0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2e0d0-133">System.String</span></span>

## <span data-ttu-id="2e0d0-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e0d0-134">OUTPUTS</span></span>

### <span data-ttu-id="2e0d0-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2e0d0-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2e0d0-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e0d0-136">NOTES</span></span>

## <span data-ttu-id="2e0d0-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e0d0-137">RELATED LINKS</span></span>

[<span data-ttu-id="2e0d0-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2e0d0-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2e0d0-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2e0d0-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2e0d0-140">Satz-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2e0d0-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


