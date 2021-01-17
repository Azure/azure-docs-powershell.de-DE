---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370809"
---
# <span data-ttu-id="0f367-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="0f367-101">Get-AzTenant</span></span>

## <span data-ttu-id="0f367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f367-102">SYNOPSIS</span></span>
<span data-ttu-id="0f367-103">Ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="0f367-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="0f367-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f367-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f367-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f367-105">DESCRIPTION</span></span>
<span data-ttu-id="0f367-106">Das Get-AzTenant cmdlet bekommt Mandanten, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="0f367-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="0f367-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f367-107">EXAMPLES</span></span>

### <span data-ttu-id="0f367-108">Beispiel 1: Abrufen aller Mandanten</span><span class="sxs-lookup"><span data-stu-id="0f367-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="0f367-109">Dieses Beispiel zeigt, wie Sie alle autorisierten Mandanten eines Azure-Kontos erhalten.</span><span class="sxs-lookup"><span data-stu-id="0f367-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="0f367-110">Beispiel 2: Abrufen eines bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="0f367-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="0f367-111">Dieses Beispiel zeigt, wie Sie einen bestimmten autorisierten Mandanten eines Azure-Kontos erhalten.</span><span class="sxs-lookup"><span data-stu-id="0f367-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="0f367-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f367-112">PARAMETERS</span></span>

### <span data-ttu-id="0f367-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f367-113">-DefaultProfile</span></span>
<span data-ttu-id="0f367-114">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0f367-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f367-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="0f367-115">-TenantId</span></span>
<span data-ttu-id="0f367-116">Gibt die ID des Mandanten an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0f367-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0f367-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f367-117">CommonParameters</span></span>
<span data-ttu-id="0f367-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f367-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f367-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f367-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f367-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f367-120">INPUTS</span></span>

### <span data-ttu-id="0f367-121">System.String</span><span class="sxs-lookup"><span data-stu-id="0f367-121">System.String</span></span>

## <span data-ttu-id="0f367-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f367-122">OUTPUTS</span></span>

### <span data-ttu-id="0f367-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="0f367-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="0f367-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f367-124">NOTES</span></span>

## <span data-ttu-id="0f367-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f367-125">RELATED LINKS</span></span>
