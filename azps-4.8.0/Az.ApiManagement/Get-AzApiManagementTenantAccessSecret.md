---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009463"
---
# <span data-ttu-id="a855e-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="a855e-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="a855e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a855e-102">SYNOPSIS</span></span>
<span data-ttu-id="a855e-103">Ruft die Zugriffs Konfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="a855e-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="a855e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a855e-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a855e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a855e-105">DESCRIPTION</span></span>
<span data-ttu-id="a855e-106">Ruft die Zugriffs Konfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="a855e-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="a855e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a855e-107">EXAMPLES</span></span>

### <span data-ttu-id="a855e-108">Beispiel 1: Abrufen von Mandanten Zugriffs-Konfigurationsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="a855e-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="a855e-109">Dieser Befehl ruft die Konfigurationsschlüssel für den Mandanten Zugriff für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="a855e-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="a855e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a855e-110">PARAMETERS</span></span>

### <span data-ttu-id="a855e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a855e-111">-Context</span></span>
<span data-ttu-id="a855e-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a855e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a855e-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a855e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a855e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a855e-114">-DefaultProfile</span></span>
<span data-ttu-id="a855e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a855e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a855e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a855e-116">CommonParameters</span></span>
<span data-ttu-id="a855e-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a855e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a855e-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a855e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a855e-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a855e-119">INPUTS</span></span>

### <span data-ttu-id="a855e-120">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a855e-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="a855e-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a855e-121">OUTPUTS</span></span>

### <span data-ttu-id="a855e-122">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="a855e-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="a855e-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="a855e-123">NOTES</span></span>

## <span data-ttu-id="a855e-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a855e-124">RELATED LINKS</span></span>
