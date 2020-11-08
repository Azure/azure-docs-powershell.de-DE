---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180142"
---
# <span data-ttu-id="98bb3-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="98bb3-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="98bb3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="98bb3-103">Aktualisiert einen Traffic Manager-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="98bb3-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="98bb3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98bb3-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98bb3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98bb3-105">DESCRIPTION</span></span>
<span data-ttu-id="98bb3-106">Das Cmdlet " **Satz-AzTrafficManagerEndpoint** " aktualisiert einen Endpunkt in Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="98bb3-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="98bb3-107">Dieses Cmdlet aktualisiert die Einstellungen von einem lokalen Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="98bb3-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="98bb3-108">Sie können das Endpunkt Objekt entweder mithilfe des *TrafficManagerEndpoint* -Parameters oder mithilfe der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="98bb3-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="98bb3-109">Mithilfe des Get-AzTrafficManagerEndpoint-Cmdlets können Sie ein lokales Objekt abrufen, das einen Endpunkt darstellt.</span><span class="sxs-lookup"><span data-stu-id="98bb3-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="98bb3-110">Ändern Sie das Objekt lokal, und verwenden Sie dann die **Einstellung AzTrafficManagerEndpoint** , um die Änderungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="98bb3-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="98bb3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98bb3-111">EXAMPLES</span></span>

### <span data-ttu-id="98bb3-112">Beispiel 1: Aktualisieren eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="98bb3-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="98bb3-113">Der erste Befehl ruft einen Azure Traffic Manager-Endpunkt mit dem Cmdlet **Get-AzTrafficManagerEndpoint** ab.</span><span class="sxs-lookup"><span data-stu-id="98bb3-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="98bb3-114">Der Befehl speichert den Endpunkt lokal in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="98bb3-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="98bb3-115">Der zweite Befehl ändert diesen Endpunkt lokal.</span><span class="sxs-lookup"><span data-stu-id="98bb3-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="98bb3-116">Mit diesem Befehl wird die Endpunkt Gewichtung auf 20 geändert.</span><span class="sxs-lookup"><span data-stu-id="98bb3-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="98bb3-117">Der dritte Befehl aktualisiert den Endpunkt im Traffic Manager so, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.</span><span class="sxs-lookup"><span data-stu-id="98bb3-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="98bb3-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="98bb3-118">PARAMETERS</span></span>

### <span data-ttu-id="98bb3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98bb3-119">-DefaultProfile</span></span>
<span data-ttu-id="98bb3-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="98bb3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98bb3-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="98bb3-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="98bb3-122">Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="98bb3-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="98bb3-123">Dieses Cmdlet aktualisiert den Datenverkehrs-Manager, um diesem lokalen Objekt zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="98bb3-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="98bb3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98bb3-124">CommonParameters</span></span>
<span data-ttu-id="98bb3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98bb3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98bb3-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98bb3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98bb3-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98bb3-127">INPUTS</span></span>

### <span data-ttu-id="98bb3-128">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="98bb3-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="98bb3-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98bb3-129">OUTPUTS</span></span>

### <span data-ttu-id="98bb3-130">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="98bb3-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="98bb3-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="98bb3-131">NOTES</span></span>

## <span data-ttu-id="98bb3-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98bb3-132">RELATED LINKS</span></span>
