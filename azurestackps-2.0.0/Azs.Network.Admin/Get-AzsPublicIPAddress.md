---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842527"
---
# <span data-ttu-id="99c86-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="99c86-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="99c86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99c86-102">SYNOPSIS</span></span>
<span data-ttu-id="99c86-103">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="99c86-103">List of public ip addresses.</span></span>

## <span data-ttu-id="99c86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99c86-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="99c86-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99c86-105">DESCRIPTION</span></span>
<span data-ttu-id="99c86-106">Liste der öffentlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="99c86-106">List of public ip addresses.</span></span>

## <span data-ttu-id="99c86-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99c86-107">EXAMPLES</span></span>

### <span data-ttu-id="99c86-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="99c86-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="99c86-109">Rufen Sie die Liste der öffentlichen IP-Adressen ab, die entweder zugewiesen oder nicht zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="99c86-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="99c86-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="99c86-110">PARAMETERS</span></span>

### <span data-ttu-id="99c86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c86-111">-DefaultProfile</span></span>
<span data-ttu-id="99c86-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99c86-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99c86-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="99c86-113">-Filter</span></span>
<span data-ttu-id="99c86-114">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="99c86-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="99c86-115">-Inline count</span><span class="sxs-lookup"><span data-stu-id="99c86-115">-InlineCount</span></span>
<span data-ttu-id="99c86-116">OData Inline count-Parameter</span><span class="sxs-lookup"><span data-stu-id="99c86-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="99c86-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="99c86-117">-OrderBy</span></span>
<span data-ttu-id="99c86-118">OData-orderBy-Parameter</span><span class="sxs-lookup"><span data-stu-id="99c86-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="99c86-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="99c86-119">-Skip</span></span>
<span data-ttu-id="99c86-120">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="99c86-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="99c86-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="99c86-121">-SubscriptionId</span></span>
<span data-ttu-id="99c86-122">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="99c86-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="99c86-123">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="99c86-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="99c86-124">-Top</span><span class="sxs-lookup"><span data-stu-id="99c86-124">-Top</span></span>
<span data-ttu-id="99c86-125">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="99c86-125">OData top parameter.</span></span>

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

### <span data-ttu-id="99c86-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c86-126">CommonParameters</span></span>
<span data-ttu-id="99c86-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c86-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c86-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99c86-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c86-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99c86-129">INPUTS</span></span>

## <span data-ttu-id="99c86-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99c86-130">OUTPUTS</span></span>

### <span data-ttu-id="99c86-131">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="99c86-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="99c86-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="99c86-132">NOTES</span></span>

## <span data-ttu-id="99c86-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99c86-133">RELATED LINKS</span></span>

