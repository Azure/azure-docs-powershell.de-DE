---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 1d5312cfaf7afb96149ae00b0e7900905206fb3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495786"
---
# <span data-ttu-id="95ef5-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="95ef5-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="95ef5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="95ef5-103">Ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="95ef5-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95ef5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95ef5-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95ef5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95ef5-105">DESCRIPTION</span></span>
<span data-ttu-id="95ef5-106">Das Get-AzureRmTenant-Cmdlet ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="95ef5-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="95ef5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95ef5-107">EXAMPLES</span></span>

### <span data-ttu-id="95ef5-108">Beispiel 1: Abrufen aller Mandanten</span><span class="sxs-lookup"><span data-stu-id="95ef5-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy microsoft.com
```

<span data-ttu-id="95ef5-109">In diesem Beispiel wird gezeigt, wie Sie alle autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="95ef5-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="95ef5-110">Beispiel 2: Abrufen eines bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="95ef5-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Directory
--                                   ---------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx microsoft.com
```

<span data-ttu-id="95ef5-111">In diesem Beispiel wird gezeigt, wie Sie einen bestimmten autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="95ef5-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="95ef5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="95ef5-112">PARAMETERS</span></span>

### <span data-ttu-id="95ef5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ef5-113">-DefaultProfile</span></span>
<span data-ttu-id="95ef5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="95ef5-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95ef5-115">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="95ef5-115">-TenantId</span></span>
<span data-ttu-id="95ef5-116">Gibt die ID des Mandanten an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="95ef5-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="95ef5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ef5-117">CommonParameters</span></span>
<span data-ttu-id="95ef5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ef5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ef5-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ef5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ef5-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95ef5-120">INPUTS</span></span>

### <span data-ttu-id="95ef5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="95ef5-121">System.String</span></span>

## <span data-ttu-id="95ef5-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95ef5-122">OUTPUTS</span></span>

### <span data-ttu-id="95ef5-123">Microsoft. Azure. Commands. profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="95ef5-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="95ef5-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="95ef5-124">NOTES</span></span>

## <span data-ttu-id="95ef5-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95ef5-125">RELATED LINKS</span></span>
