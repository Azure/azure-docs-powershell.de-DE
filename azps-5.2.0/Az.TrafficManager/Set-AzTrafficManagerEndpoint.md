---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302072"
---
# <span data-ttu-id="f1e98-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1e98-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="f1e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e98-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e98-103">Aktualisiert einen Verkehrs-Manager-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="f1e98-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="f1e98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1e98-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1e98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1e98-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e98-106">Das **Cmdlet "Set-AzTrafficManagerEndpoint"** aktualisiert einen Endpunkt in Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f1e98-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="f1e98-107">Dieses Cmdlet aktualisiert die Einstellungen eines lokalen Endpunktobjekts.</span><span class="sxs-lookup"><span data-stu-id="f1e98-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="f1e98-108">Sie können das Endpunktobjekt entweder mithilfe des *Parameters "TrafficManagerEndpoint"* oder mithilfe der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="f1e98-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="f1e98-109">Sie können ein lokales Objekt, das einen Endpunkt darstellt, mithilfe des Get-AzTrafficManagerEndpoint abrufen.</span><span class="sxs-lookup"><span data-stu-id="f1e98-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="f1e98-110">Ändern Sie das Objekt lokal, und verwenden Sie **dann "Set-AzTrafficManagerEndpoint",** um ihre Änderungen zu commiten.</span><span class="sxs-lookup"><span data-stu-id="f1e98-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="f1e98-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1e98-111">EXAMPLES</span></span>

### <span data-ttu-id="f1e98-112">Beispiel 1: Aktualisieren eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="f1e98-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="f1e98-113">Der erste Befehl ruft mit dem **Cmdlet "Get-AzTrafficManagerEndpoint"** einen Azure Traffic Manager-Endpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="f1e98-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="f1e98-114">Der Befehl speichert den Endpunkt lokal in der $TrafficManagerEndpoint Variable.</span><span class="sxs-lookup"><span data-stu-id="f1e98-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="f1e98-115">Der zweite Befehl ändert diesen Endpunkt lokal.</span><span class="sxs-lookup"><span data-stu-id="f1e98-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="f1e98-116">Mit diesem Befehl wird die Endpunktgewichtung in "20" geändert.</span><span class="sxs-lookup"><span data-stu-id="f1e98-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="f1e98-117">Mit dem dritten Befehl wird der Endpunkt im Verkehrs-Manager so aktualisiert, dass er dem lokalen Wert in der $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f1e98-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="f1e98-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1e98-118">PARAMETERS</span></span>

### <span data-ttu-id="f1e98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e98-119">-DefaultProfile</span></span>
<span data-ttu-id="f1e98-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1e98-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1e98-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1e98-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="f1e98-122">Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f1e98-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="f1e98-123">Mit diesem Cmdlet wird der Datenverkehrs-Manager so aktualisiert, dass er diesem lokalen Objekt entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="f1e98-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="f1e98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e98-124">CommonParameters</span></span>
<span data-ttu-id="f1e98-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e98-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e98-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e98-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1e98-127">INPUTS</span></span>

### <span data-ttu-id="f1e98-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1e98-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="f1e98-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1e98-129">OUTPUTS</span></span>

### <span data-ttu-id="f1e98-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1e98-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="f1e98-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1e98-131">NOTES</span></span>

## <span data-ttu-id="f1e98-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1e98-132">RELATED LINKS</span></span>
