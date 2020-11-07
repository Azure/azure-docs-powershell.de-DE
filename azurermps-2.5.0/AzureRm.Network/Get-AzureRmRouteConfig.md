---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: 907ca017518304a38340e9539aa4e8faf4216d59
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850688"
---
# <span data-ttu-id="8e375-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8e375-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="8e375-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e375-102">SYNOPSIS</span></span>
<span data-ttu-id="8e375-103">Ruft Routen aus einer Routentabelle ab.</span><span class="sxs-lookup"><span data-stu-id="8e375-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e375-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e375-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e375-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e375-105">DESCRIPTION</span></span>
<span data-ttu-id="8e375-106">Das Cmdlet " **Get-AzureRmRouteConfig** " ruft Routen aus einer Azure Route-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="8e375-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="8e375-107">Sie können eine Route nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="8e375-107">You can specify a route by name.</span></span>

## <span data-ttu-id="8e375-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e375-108">EXAMPLES</span></span>

### <span data-ttu-id="8e375-109">Beispiel 1: Abrufen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="8e375-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="8e375-110">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mit dem Cmdlet **Get-AzureRmRouteTable** ab.</span><span class="sxs-lookup"><span data-stu-id="8e375-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="8e375-111">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e375-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8e375-112">Das aktuelle Cmdlet ruft die Route mit dem Namen Route07 in der Routingtabelle mit dem Namen RouteTable01 ab.</span><span class="sxs-lookup"><span data-stu-id="8e375-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="8e375-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e375-113">PARAMETERS</span></span>

### <span data-ttu-id="8e375-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e375-114">-DefaultProfile</span></span>
<span data-ttu-id="8e375-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e375-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e375-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8e375-116">-Name</span></span>
<span data-ttu-id="8e375-117">Gibt den Namen der Route an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="8e375-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e375-118">-Routel</span><span class="sxs-lookup"><span data-stu-id="8e375-118">-RouteTable</span></span>
<span data-ttu-id="8e375-119">Gibt die Route-Tabelle an, aus der dieses Cmdlet Routen abruft.</span><span class="sxs-lookup"><span data-stu-id="8e375-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e375-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e375-120">CommonParameters</span></span>
<span data-ttu-id="8e375-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e375-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e375-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e375-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e375-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e375-123">INPUTS</span></span>

### <span data-ttu-id="8e375-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e375-124">PSRouteTable</span></span>
<span data-ttu-id="8e375-125">Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e375-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="8e375-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e375-126">OUTPUTS</span></span>

### <span data-ttu-id="8e375-127">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="8e375-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="8e375-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e375-128">NOTES</span></span>

## <span data-ttu-id="8e375-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e375-129">RELATED LINKS</span></span>

[<span data-ttu-id="8e375-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8e375-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="8e375-131">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e375-131">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="8e375-132">Neu – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8e375-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="8e375-133">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8e375-133">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="8e375-134">Satz-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8e375-134">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


