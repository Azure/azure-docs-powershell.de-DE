---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 7764b9c1226d86e44631ed3114fffde5bddc21f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658453"
---
# <span data-ttu-id="79c9a-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="79c9a-101">Get-AzTenant</span></span>

## <span data-ttu-id="79c9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="79c9a-103">Ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="79c9a-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="79c9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c9a-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c9a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79c9a-105">DESCRIPTION</span></span>
<span data-ttu-id="79c9a-106">Das Get-AzTenant-Cmdlet ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="79c9a-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="79c9a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79c9a-107">EXAMPLES</span></span>

### <span data-ttu-id="79c9a-108">Beispiel 1: Abrufen aller Mandanten</span><span class="sxs-lookup"><span data-stu-id="79c9a-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="79c9a-109">In diesem Beispiel wird gezeigt, wie Sie alle autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="79c9a-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="79c9a-110">Beispiel 2: Abrufen eines bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="79c9a-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="79c9a-111">In diesem Beispiel wird gezeigt, wie Sie einen bestimmten autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="79c9a-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="79c9a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="79c9a-112">PARAMETERS</span></span>

### <span data-ttu-id="79c9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c9a-113">-DefaultProfile</span></span>
<span data-ttu-id="79c9a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="79c9a-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79c9a-115">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="79c9a-115">-TenantId</span></span>
<span data-ttu-id="79c9a-116">Gibt die ID des Mandanten an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="79c9a-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="79c9a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c9a-117">CommonParameters</span></span>
<span data-ttu-id="79c9a-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c9a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c9a-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c9a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c9a-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79c9a-120">INPUTS</span></span>

### <span data-ttu-id="79c9a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="79c9a-121">System.String</span></span>

## <span data-ttu-id="79c9a-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79c9a-122">OUTPUTS</span></span>

### <span data-ttu-id="79c9a-123">Microsoft. Azure. Commands. profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="79c9a-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="79c9a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="79c9a-124">NOTES</span></span>

## <span data-ttu-id="79c9a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79c9a-125">RELATED LINKS</span></span>
