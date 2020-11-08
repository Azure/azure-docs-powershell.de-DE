---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005469"
---
# <span data-ttu-id="204f2-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="204f2-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="204f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="204f2-102">SYNOPSIS</span></span>
<span data-ttu-id="204f2-103">Abrufen einer Liste aller virtuellen Netzwerke</span><span class="sxs-lookup"><span data-stu-id="204f2-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="204f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="204f2-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="204f2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="204f2-105">DESCRIPTION</span></span>
<span data-ttu-id="204f2-106">Abrufen einer Liste aller virtuellen Netzwerke</span><span class="sxs-lookup"><span data-stu-id="204f2-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="204f2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="204f2-107">EXAMPLES</span></span>

### <span data-ttu-id="204f2-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="204f2-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="204f2-109">Gibt eine Liste der virtuellen Netzwerke für den Azure-Stapel Stempel zurück.</span><span class="sxs-lookup"><span data-stu-id="204f2-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="204f2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="204f2-110">PARAMETERS</span></span>

### <span data-ttu-id="204f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="204f2-111">-DefaultProfile</span></span>
<span data-ttu-id="204f2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="204f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="204f2-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="204f2-113">-Filter</span></span>
<span data-ttu-id="204f2-114">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="204f2-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="204f2-115">-Inline count</span><span class="sxs-lookup"><span data-stu-id="204f2-115">-InlineCount</span></span>
<span data-ttu-id="204f2-116">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="204f2-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="204f2-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="204f2-117">-OrderBy</span></span>
<span data-ttu-id="204f2-118">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="204f2-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="204f2-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="204f2-119">-Skip</span></span>
<span data-ttu-id="204f2-120">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="204f2-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="204f2-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="204f2-121">-SubscriptionId</span></span>
<span data-ttu-id="204f2-122">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="204f2-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="204f2-123">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="204f2-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="204f2-124">-Top</span><span class="sxs-lookup"><span data-stu-id="204f2-124">-Top</span></span>
<span data-ttu-id="204f2-125">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="204f2-125">OData top parameter.</span></span>

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

### <span data-ttu-id="204f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="204f2-126">CommonParameters</span></span>
<span data-ttu-id="204f2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="204f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="204f2-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="204f2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="204f2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="204f2-129">INPUTS</span></span>

## <span data-ttu-id="204f2-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="204f2-130">OUTPUTS</span></span>

### <span data-ttu-id="204f2-131">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="204f2-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="204f2-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="204f2-132">NOTES</span></span>

## <span data-ttu-id="204f2-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="204f2-133">RELATED LINKS</span></span>

