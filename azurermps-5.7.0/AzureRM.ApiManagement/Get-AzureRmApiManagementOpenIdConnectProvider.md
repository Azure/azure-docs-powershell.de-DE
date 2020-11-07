---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c26fb8991acc47ab655cb47c44194ca209423a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663799"
---
# <span data-ttu-id="23e1c-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="23e1c-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="23e1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="23e1c-103">Ruft OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="23e1c-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23e1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23e1c-104">SYNTAX</span></span>

### <span data-ttu-id="23e1c-105">GetAllOpenIdConnectProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="23e1c-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23e1c-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="23e1c-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23e1c-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="23e1c-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23e1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="23e1c-109">Das Cmdlet " **Get-AzureRmApiManagementOpenIdConnectProvider** " erhält OpenID Connect-Anbieter in der Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="23e1c-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="23e1c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="23e1c-111">Beispiel 1: Abrufen aller Anbieter</span><span class="sxs-lookup"><span data-stu-id="23e1c-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="23e1c-112">Dieser Befehl ruft alle OpenID Connect-Anbieter für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="23e1c-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="23e1c-113">Beispiel 2: Abrufen eines Anbieters mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="23e1c-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="23e1c-114">Dieser Befehl ruft den Anbieter ab, der die ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="23e1c-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="23e1c-115">Beispiel 3: Abrufen eines Anbieters mit einem Namen</span><span class="sxs-lookup"><span data-stu-id="23e1c-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="23e1c-116">Dieser Befehl ruft den Anbieter mit dem Namen contoso OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="23e1c-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="23e1c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="23e1c-117">PARAMETERS</span></span>

### <span data-ttu-id="23e1c-118">-Context</span><span class="sxs-lookup"><span data-stu-id="23e1c-118">-Context</span></span>
<span data-ttu-id="23e1c-119">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="23e1c-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="23e1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e1c-120">-DefaultProfile</span></span>
<span data-ttu-id="23e1c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23e1c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="23e1c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="23e1c-122">-Name</span></span>
<span data-ttu-id="23e1c-123">Gibt einen Anzeigenamen eines Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="23e1c-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="23e1c-124">Wenn Sie einen Namen angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="23e1c-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e1c-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="23e1c-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="23e1c-126">Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="23e1c-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="23e1c-127">Wenn Sie eine ID angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="23e1c-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e1c-128">CommonParameters</span></span>
<span data-ttu-id="23e1c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e1c-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e1c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e1c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23e1c-131">INPUTS</span></span>

### <span data-ttu-id="23e1c-132">Keine</span><span class="sxs-lookup"><span data-stu-id="23e1c-132">None</span></span>
<span data-ttu-id="23e1c-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="23e1c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23e1c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23e1c-134">OUTPUTS</span></span>

### <span data-ttu-id="23e1c-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="23e1c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>
<span data-ttu-id="23e1c-136">Das Detail des im API-Verwaltungsdienst konfigurierten OpenID Connect-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="23e1c-136">The detail of the OpenId connect Provider configured in API Management service.</span></span>

### <span data-ttu-id="23e1c-137">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="23e1c-137">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>
<span data-ttu-id="23e1c-138">Die Liste der OpenID Connect-Anbieter, die im API-Verwaltungsdienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="23e1c-138">The list of OpenId Connect Providers configured in API Management service.</span></span>

## <span data-ttu-id="23e1c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="23e1c-139">NOTES</span></span>

## <span data-ttu-id="23e1c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23e1c-140">RELATED LINKS</span></span>

[<span data-ttu-id="23e1c-141">Neu – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="23e1c-141">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="23e1c-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="23e1c-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="23e1c-143">Satz-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="23e1c-143">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


