---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: fd50f9d9c49b91139753d9ac0fc503a71955962a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848715"
---
# <span data-ttu-id="ac799-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ac799-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ac799-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac799-102">SYNOPSIS</span></span>
<span data-ttu-id="ac799-103">Löschen einer virtuellen Netzwerk Gateway-Verbindung</span><span class="sxs-lookup"><span data-stu-id="ac799-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac799-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac799-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac799-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac799-105">DESCRIPTION</span></span>
<span data-ttu-id="ac799-106">Die VPN-Gatewayverbindung ist das Objekt, das den IPSec-Tunnel (Site-to-Site oder vnet-to-vnet) darstellt, der mit dem virtuellen Netzwerkgateway in Azure verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ac799-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="ac799-107">Das Cmdlet **Remove-AzureRmVirtualNetworkGatewayConnection** löscht das Objekt Ihrer Verbindung basierend auf Name und Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ac799-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ac799-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac799-108">EXAMPLES</span></span>

### <span data-ttu-id="ac799-109">1: Löschen einer virtuellen Netzwerk Gateway-Verbindung</span><span class="sxs-lookup"><span data-stu-id="ac799-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="ac799-110">Löscht das Objekt der virtuellen Netzwerk Gateway-Verbindung mit dem Namen "mytunnel" innerhalb der Ressourcengruppe "myRG"</span><span class="sxs-lookup"><span data-stu-id="ac799-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="ac799-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac799-111">PARAMETERS</span></span>

### <span data-ttu-id="ac799-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac799-112">-DefaultProfile</span></span>
<span data-ttu-id="ac799-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac799-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac799-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ac799-114">-Force</span></span>
<span data-ttu-id="ac799-115">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ac799-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac799-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ac799-116">-Name</span></span>
<span data-ttu-id="ac799-117">Gibt den Namen der virtuellen Netzwerkgateway-Verbindung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ac799-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac799-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac799-118">-PassThru</span></span>
<span data-ttu-id="ac799-119">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ac799-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac799-120">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ac799-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac799-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac799-121">-ResourceGroupName</span></span>
<span data-ttu-id="ac799-122">Gibt den Namen der Ressourcengruppe an, die die virtuelle Netzwerkgateway-Verbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="ac799-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac799-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac799-123">-Confirm</span></span>
<span data-ttu-id="ac799-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac799-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac799-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac799-125">-WhatIf</span></span>
<span data-ttu-id="ac799-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac799-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac799-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac799-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac799-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac799-128">CommonParameters</span></span>
<span data-ttu-id="ac799-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac799-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac799-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac799-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac799-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac799-131">INPUTS</span></span>

## <span data-ttu-id="ac799-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac799-132">OUTPUTS</span></span>

## <span data-ttu-id="ac799-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac799-133">NOTES</span></span>

## <span data-ttu-id="ac799-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac799-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac799-135">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ac799-135">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ac799-136">Neu – AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ac799-136">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ac799-137">Satz-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ac799-137">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)


