---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 99f621824d10b574c7f64fb7653bc4154ba6766e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662712"
---
# <span data-ttu-id="50e4f-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="50e4f-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="50e4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="50e4f-103">Aktualisiert einen Traffic Manager-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="50e4f-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50e4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50e4f-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50e4f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="50e4f-106">Das Cmdlet " **Satz-AzureRmTrafficManagerEndpoint** " aktualisiert einen Endpunkt in Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="50e4f-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="50e4f-107">Dieses Cmdlet aktualisiert die Einstellungen von einem lokalen Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="50e4f-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="50e4f-108">Sie können das Endpunkt Objekt entweder mithilfe des *TrafficManagerEndpoint* -Parameters oder mithilfe der Pipeline angeben.</span><span class="sxs-lookup"><span data-stu-id="50e4f-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="50e4f-109">Mithilfe des Get-AzureRmTrafficManagerEndpoint-Cmdlets können Sie ein lokales Objekt abrufen, das einen Endpunkt darstellt.</span><span class="sxs-lookup"><span data-stu-id="50e4f-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="50e4f-110">Ändern Sie das Objekt lokal, und verwenden Sie dann die **Einstellung AzureRmTrafficManagerEndpoint** , um die Änderungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="50e4f-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="50e4f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50e4f-111">EXAMPLES</span></span>

### <span data-ttu-id="50e4f-112">Beispiel 1: Aktualisieren eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="50e4f-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="50e4f-113">Der erste Befehl ruft einen Azure Traffic Manager-Endpunkt mit dem Cmdlet **Get-AzureRmTrafficManagerEndpoint** ab.</span><span class="sxs-lookup"><span data-stu-id="50e4f-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="50e4f-114">Der Befehl speichert den Endpunkt lokal in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="50e4f-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="50e4f-115">Der zweite Befehl ändert diesen Endpunkt lokal.</span><span class="sxs-lookup"><span data-stu-id="50e4f-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="50e4f-116">Mit diesem Befehl wird die Endpunkt Gewichtung auf 20 geändert.</span><span class="sxs-lookup"><span data-stu-id="50e4f-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="50e4f-117">Der dritte Befehl aktualisiert den Endpunkt im Traffic Manager so, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.</span><span class="sxs-lookup"><span data-stu-id="50e4f-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="50e4f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="50e4f-118">PARAMETERS</span></span>

### <span data-ttu-id="50e4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e4f-119">-DefaultProfile</span></span>
<span data-ttu-id="50e4f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50e4f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e4f-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="50e4f-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="50e4f-122">Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="50e4f-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="50e4f-123">Dieses Cmdlet aktualisiert den Datenverkehrs-Manager, um diesem lokalen Objekt zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="50e4f-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50e4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e4f-124">CommonParameters</span></span>
<span data-ttu-id="50e4f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e4f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e4f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e4f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50e4f-127">INPUTS</span></span>

### <span data-ttu-id="50e4f-128">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="50e4f-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="50e4f-129">Dieses Cmdlet akzeptiert ein **TrafficManagerEndpoint** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="50e4f-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="50e4f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50e4f-130">OUTPUTS</span></span>

### <span data-ttu-id="50e4f-131">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="50e4f-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="50e4f-132">Dieses Cmdlet gibt ein **TrafficManagerEndpoint** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="50e4f-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="50e4f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="50e4f-133">NOTES</span></span>

## <span data-ttu-id="50e4f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50e4f-134">RELATED LINKS</span></span>

