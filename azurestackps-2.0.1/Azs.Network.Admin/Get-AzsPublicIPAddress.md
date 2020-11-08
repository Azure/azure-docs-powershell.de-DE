---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005410"
---
# <span data-ttu-id="9e761-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="9e761-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="9e761-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e761-102">SYNOPSIS</span></span>
<span data-ttu-id="9e761-103">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="9e761-103">List of public ip addresses.</span></span>

## <span data-ttu-id="9e761-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e761-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9e761-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e761-105">DESCRIPTION</span></span>
<span data-ttu-id="9e761-106">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="9e761-106">List of public ip addresses.</span></span>

## <span data-ttu-id="9e761-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e761-107">EXAMPLES</span></span>

### <span data-ttu-id="9e761-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9e761-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="9e761-109">Rufen Sie die Liste der öffentlichen IP-Adressen ab, die entweder zugewiesen oder nicht zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="9e761-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="9e761-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e761-110">PARAMETERS</span></span>

### <span data-ttu-id="9e761-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e761-111">-DefaultProfile</span></span>
<span data-ttu-id="9e761-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e761-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e761-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="9e761-113">-Filter</span></span>
<span data-ttu-id="9e761-114">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="9e761-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="9e761-115">-Inline count</span><span class="sxs-lookup"><span data-stu-id="9e761-115">-InlineCount</span></span>
<span data-ttu-id="9e761-116">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="9e761-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="9e761-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="9e761-117">-OrderBy</span></span>
<span data-ttu-id="9e761-118">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="9e761-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="9e761-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="9e761-119">-Skip</span></span>
<span data-ttu-id="9e761-120">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="9e761-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="9e761-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9e761-121">-SubscriptionId</span></span>
<span data-ttu-id="9e761-122">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9e761-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9e761-123">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9e761-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9e761-124">-Top</span><span class="sxs-lookup"><span data-stu-id="9e761-124">-Top</span></span>
<span data-ttu-id="9e761-125">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="9e761-125">OData top parameter.</span></span>

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

### <span data-ttu-id="9e761-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e761-126">CommonParameters</span></span>
<span data-ttu-id="9e761-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e761-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e761-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e761-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e761-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e761-129">INPUTS</span></span>

## <span data-ttu-id="9e761-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e761-130">OUTPUTS</span></span>

### <span data-ttu-id="9e761-131">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="9e761-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="9e761-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e761-132">NOTES</span></span>

## <span data-ttu-id="9e761-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e761-133">RELATED LINKS</span></span>

