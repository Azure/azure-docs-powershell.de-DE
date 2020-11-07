---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: c5117fc961a93395991055eff2d404b5b8c6c051
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850620"
---
# <span data-ttu-id="b1df4-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b1df4-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="b1df4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1df4-102">SYNOPSIS</span></span>
<span data-ttu-id="b1df4-103">Entfernt eine Route aus einer Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b1df4-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1df4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1df4-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1df4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1df4-105">DESCRIPTION</span></span>
<span data-ttu-id="b1df4-106">Das Cmdlet **Remove-AzureRmRouteConfig** entfernt eine Route aus einer Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b1df4-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="b1df4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1df4-107">EXAMPLES</span></span>

### <span data-ttu-id="b1df4-108">Beispiel 1: Entfernen einer Route</span><span class="sxs-lookup"><span data-stu-id="b1df4-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="b1df4-109">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mit dem Cmdlet **Get-AzureRmRouteTable** ab.</span><span class="sxs-lookup"><span data-stu-id="b1df4-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="b1df4-110">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1df4-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b1df4-111">Das aktuelle Cmdlet entfernt die Route mit dem Namen "Route02" und übergibt das Ergebnis an das Cmdlet " **setAzureRmRouteTable** ", das die Tabelle so aktualisiert, dass die Änderungen wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b1df4-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="b1df4-112">Die Tabelle enthält nicht mehr die Route mit dem Namen Route02.</span><span class="sxs-lookup"><span data-stu-id="b1df4-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="b1df4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1df4-113">PARAMETERS</span></span>

### <span data-ttu-id="b1df4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1df4-114">-DefaultProfile</span></span>
<span data-ttu-id="b1df4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1df4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1df4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b1df4-116">-Name</span></span>
<span data-ttu-id="b1df4-117">Gibt den Namen der Route an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="b1df4-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1df4-118">-Routel</span><span class="sxs-lookup"><span data-stu-id="b1df4-118">-RouteTable</span></span>
<span data-ttu-id="b1df4-119">Gibt die Route-Tabelle an, die die Route enthält, die dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="b1df4-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b1df4-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1df4-120">-Confirm</span></span>
<span data-ttu-id="b1df4-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1df4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1df4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1df4-122">-WhatIf</span></span>
<span data-ttu-id="b1df4-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1df4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1df4-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1df4-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1df4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1df4-125">CommonParameters</span></span>
<span data-ttu-id="b1df4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1df4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1df4-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1df4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1df4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1df4-128">INPUTS</span></span>

### <span data-ttu-id="b1df4-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b1df4-129">PSRouteTable</span></span>
<span data-ttu-id="b1df4-130">Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1df4-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="b1df4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1df4-131">OUTPUTS</span></span>

### <span data-ttu-id="b1df4-132">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b1df4-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="b1df4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1df4-133">NOTES</span></span>

## <span data-ttu-id="b1df4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1df4-134">RELATED LINKS</span></span>

[<span data-ttu-id="b1df4-135">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b1df4-135">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="b1df4-136">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b1df4-136">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="b1df4-137">Neu – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b1df4-137">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="b1df4-138">Satz-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b1df4-138">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


