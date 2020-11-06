---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475049"
---
# <span data-ttu-id="a280d-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="a280d-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="a280d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a280d-102">SYNOPSIS</span></span>
<span data-ttu-id="a280d-103">Ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="a280d-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="a280d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a280d-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a280d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a280d-105">DESCRIPTION</span></span>
<span data-ttu-id="a280d-106">Das Get-AzureRmTenant-Cmdlet ruft Mandanten ab, die für den aktuellen Benutzer autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="a280d-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="a280d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a280d-107">EXAMPLES</span></span>

### <span data-ttu-id="a280d-108">Beispiel 1: Abrufen aller Mandanten</span><span class="sxs-lookup"><span data-stu-id="a280d-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="a280d-109">In diesem Beispiel wird gezeigt, wie Sie alle autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="a280d-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="a280d-110">Beispiel 2: Abrufen eines bestimmten Mandanten</span><span class="sxs-lookup"><span data-stu-id="a280d-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="a280d-111">In diesem Beispiel wird gezeigt, wie Sie einen bestimmten autorisierten Mandanten eines Azure-Kontos abrufen.</span><span class="sxs-lookup"><span data-stu-id="a280d-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="a280d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a280d-112">PARAMETERS</span></span>

### <span data-ttu-id="a280d-113">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="a280d-113">-TenantId</span></span>
<span data-ttu-id="a280d-114">Gibt die ID des Mandanten an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a280d-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a280d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a280d-115">CommonParameters</span></span>
<span data-ttu-id="a280d-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a280d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a280d-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a280d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a280d-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a280d-118">INPUTS</span></span>

## <span data-ttu-id="a280d-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a280d-119">OUTPUTS</span></span>

### <span data-ttu-id="a280d-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="a280d-120">PSAzureTenant</span></span>
<span data-ttu-id="a280d-121">Dieses Cmdlet gibt die Mandanten-ID und die zugehörigen Domäneninformationen für Mandanten zurück, die für das aktuelle Konto autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="a280d-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="a280d-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="a280d-122">NOTES</span></span>

## <span data-ttu-id="a280d-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a280d-123">RELATED LINKS</span></span>

