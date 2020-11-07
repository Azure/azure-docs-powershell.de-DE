---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: b6c8c0260e1f45b55dedca4d0a9f1f5ab3fed59a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650384"
---
# <span data-ttu-id="52392-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="52392-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="52392-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52392-102">SYNOPSIS</span></span>
<span data-ttu-id="52392-103">Ruft OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="52392-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="52392-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52392-104">SYNTAX</span></span>

### <span data-ttu-id="52392-105">GetAllOpenIdConnectProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="52392-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52392-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="52392-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52392-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="52392-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52392-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52392-108">DESCRIPTION</span></span>
<span data-ttu-id="52392-109">Das Cmdlet " **Get-AzApiManagementOpenIdConnectProvider** " erhält OpenID Connect-Anbieter in der Azure-API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="52392-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="52392-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52392-110">EXAMPLES</span></span>

### <span data-ttu-id="52392-111">Beispiel 1: Abrufen aller Anbieter</span><span class="sxs-lookup"><span data-stu-id="52392-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="52392-112">Dieser Befehl ruft alle OpenID Connect-Anbieter für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="52392-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="52392-113">Beispiel 2: Abrufen eines Anbieters mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="52392-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="52392-114">Dieser Befehl ruft den Anbieter ab, der die ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="52392-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="52392-115">Beispiel 3: Abrufen eines Anbieters mit einem Namen</span><span class="sxs-lookup"><span data-stu-id="52392-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="52392-116">Dieser Befehl ruft den Anbieter mit dem Namen contoso OpenID Connect-Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="52392-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="52392-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="52392-117">PARAMETERS</span></span>

### <span data-ttu-id="52392-118">-Context</span><span class="sxs-lookup"><span data-stu-id="52392-118">-Context</span></span>
<span data-ttu-id="52392-119">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="52392-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="52392-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52392-120">-DefaultProfile</span></span>
<span data-ttu-id="52392-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52392-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52392-122">-Name</span><span class="sxs-lookup"><span data-stu-id="52392-122">-Name</span></span>
<span data-ttu-id="52392-123">Gibt einen Anzeigenamen eines Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="52392-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="52392-124">Wenn Sie einen Namen angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="52392-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="52392-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="52392-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="52392-126">Gibt eine ID des Anbieters an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="52392-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="52392-127">Wenn Sie eine ID angeben, ruft dieses Cmdlet diesen Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="52392-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="52392-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52392-128">CommonParameters</span></span>
<span data-ttu-id="52392-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52392-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52392-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52392-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52392-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52392-131">INPUTS</span></span>

### <span data-ttu-id="52392-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="52392-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="52392-133">System. String</span><span class="sxs-lookup"><span data-stu-id="52392-133">System.String</span></span>

## <span data-ttu-id="52392-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52392-134">OUTPUTS</span></span>

### <span data-ttu-id="52392-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="52392-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="52392-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="52392-136">NOTES</span></span>

## <span data-ttu-id="52392-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52392-137">RELATED LINKS</span></span>

[<span data-ttu-id="52392-138">Neu – AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="52392-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="52392-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="52392-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="52392-140">Satz-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="52392-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


