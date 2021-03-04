---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936440"
---
# <span data-ttu-id="6bfa6-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6bfa6-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="6bfa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bfa6-102">SYNOPSIS</span></span>
<span data-ttu-id="6bfa6-103">Aktualisiert einen Traffic Manager-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="6bfa6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6bfa6-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bfa6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6bfa6-105">DESCRIPTION</span></span>
<span data-ttu-id="6bfa6-106">Das **Cmdlet Set-AzTrafficManagerEndpoint** aktualisiert einen Endpunkt in Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="6bfa6-107">Dieses Cmdlet aktualisiert die Einstellungen eines lokalen Endpunktobjekts.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="6bfa6-108">Sie können das Endpunktobjekt entweder mithilfe des *TrafficManagerEndpoint-Parameters* oder mithilfe der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="6bfa6-109">Sie können ein lokales Objekt abrufen, das einen Endpunkt darstellt, indem Sie das cmdlet Get-AzTrafficManagerEndpoint verwenden.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="6bfa6-110">Ändern Sie das Objekt lokal, und verwenden Sie **dann Set-AzTrafficManagerEndpoint,** um Ihre Änderungen zu commiten.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="6bfa6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6bfa6-111">EXAMPLES</span></span>

### <span data-ttu-id="6bfa6-112">Beispiel 1: Aktualisieren eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="6bfa6-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="6bfa6-113">Der erste Befehl ruft einen Azure Traffic Manager-Endpunkt mithilfe des **Get-AzTrafficManagerEndpoint-Cmdlets** ab.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="6bfa6-114">Der Befehl speichert den Endpunkt lokal in der $TrafficManagerEndpoint-Variable.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="6bfa6-115">Der zweite Befehl ändert diesen Endpunkt lokal.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="6bfa6-116">Mit diesem Befehl wird die Endpunktgewichtung auf 20 geändert.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="6bfa6-117">Der dritte Befehl aktualisiert den Endpunkt in Traffic Manager so, dass er dem lokalen Wert in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="6bfa6-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6bfa6-118">PARAMETERS</span></span>

### <span data-ttu-id="6bfa6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bfa6-119">-DefaultProfile</span></span>
<span data-ttu-id="6bfa6-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bfa6-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6bfa6-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="6bfa6-122">Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="6bfa6-123">Dieses Cmdlet aktualisiert Traffic Manager so, dass es mit diesem lokalen Objekt übereinstimmen kann.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bfa6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bfa6-124">CommonParameters</span></span>
<span data-ttu-id="6bfa6-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bfa6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bfa6-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bfa6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bfa6-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6bfa6-127">INPUTS</span></span>

### <span data-ttu-id="6bfa6-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6bfa6-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6bfa6-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6bfa6-129">OUTPUTS</span></span>

### <span data-ttu-id="6bfa6-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6bfa6-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6bfa6-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6bfa6-131">NOTES</span></span>

## <span data-ttu-id="6bfa6-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6bfa6-132">RELATED LINKS</span></span>
