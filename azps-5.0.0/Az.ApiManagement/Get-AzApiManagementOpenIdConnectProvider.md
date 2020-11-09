---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303879"
---
# <span data-ttu-id="75f32-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="75f32-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="75f32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75f32-102">SYNOPSIS</span></span>
<span data-ttu-id="75f32-103">Ruft OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="75f32-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="75f32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75f32-104">SYNTAX</span></span>

### <span data-ttu-id="75f32-105">GetAllOpenIdConnectProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="75f32-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75f32-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="75f32-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75f32-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="75f32-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f32-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75f32-108">DESCRIPTION</span></span>
<span data-ttu-id="75f32-109">Das Cmdlet " **Get-AzApiManagementOpenIdConnectProvider** " erhält OpenID Connect-Anbieter in der Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="75f32-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="75f32-110">ClientSecret wird nicht in Ergebnisdetails eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="75f32-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="75f32-111">Verwenden **Sie Get-AzApiManagementOpenIdConnectProviderClientSecret** , um Client Secret zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="75f32-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="75f32-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75f32-112">EXAMPLES</span></span>

### <span data-ttu-id="75f32-113">Beispiel 1: Abrufen aller Anbieter</span><span class="sxs-lookup"><span data-stu-id="75f32-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="75f32-114">Dieser Befehl ruft alle OpenID Connect-Anbieter für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="75f32-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="75f32-115">Beispiel 2: Abrufen eines Anbieters mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="75f32-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="75f32-116">Dieser Befehl ruft den Anbieter ab, der die ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="75f32-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="75f32-117">Beispiel 3: Abrufen eines Anbieters mit einem Namen</span><span class="sxs-lookup"><span data-stu-id="75f32-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="75f32-118">Dieser Befehl ruft den Anbieter mit dem Namen contoso OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="75f32-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="75f32-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="75f32-119">PARAMETERS</span></span>

### <span data-ttu-id="75f32-120">-Context</span><span class="sxs-lookup"><span data-stu-id="75f32-120">-Context</span></span>
<span data-ttu-id="75f32-121">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="75f32-121">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75f32-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f32-122">-DefaultProfile</span></span>
<span data-ttu-id="75f32-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75f32-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75f32-124">-Name</span><span class="sxs-lookup"><span data-stu-id="75f32-124">-Name</span></span>
<span data-ttu-id="75f32-125">Gibt einen Anzeigenamen eines Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="75f32-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="75f32-126">Wenn Sie einen Namen angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="75f32-126">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f32-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="75f32-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="75f32-128">Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="75f32-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="75f32-129">Wenn Sie eine ID angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="75f32-129">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f32-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f32-130">CommonParameters</span></span>
<span data-ttu-id="75f32-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f32-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f32-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75f32-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f32-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75f32-133">INPUTS</span></span>

### <span data-ttu-id="75f32-134">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="75f32-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="75f32-135">System. String</span><span class="sxs-lookup"><span data-stu-id="75f32-135">System.String</span></span>

## <span data-ttu-id="75f32-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75f32-136">OUTPUTS</span></span>

### <span data-ttu-id="75f32-137">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="75f32-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="75f32-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="75f32-138">NOTES</span></span>

## <span data-ttu-id="75f32-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75f32-139">RELATED LINKS</span></span>

[<span data-ttu-id="75f32-140">Neu – AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="75f32-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="75f32-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="75f32-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="75f32-142">Satz-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="75f32-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


