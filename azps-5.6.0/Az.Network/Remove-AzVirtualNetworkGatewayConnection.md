---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3a598001421bf237f93a63fb4f45d069bf9404ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945839"
---
# <span data-ttu-id="ae671-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ae671-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ae671-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae671-102">SYNOPSIS</span></span>
<span data-ttu-id="ae671-103">Löscht eine Verbindung mit einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="ae671-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="ae671-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae671-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae671-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae671-105">DESCRIPTION</span></span>
<span data-ttu-id="ae671-106">Die Virtual Network Gateway Connection ist das Objekt, das den IPsec-Tunnel (Site-to-Site oder Vnet-to-Vnet) darstellt, der mit Ihrem Virtuellen Netzwerkgateway in Azure verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ae671-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="ae671-107">Das **Cmdlet Remove-AzVirtualNetworkGatewayConnection** löscht das Objekt Ihrer Verbindung basierend auf Name und Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ae671-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ae671-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ae671-108">EXAMPLES</span></span>

### <span data-ttu-id="ae671-109">Beispiel 1: Löschen einer Virtuellen Netzwerkgatewayverbindung</span><span class="sxs-lookup"><span data-stu-id="ae671-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="ae671-110">Löscht das Objekt der Virtual Network Gateway Connection mit dem Namen "myTunnel" innerhalb der Ressourcengruppe "myRG"</span><span class="sxs-lookup"><span data-stu-id="ae671-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="ae671-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ae671-111">PARAMETERS</span></span>

### <span data-ttu-id="ae671-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae671-112">-DefaultProfile</span></span>
<span data-ttu-id="ae671-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae671-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae671-114">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ae671-114">-Force</span></span>
<span data-ttu-id="ae671-115">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="ae671-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ae671-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ae671-116">-Name</span></span>
<span data-ttu-id="ae671-117">Gibt den Namen der virtuellen Netzwerkgatewayverbindung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ae671-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ae671-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae671-118">-PassThru</span></span>
<span data-ttu-id="ae671-119">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ae671-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ae671-120">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ae671-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae671-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae671-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae671-122">Gibt den Namen der Ressourcengruppe an, die die Verbindung des virtuellen Netzwerkgateways enthält.</span><span class="sxs-lookup"><span data-stu-id="ae671-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="ae671-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ae671-123">-Confirm</span></span>
<span data-ttu-id="ae671-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ae671-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae671-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae671-125">-WhatIf</span></span>
<span data-ttu-id="ae671-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae671-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae671-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ae671-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae671-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae671-128">CommonParameters</span></span>
<span data-ttu-id="ae671-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae671-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae671-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae671-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae671-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ae671-131">INPUTS</span></span>

### <span data-ttu-id="ae671-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ae671-132">System.String</span></span>

## <span data-ttu-id="ae671-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ae671-133">OUTPUTS</span></span>

### <span data-ttu-id="ae671-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae671-134">System.Boolean</span></span>

## <span data-ttu-id="ae671-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ae671-135">NOTES</span></span>

## <span data-ttu-id="ae671-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ae671-136">RELATED LINKS</span></span>

[<span data-ttu-id="ae671-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ae671-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ae671-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ae671-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ae671-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ae671-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
