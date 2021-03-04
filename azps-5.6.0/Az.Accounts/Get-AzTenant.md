---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 4ef371f26eeca71edda42a6aca5e7d5ad28fe753
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920131"
---
# <span data-ttu-id="9f362-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="9f362-101">Get-AzTenant</span></span>

## <span data-ttu-id="9f362-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f362-102">SYNOPSIS</span></span>
<span data-ttu-id="9f362-103">Ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="9f362-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="9f362-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f362-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f362-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f362-105">DESCRIPTION</span></span>
<span data-ttu-id="9f362-106">Das Get-AzTenant cmdlet erhält Mandanten, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="9f362-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="9f362-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9f362-107">EXAMPLES</span></span>

### <span data-ttu-id="9f362-108">Beispiel 1: Abrufen aller Mandanten</span><span class="sxs-lookup"><span data-stu-id="9f362-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="9f362-109">In diesem Beispiel wird gezeigt, wie Sie alle autorisierten Mandanten eines Azure-Kontos erhalten.</span><span class="sxs-lookup"><span data-stu-id="9f362-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="9f362-110">Beispiel 2: Abrufen eines bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="9f362-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="9f362-111">In diesem Beispiel wird gezeigt, wie Sie einen bestimmten autorisierten Mandanten eines Azure-Kontos erhalten.</span><span class="sxs-lookup"><span data-stu-id="9f362-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="9f362-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9f362-112">PARAMETERS</span></span>

### <span data-ttu-id="9f362-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f362-113">-DefaultProfile</span></span>
<span data-ttu-id="9f362-114">Die Anmeldeinformationen, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9f362-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f362-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="9f362-115">-TenantId</span></span>
<span data-ttu-id="9f362-116">Gibt die ID des Mandanten an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9f362-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f362-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f362-117">CommonParameters</span></span>
<span data-ttu-id="9f362-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f362-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f362-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f362-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f362-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9f362-120">INPUTS</span></span>

### <span data-ttu-id="9f362-121">System.String</span><span class="sxs-lookup"><span data-stu-id="9f362-121">System.String</span></span>

## <span data-ttu-id="9f362-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9f362-122">OUTPUTS</span></span>

### <span data-ttu-id="9f362-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="9f362-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="9f362-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9f362-124">NOTES</span></span>

## <span data-ttu-id="9f362-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9f362-125">RELATED LINKS</span></span>
