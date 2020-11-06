---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: f4ef683b65967fe694713b7990d23eb173f02163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481866"
---
# <span data-ttu-id="2bb91-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2bb91-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="2bb91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bb91-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb91-103">Erstellt eine Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="2bb91-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bb91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bb91-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -Location <String>
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2bb91-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bb91-105">DESCRIPTION</span></span>
<span data-ttu-id="2bb91-106">Das Cmdlet **New-AzureRmRouteTable** erstellt eine Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2bb91-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="2bb91-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bb91-107">EXAMPLES</span></span>

### <span data-ttu-id="2bb91-108">Beispiel 1: Erstellen einer Arbeitsplan Tabelle, die eine Route enthält</span><span class="sxs-lookup"><span data-stu-id="2bb91-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="2bb91-109">Der erste Befehl erstellt eine Route mit dem Namen Route07 mithilfe des New-AzureRmRouteConfig-Cmdlets und speichert Sie dann in der $Route-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2bb91-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="2bb91-110">Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.</span><span class="sxs-lookup"><span data-stu-id="2bb91-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="2bb91-111">Mit dem zweiten Befehl wird eine Routentabelle mit dem Namen RouteTable01 erstellt, und die in $Route gespeicherte Route wird der neuen Tabelle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2bb91-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="2bb91-112">Der Befehl gibt die Ressourcengruppe an, zu der die Tabelle gehört, und den Speicherort für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2bb91-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="2bb91-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bb91-113">PARAMETERS</span></span>

### <span data-ttu-id="2bb91-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2bb91-114">-Force</span></span>
<span data-ttu-id="2bb91-115">Gibt an, dass dieses Cmdlet eine Route-Tabelle erstellt, auch wenn bereits eine Route-Tabelle mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2bb91-115">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb91-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="2bb91-116">-Location</span></span>
<span data-ttu-id="2bb91-117">Gibt den Azure-Bereich an, in dem dieses Cmdlet eine Routentabelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="2bb91-117">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="2bb91-118">Weitere Informationen finden Sie unter [Azure-Bereiche](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="2bb91-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb91-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2bb91-119">-Name</span></span>
<span data-ttu-id="2bb91-120">Gibt einen Namen für die Route-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="2bb91-120">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb91-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bb91-121">-ResourceGroupName</span></span>
<span data-ttu-id="2bb91-122">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet eine Routentabelle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2bb91-122">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb91-123">-Route</span><span class="sxs-lookup"><span data-stu-id="2bb91-123">-Route</span></span>
<span data-ttu-id="2bb91-124">Gibt ein Array von **Route** -Objekten an, die der Route-Tabelle zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2bb91-124">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb91-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2bb91-125">-Tag</span></span>
<span data-ttu-id="2bb91-126">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2bb91-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2bb91-127">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2bb91-127">For example:</span></span>

<span data-ttu-id="2bb91-128">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2bb91-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb91-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2bb91-129">-Confirm</span></span>
<span data-ttu-id="2bb91-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2bb91-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb91-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bb91-131">-WhatIf</span></span>
<span data-ttu-id="2bb91-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bb91-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bb91-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2bb91-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb91-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb91-134">-DefaultProfile</span></span>
<span data-ttu-id="2bb91-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bb91-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb91-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb91-136">CommonParameters</span></span>
<span data-ttu-id="2bb91-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb91-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb91-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb91-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb91-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bb91-139">INPUTS</span></span>

## <span data-ttu-id="2bb91-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bb91-140">OUTPUTS</span></span>

### <span data-ttu-id="2bb91-141">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2bb91-141">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2bb91-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bb91-142">NOTES</span></span>

## <span data-ttu-id="2bb91-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bb91-143">RELATED LINKS</span></span>

[<span data-ttu-id="2bb91-144">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2bb91-144">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="2bb91-145">Neu – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2bb91-145">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="2bb91-146">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2bb91-146">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="2bb91-147">Satz-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2bb91-147">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
