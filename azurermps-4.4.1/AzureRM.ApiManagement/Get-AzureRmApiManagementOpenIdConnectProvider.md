---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477454"
---
# <span data-ttu-id="5dec7-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5dec7-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5dec7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5dec7-102">SYNOPSIS</span></span>
<span data-ttu-id="5dec7-103">Ruft OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="5dec7-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dec7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dec7-104">SYNTAX</span></span>

### <span data-ttu-id="5dec7-105">Alle OpenID Connect-Anbieter abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="5dec7-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dec7-106">Erhalten Sie von der OpenID Connect-Anbieter-ID</span><span class="sxs-lookup"><span data-stu-id="5dec7-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dec7-107">Suchen nach dem OpenID Connect-Anbieter Anzeigenamen</span><span class="sxs-lookup"><span data-stu-id="5dec7-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dec7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dec7-108">DESCRIPTION</span></span>
<span data-ttu-id="5dec7-109">Das Cmdlet " **Get-AzureRmApiManagementOpenIdConnectProvider** " erhält OpenID Connect-Anbieter in der Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="5dec7-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="5dec7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5dec7-110">EXAMPLES</span></span>

### <span data-ttu-id="5dec7-111">Beispiel 1: Abrufen aller Anbieter</span><span class="sxs-lookup"><span data-stu-id="5dec7-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="5dec7-112">Dieser Befehl ruft alle OpenID Connect-Anbieter für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="5dec7-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="5dec7-113">Beispiel 2: Abrufen eines Anbieters mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="5dec7-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="5dec7-114">Dieser Befehl ruft den Anbieter ab, der die ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="5dec7-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="5dec7-115">Beispiel 3: Abrufen eines Anbieters mit einem Namen</span><span class="sxs-lookup"><span data-stu-id="5dec7-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="5dec7-116">Dieser Befehl ruft den Anbieter mit dem Namen contoso OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="5dec7-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="5dec7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dec7-117">PARAMETERS</span></span>

### <span data-ttu-id="5dec7-118">-Context</span><span class="sxs-lookup"><span data-stu-id="5dec7-118">-Context</span></span>
<span data-ttu-id="5dec7-119">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5dec7-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5dec7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5dec7-120">-Name</span></span>
<span data-ttu-id="5dec7-121">Gibt einen Anzeigenamen eines Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="5dec7-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="5dec7-122">Wenn Sie einen Namen angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="5dec7-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dec7-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5dec7-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5dec7-124">Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="5dec7-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="5dec7-125">Wenn Sie eine ID angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="5dec7-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dec7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dec7-126">-DefaultProfile</span></span>
<span data-ttu-id="5dec7-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5dec7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dec7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dec7-128">CommonParameters</span></span>
<span data-ttu-id="5dec7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dec7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dec7-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dec7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dec7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5dec7-131">INPUTS</span></span>

## <span data-ttu-id="5dec7-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5dec7-132">OUTPUTS</span></span>

### <span data-ttu-id="5dec7-133">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="5dec7-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="5dec7-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="5dec7-134">NOTES</span></span>

## <span data-ttu-id="5dec7-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5dec7-135">RELATED LINKS</span></span>

[<span data-ttu-id="5dec7-136">Neu – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5dec7-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5dec7-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5dec7-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5dec7-138">Satz-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5dec7-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


