---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007265"
---
# <span data-ttu-id="e0b1b-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0b1b-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="e0b1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b1b-103">Abrufen einer Liste aller Lasten ausgleichsgeräte</span><span class="sxs-lookup"><span data-stu-id="e0b1b-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="e0b1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0b1b-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e0b1b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b1b-106">Abrufen einer Liste aller Lasten ausgleichsgeräte</span><span class="sxs-lookup"><span data-stu-id="e0b1b-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="e0b1b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0b1b-107">EXAMPLES</span></span>

### <span data-ttu-id="e0b1b-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e0b1b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="e0b1b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b1b-109">PARAMETERS</span></span>

### <span data-ttu-id="e0b1b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b1b-110">-DefaultProfile</span></span>
<span data-ttu-id="e0b1b-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0b1b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b1b-112">-Filter</span><span class="sxs-lookup"><span data-stu-id="e0b1b-112">-Filter</span></span>
<span data-ttu-id="e0b1b-113">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="e0b1b-113">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0b1b-114">-Inline count</span><span class="sxs-lookup"><span data-stu-id="e0b1b-114">-InlineCount</span></span>
<span data-ttu-id="e0b1b-115">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b1b-115">OData inline count parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0b1b-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e0b1b-116">-OrderBy</span></span>
<span data-ttu-id="e0b1b-117">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b1b-117">OData orderBy parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0b1b-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="e0b1b-118">-Skip</span></span>
<span data-ttu-id="e0b1b-119">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="e0b1b-119">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0b1b-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e0b1b-120">-SubscriptionId</span></span>
<span data-ttu-id="e0b1b-121">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e0b1b-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e0b1b-122">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e0b1b-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e0b1b-123">-Top</span><span class="sxs-lookup"><span data-stu-id="e0b1b-123">-Top</span></span>
<span data-ttu-id="e0b1b-124">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="e0b1b-124">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0b1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b1b-125">CommonParameters</span></span>
<span data-ttu-id="e0b1b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b1b-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0b1b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b1b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0b1b-128">INPUTS</span></span>

## <span data-ttu-id="e0b1b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0b1b-129">OUTPUTS</span></span>

### <span data-ttu-id="e0b1b-130">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. ILoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0b1b-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="e0b1b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0b1b-131">NOTES</span></span>

## <span data-ttu-id="e0b1b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0b1b-132">RELATED LINKS</span></span>

