---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f5ea9c291d23c6378170946ee6b605ec02742ed8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305419"
---
# <span data-ttu-id="03a98-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="03a98-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="03a98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a98-102">SYNOPSIS</span></span>
<span data-ttu-id="03a98-103">Löscht eine Virtuelle Netzwerkgatewayverbindung</span><span class="sxs-lookup"><span data-stu-id="03a98-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="03a98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03a98-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03a98-105">DESCRIPTION</span></span>
<span data-ttu-id="03a98-106">Die Virtuelle Netzwerkgatewayverbindung ist das Objekt, das den mit dem virtuellen Netzwerkgateway in Azure verbundenen IPsec-Tunnel (Site-to-Site oder Vnet-to-Vnet) darstellt.</span><span class="sxs-lookup"><span data-stu-id="03a98-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="03a98-107">Das **Cmdlet "Remove-AzVirtualNetworkGatewayConnection"** löscht das Objekt Ihrer Verbindung basierend auf "Name" und "Ressourcengruppenname".</span><span class="sxs-lookup"><span data-stu-id="03a98-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="03a98-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03a98-108">EXAMPLES</span></span>

### <span data-ttu-id="03a98-109">Beispiel 1: Löschen einer virtuellen Netzwerkgatewayverbindung</span><span class="sxs-lookup"><span data-stu-id="03a98-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="03a98-110">Löscht das Objekt der Virtuellen Netzwerkgatewayverbindung mit dem Namen "myKlasse" in der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="03a98-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="03a98-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03a98-111">PARAMETERS</span></span>

### <span data-ttu-id="03a98-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a98-112">-DefaultProfile</span></span>
<span data-ttu-id="03a98-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03a98-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03a98-114">-Force</span><span class="sxs-lookup"><span data-stu-id="03a98-114">-Force</span></span>
<span data-ttu-id="03a98-115">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="03a98-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03a98-116">-Name</span><span class="sxs-lookup"><span data-stu-id="03a98-116">-Name</span></span>
<span data-ttu-id="03a98-117">Gibt den Namen der virtuellen Netzwerkgatewayverbindung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="03a98-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="03a98-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03a98-118">-PassThru</span></span>
<span data-ttu-id="03a98-119">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="03a98-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03a98-120">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="03a98-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03a98-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a98-121">-ResourceGroupName</span></span>
<span data-ttu-id="03a98-122">Gibt den Namen der Ressourcengruppe an, die die virtuelle Netzwerkgatewayverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="03a98-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="03a98-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03a98-123">-Confirm</span></span>
<span data-ttu-id="03a98-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03a98-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03a98-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="03a98-125">-WhatIf</span></span>
<span data-ttu-id="03a98-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03a98-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a98-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03a98-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03a98-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a98-128">CommonParameters</span></span>
<span data-ttu-id="03a98-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03a98-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a98-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a98-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a98-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03a98-131">INPUTS</span></span>

### <span data-ttu-id="03a98-132">System.String</span><span class="sxs-lookup"><span data-stu-id="03a98-132">System.String</span></span>

## <span data-ttu-id="03a98-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03a98-133">OUTPUTS</span></span>

### <span data-ttu-id="03a98-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03a98-134">System.Boolean</span></span>

## <span data-ttu-id="03a98-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="03a98-135">NOTES</span></span>

## <span data-ttu-id="03a98-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="03a98-136">RELATED LINKS</span></span>

[<span data-ttu-id="03a98-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="03a98-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="03a98-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="03a98-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="03a98-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="03a98-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
