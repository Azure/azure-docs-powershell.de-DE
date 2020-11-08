---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179905"
---
# <span data-ttu-id="1d168-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d168-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="1d168-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1d168-102">SYNOPSIS</span></span>
<span data-ttu-id="1d168-103">Ruft Routen aus einer Routentabelle ab.</span><span class="sxs-lookup"><span data-stu-id="1d168-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="1d168-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d168-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d168-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d168-105">DESCRIPTION</span></span>
<span data-ttu-id="1d168-106">Das Cmdlet " **Get-AzRouteConfig** " ruft Routen aus einer Azure Route-Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="1d168-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="1d168-107">Sie können eine Route nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="1d168-107">You can specify a route by name.</span></span>

## <span data-ttu-id="1d168-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1d168-108">EXAMPLES</span></span>

### <span data-ttu-id="1d168-109">Beispiel 1: Abrufen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="1d168-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="1d168-110">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mit dem Cmdlet **Get-AzRouteTable** ab.</span><span class="sxs-lookup"><span data-stu-id="1d168-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="1d168-111">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d168-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1d168-112">Das aktuelle Cmdlet ruft die Route mit dem Namen Route07 in der Routingtabelle mit dem Namen RouteTable01 ab.</span><span class="sxs-lookup"><span data-stu-id="1d168-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="1d168-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d168-113">PARAMETERS</span></span>

### <span data-ttu-id="1d168-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d168-114">-DefaultProfile</span></span>
<span data-ttu-id="1d168-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d168-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d168-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1d168-116">-Name</span></span>
<span data-ttu-id="1d168-117">Gibt den Namen der Route an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1d168-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1d168-118">-Routel</span><span class="sxs-lookup"><span data-stu-id="1d168-118">-RouteTable</span></span>
<span data-ttu-id="1d168-119">Gibt die Route-Tabelle an, aus der dieses Cmdlet Routen abruft.</span><span class="sxs-lookup"><span data-stu-id="1d168-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d168-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d168-120">CommonParameters</span></span>
<span data-ttu-id="1d168-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d168-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d168-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d168-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d168-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1d168-123">INPUTS</span></span>

### <span data-ttu-id="1d168-124">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d168-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1d168-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1d168-125">OUTPUTS</span></span>

### <span data-ttu-id="1d168-126">Microsoft. Azure. Commands. Network. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="1d168-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="1d168-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="1d168-127">NOTES</span></span>

## <span data-ttu-id="1d168-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1d168-128">RELATED LINKS</span></span>

[<span data-ttu-id="1d168-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d168-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="1d168-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="1d168-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="1d168-131">Neu – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d168-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="1d168-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d168-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="1d168-133">Satz-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="1d168-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


