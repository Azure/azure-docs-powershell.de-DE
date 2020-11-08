---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176694"
---
# <span data-ttu-id="0c176-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="0c176-101">Get-AzTenant</span></span>

## <span data-ttu-id="0c176-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c176-102">SYNOPSIS</span></span>
<span data-ttu-id="0c176-103">Ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="0c176-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="0c176-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c176-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c176-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c176-105">DESCRIPTION</span></span>
<span data-ttu-id="0c176-106">Das Get-AzTenant-Cmdlet ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="0c176-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="0c176-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c176-107">EXAMPLES</span></span>

### <span data-ttu-id="0c176-108">Beispiel 1: Abrufen aller Mandanten</span><span class="sxs-lookup"><span data-stu-id="0c176-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="0c176-109">In diesem Beispiel wird gezeigt, wie Sie alle autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="0c176-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="0c176-110">Beispiel 2: Abrufen eines bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="0c176-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="0c176-111">In diesem Beispiel wird gezeigt, wie Sie einen bestimmten autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="0c176-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="0c176-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c176-112">PARAMETERS</span></span>

### <span data-ttu-id="0c176-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c176-113">-DefaultProfile</span></span>
<span data-ttu-id="0c176-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="0c176-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c176-115">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="0c176-115">-TenantId</span></span>
<span data-ttu-id="0c176-116">Gibt die ID des Mandanten an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0c176-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0c176-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c176-117">CommonParameters</span></span>
<span data-ttu-id="0c176-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c176-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c176-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c176-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c176-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c176-120">INPUTS</span></span>

### <span data-ttu-id="0c176-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0c176-121">System.String</span></span>

## <span data-ttu-id="0c176-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c176-122">OUTPUTS</span></span>

### <span data-ttu-id="0c176-123">Microsoft. Azure. Commands. profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="0c176-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="0c176-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c176-124">NOTES</span></span>

## <span data-ttu-id="0c176-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c176-125">RELATED LINKS</span></span>
