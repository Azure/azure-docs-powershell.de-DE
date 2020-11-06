---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498113"
---
# <span data-ttu-id="6f43a-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6f43a-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="6f43a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f43a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f43a-103">Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="6f43a-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f43a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f43a-104">SYNTAX</span></span>

### <span data-ttu-id="6f43a-105">AllIdentityProviders (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f43a-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f43a-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="6f43a-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f43a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f43a-107">DESCRIPTION</span></span>
<span data-ttu-id="6f43a-108">Rufen Sie die Konfigurationsdetails des Identitätsanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="6f43a-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="6f43a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f43a-109">EXAMPLES</span></span>

### <span data-ttu-id="6f43a-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6f43a-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="6f43a-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="6f43a-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

<span data-ttu-id="6f43a-112">Rufen Sie alle Identität Anbieterkonfiguration für den Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="6f43a-112">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="6f43a-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6f43a-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="6f43a-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="6f43a-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

<span data-ttu-id="6f43a-115">Ruft die Identität Anbieterkonfiguration von Azure Active Directory ab.</span><span class="sxs-lookup"><span data-stu-id="6f43a-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="6f43a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f43a-116">PARAMETERS</span></span>

### <span data-ttu-id="6f43a-117">-Context</span><span class="sxs-lookup"><span data-stu-id="6f43a-117">-Context</span></span>
<span data-ttu-id="6f43a-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6f43a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6f43a-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6f43a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="6f43a-120">-Typ</span><span class="sxs-lookup"><span data-stu-id="6f43a-120">-Type</span></span>
<span data-ttu-id="6f43a-121">Bezeichner eines Identitätsanbieters.</span><span class="sxs-lookup"><span data-stu-id="6f43a-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="6f43a-122">Wenn angegeben, wird versucht, die Konfiguration des Identitätsanbieters anhand des Bezeichners zu finden.</span><span class="sxs-lookup"><span data-stu-id="6f43a-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="6f43a-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6f43a-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f43a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f43a-124">-DefaultProfile</span></span>
<span data-ttu-id="6f43a-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f43a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f43a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f43a-126">CommonParameters</span></span>
<span data-ttu-id="6f43a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f43a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f43a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f43a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f43a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f43a-129">INPUTS</span></span>

## <span data-ttu-id="6f43a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f43a-130">OUTPUTS</span></span>

### <span data-ttu-id="6f43a-131">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="6f43a-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>

### <span data-ttu-id="6f43a-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6f43a-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="6f43a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f43a-133">NOTES</span></span>

## <span data-ttu-id="6f43a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f43a-134">RELATED LINKS</span></span>

