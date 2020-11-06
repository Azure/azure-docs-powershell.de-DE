---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 8ac36dd86abb996a934b59d064980233c931d214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496958"
---
# <span data-ttu-id="78168-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="78168-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="78168-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78168-102">SYNOPSIS</span></span>
<span data-ttu-id="78168-103">Ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="78168-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78168-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78168-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78168-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78168-105">DESCRIPTION</span></span>
<span data-ttu-id="78168-106">Das Get-AzureRmTenant-Cmdlet ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="78168-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="78168-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78168-107">EXAMPLES</span></span>

### <span data-ttu-id="78168-108">Beispiel 1: Abrufen aller Mandanten</span><span class="sxs-lookup"><span data-stu-id="78168-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="78168-109">In diesem Beispiel wird gezeigt, wie Sie alle autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="78168-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="78168-110">Beispiel 2: Abrufen eines bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="78168-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="78168-111">In diesem Beispiel wird gezeigt, wie Sie einen bestimmten autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="78168-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="78168-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="78168-112">PARAMETERS</span></span>

### <span data-ttu-id="78168-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78168-113">-DefaultProfile</span></span>
<span data-ttu-id="78168-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="78168-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78168-115">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="78168-115">-TenantId</span></span>
<span data-ttu-id="78168-116">Gibt die ID des Mandanten an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="78168-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78168-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78168-117">CommonParameters</span></span>
<span data-ttu-id="78168-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78168-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78168-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78168-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78168-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78168-120">INPUTS</span></span>

## <span data-ttu-id="78168-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78168-121">OUTPUTS</span></span>

### <span data-ttu-id="78168-122">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="78168-122">PSAzureTenant</span></span>
<span data-ttu-id="78168-123">Dieses Cmdlet gibt die Mandanten-ID und die zugehörigen Domäneninformationen für Mandanten zurück, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="78168-123">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="78168-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="78168-124">NOTES</span></span>

## <span data-ttu-id="78168-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78168-125">RELATED LINKS</span></span>

