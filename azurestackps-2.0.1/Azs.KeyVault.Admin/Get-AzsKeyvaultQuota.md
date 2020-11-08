---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005422"
---
# <span data-ttu-id="dd841-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="dd841-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="dd841-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd841-102">SYNOPSIS</span></span>
<span data-ttu-id="dd841-103">Abrufen einer Liste aller Kontingent Objekte für keyvault an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="dd841-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="dd841-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd841-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd841-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd841-105">DESCRIPTION</span></span>
<span data-ttu-id="dd841-106">Abrufen einer Liste aller Kontingent Objekte für keyvault an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="dd841-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="dd841-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd841-107">EXAMPLES</span></span>

### <span data-ttu-id="dd841-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="dd841-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="dd841-109">Abrufen einer Liste aller Kontingent Objekte für keyvault an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="dd841-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="dd841-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd841-110">PARAMETERS</span></span>

### <span data-ttu-id="dd841-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd841-111">-DefaultProfile</span></span>
<span data-ttu-id="dd841-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd841-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd841-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="dd841-113">-Location</span></span>
<span data-ttu-id="dd841-114">Der Speicherort des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="dd841-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd841-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="dd841-115">-SubscriptionId</span></span>
<span data-ttu-id="dd841-116">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="dd841-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dd841-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd841-117">CommonParameters</span></span>
<span data-ttu-id="dd841-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd841-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd841-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd841-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd841-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd841-120">INPUTS</span></span>

## <span data-ttu-id="dd841-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd841-121">OUTPUTS</span></span>

### <span data-ttu-id="dd841-122">Microsoft. Azure. PowerShell. Cmdlets. KeyVaultAdmin. Models. Api20170201Preview. IQuota</span><span class="sxs-lookup"><span data-stu-id="dd841-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="dd841-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd841-123">NOTES</span></span>

## <span data-ttu-id="dd841-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd841-124">RELATED LINKS</span></span>

