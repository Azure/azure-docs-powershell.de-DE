---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c19888bd45ae943b60b90172913a83f42a1fd6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945436"
---
# <span data-ttu-id="88109-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="88109-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="88109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88109-102">SYNOPSIS</span></span>
<span data-ttu-id="88109-103">Ruft die Zugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="88109-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="88109-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88109-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88109-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88109-105">DESCRIPTION</span></span>
<span data-ttu-id="88109-106">Das **Get-AzApiManagementTenantAccess-Cmdlet** ruft die Mandantenzugriffskonfiguration für einen Mandanten ab.</span><span class="sxs-lookup"><span data-stu-id="88109-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="88109-107">Schlüssel werden nicht in ergebnisdetails einbezogen.</span><span class="sxs-lookup"><span data-stu-id="88109-107">Keys will not be included into result details.</span></span> <span data-ttu-id="88109-108">Verwenden Sie **Get-AzApiManagementTenantAccessSecret,** um den Geheimtipp des Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88109-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="88109-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88109-109">EXAMPLES</span></span>

### <span data-ttu-id="88109-110">Beispiel 1: Konfiguration des Mandantenzugriffs</span><span class="sxs-lookup"><span data-stu-id="88109-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="88109-111">Dieser Befehl ruft die Mandantenzugriffskonfiguration für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="88109-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="88109-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="88109-112">PARAMETERS</span></span>

### <span data-ttu-id="88109-113">-Context</span><span class="sxs-lookup"><span data-stu-id="88109-113">-Context</span></span>
<span data-ttu-id="88109-114">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="88109-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="88109-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88109-115">-DefaultProfile</span></span>
<span data-ttu-id="88109-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88109-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88109-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88109-117">CommonParameters</span></span>
<span data-ttu-id="88109-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88109-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88109-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88109-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88109-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88109-120">INPUTS</span></span>

### <span data-ttu-id="88109-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="88109-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="88109-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88109-122">OUTPUTS</span></span>

### <span data-ttu-id="88109-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="88109-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="88109-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="88109-124">NOTES</span></span>

## <span data-ttu-id="88109-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="88109-125">RELATED LINKS</span></span>

[<span data-ttu-id="88109-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="88109-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


