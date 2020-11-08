---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008224"
---
# <span data-ttu-id="a8996-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="a8996-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="a8996-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8996-102">SYNOPSIS</span></span>
<span data-ttu-id="a8996-103">Ruft den OpenID Connect-Anbieter Client Secret ab.</span><span class="sxs-lookup"><span data-stu-id="a8996-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="a8996-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8996-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8996-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8996-105">DESCRIPTION</span></span>
<span data-ttu-id="a8996-106">Ruft den OpenID Connect-Anbieter Client Secret ab.</span><span class="sxs-lookup"><span data-stu-id="a8996-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="a8996-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8996-107">EXAMPLES</span></span>

### <span data-ttu-id="a8996-108">Beispiel 1: Abrufen eines Anbieter Client Geheimnisses mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="a8996-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="a8996-109">Dieser Befehl ruft einen Client Schlüssel des Anbieters ab, der die ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="a8996-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="a8996-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8996-110">PARAMETERS</span></span>

### <span data-ttu-id="a8996-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a8996-111">-Context</span></span>
<span data-ttu-id="a8996-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a8996-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a8996-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8996-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a8996-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8996-114">-DefaultProfile</span></span>
<span data-ttu-id="a8996-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8996-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8996-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="a8996-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="a8996-117">Bezeichner eines OpenID Connect-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="a8996-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="a8996-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8996-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a8996-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8996-119">CommonParameters</span></span>
<span data-ttu-id="a8996-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8996-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8996-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8996-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8996-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8996-122">INPUTS</span></span>

### <span data-ttu-id="a8996-123">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a8996-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a8996-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a8996-124">System.String</span></span>

## <span data-ttu-id="a8996-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8996-125">OUTPUTS</span></span>

### <span data-ttu-id="a8996-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="a8996-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="a8996-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8996-127">NOTES</span></span>

## <span data-ttu-id="a8996-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8996-128">RELATED LINKS</span></span>
