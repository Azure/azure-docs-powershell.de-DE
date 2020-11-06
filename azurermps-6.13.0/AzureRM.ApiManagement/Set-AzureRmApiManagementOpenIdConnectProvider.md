---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6f568f27cf5b50cd517d8133578d6cf36060252f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478049"
---
# <span data-ttu-id="2ff71-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2ff71-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2ff71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ff71-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff71-103">Ändert einen OpenID Connect-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2ff71-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ff71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ff71-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ff71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ff71-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff71-106">Das Cmdlet " **Satz-AzureRmApiManagementOpenIdConnectProvider** " ändert einen OpenID Connect-Anbieter in Azure API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="2ff71-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="2ff71-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ff71-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff71-108">Beispiel 1: Ändern des Client Geheimnisses für einen Anbieter</span><span class="sxs-lookup"><span data-stu-id="2ff71-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="2ff71-109">Dieser Befehl ändert den Anbieter mit der ID OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="2ff71-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="2ff71-110">Der Befehl gibt einen Client Schlüssel für den Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="2ff71-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="2ff71-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ff71-111">PARAMETERS</span></span>

### <span data-ttu-id="2ff71-112">-ClientID</span><span class="sxs-lookup"><span data-stu-id="2ff71-112">-ClientId</span></span>
<span data-ttu-id="2ff71-113">Gibt die Client-ID der Entwicklerkonsole an.</span><span class="sxs-lookup"><span data-stu-id="2ff71-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="2ff71-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="2ff71-114">-ClientSecret</span></span>
<span data-ttu-id="2ff71-115">Gibt den Client Schlüssel der Entwicklerkonsole an.</span><span class="sxs-lookup"><span data-stu-id="2ff71-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="2ff71-116">-Context</span><span class="sxs-lookup"><span data-stu-id="2ff71-116">-Context</span></span>
<span data-ttu-id="2ff71-117">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2ff71-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2ff71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff71-118">-DefaultProfile</span></span>
<span data-ttu-id="2ff71-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ff71-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ff71-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ff71-120">-Description</span></span>
<span data-ttu-id="2ff71-121">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="2ff71-121">Specifies a description.</span></span>

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

### <span data-ttu-id="2ff71-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="2ff71-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="2ff71-123">Gibt einen Metadaten-Endpunkt-URI des Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="2ff71-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="2ff71-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2ff71-124">-Name</span></span>
<span data-ttu-id="2ff71-125">Gibt einen Anzeigenamen für den Anbieter an.</span><span class="sxs-lookup"><span data-stu-id="2ff71-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="2ff71-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="2ff71-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="2ff71-127">Gibt eine ID für den Anbieter an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2ff71-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="2ff71-128">Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.</span><span class="sxs-lookup"><span data-stu-id="2ff71-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="2ff71-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ff71-129">-PassThru</span></span>
<span data-ttu-id="2ff71-130">Gibt an, dass dieses Cmdlet die **PsApiManagementOpenIdConnectProvider** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2ff71-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2ff71-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff71-131">CommonParameters</span></span>
<span data-ttu-id="2ff71-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff71-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff71-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff71-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff71-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ff71-134">INPUTS</span></span>

### <span data-ttu-id="2ff71-135">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2ff71-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2ff71-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2ff71-136">System.String</span></span>

### <span data-ttu-id="2ff71-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2ff71-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2ff71-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ff71-138">OUTPUTS</span></span>

### <span data-ttu-id="2ff71-139">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2ff71-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2ff71-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ff71-140">NOTES</span></span>

## <span data-ttu-id="2ff71-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ff71-141">RELATED LINKS</span></span>

[<span data-ttu-id="2ff71-142">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2ff71-142">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2ff71-143">Neu – AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2ff71-143">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2ff71-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2ff71-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


