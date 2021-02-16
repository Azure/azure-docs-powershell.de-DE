---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154937"
---
# <span data-ttu-id="1a762-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="1a762-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="1a762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a762-102">SYNOPSIS</span></span>
<span data-ttu-id="1a762-103">Ruft die Zugriffskonfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="1a762-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="1a762-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a762-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a762-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a762-105">DESCRIPTION</span></span>
<span data-ttu-id="1a762-106">Ruft die Zugriffskonfigurationsschlüssel für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="1a762-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="1a762-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a762-107">EXAMPLES</span></span>

### <span data-ttu-id="1a762-108">Beispiel 1: Erhalten von Konfigurationsschlüsseln für den Mandantenzugriff</span><span class="sxs-lookup"><span data-stu-id="1a762-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="1a762-109">Dieser Befehl ruft die Konfigurationsschlüssel für den Mandantenzugriff für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="1a762-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="1a762-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a762-110">PARAMETERS</span></span>

### <span data-ttu-id="1a762-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1a762-111">-Context</span></span>
<span data-ttu-id="1a762-112">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1a762-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1a762-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1a762-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1a762-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a762-114">-DefaultProfile</span></span>
<span data-ttu-id="1a762-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a762-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a762-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a762-116">CommonParameters</span></span>
<span data-ttu-id="1a762-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a762-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a762-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a762-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a762-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a762-119">INPUTS</span></span>

### <span data-ttu-id="1a762-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1a762-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="1a762-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a762-121">OUTPUTS</span></span>

### <span data-ttu-id="1a762-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="1a762-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="1a762-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a762-123">NOTES</span></span>

## <span data-ttu-id="1a762-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a762-124">RELATED LINKS</span></span>
