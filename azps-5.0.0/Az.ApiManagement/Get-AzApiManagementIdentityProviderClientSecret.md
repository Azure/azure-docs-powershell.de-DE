---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299896"
---
# <span data-ttu-id="90be1-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="90be1-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="90be1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90be1-102">SYNOPSIS</span></span>
<span data-ttu-id="90be1-103">Rufen Sie den Identitätsanbieter-Client Secret ab.</span><span class="sxs-lookup"><span data-stu-id="90be1-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="90be1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90be1-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90be1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90be1-105">DESCRIPTION</span></span>
<span data-ttu-id="90be1-106">Rufen Sie den Identitätsanbieter-Client Secret ab.</span><span class="sxs-lookup"><span data-stu-id="90be1-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="90be1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90be1-107">EXAMPLES</span></span>

### <span data-ttu-id="90be1-108">Beispiel 1: Abrufen des Client Geheimnisses des Aad-Typ-Identitätsanbieters</span><span class="sxs-lookup"><span data-stu-id="90be1-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="90be1-109">Ruft den Client Schlüssel der Identität Anbieterkonfiguration von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="90be1-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="90be1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90be1-110">PARAMETERS</span></span>

### <span data-ttu-id="90be1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="90be1-111">-Context</span></span>
<span data-ttu-id="90be1-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="90be1-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="90be1-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="90be1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="90be1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90be1-114">-DefaultProfile</span></span>
<span data-ttu-id="90be1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90be1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90be1-116">-Typ</span><span class="sxs-lookup"><span data-stu-id="90be1-116">-Type</span></span>
<span data-ttu-id="90be1-117">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="90be1-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="90be1-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="90be1-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90be1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90be1-119">CommonParameters</span></span>
<span data-ttu-id="90be1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90be1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90be1-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90be1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90be1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90be1-122">INPUTS</span></span>

### <span data-ttu-id="90be1-123">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90be1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="90be1-124">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="90be1-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="90be1-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90be1-125">OUTPUTS</span></span>

### <span data-ttu-id="90be1-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="90be1-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="90be1-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="90be1-127">NOTES</span></span>

## <span data-ttu-id="90be1-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90be1-128">RELATED LINKS</span></span>
