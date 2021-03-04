---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: c4841678a1e1f318da36b506cc56e586244c233f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945850"
---
# <span data-ttu-id="8857c-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8857c-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="8857c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8857c-102">SYNOPSIS</span></span>
<span data-ttu-id="8857c-103">Löscht ein Virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="8857c-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="8857c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8857c-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8857c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8857c-105">DESCRIPTION</span></span>
<span data-ttu-id="8857c-106">Das Virtual Network Gateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="8857c-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="8857c-107">Das **Get-AzVirtualNetworkGateway-Cmdlet** gibt das Objekt Ihres Gateways in Azure basierend auf Name und Ressourcengruppenname zurück.</span><span class="sxs-lookup"><span data-stu-id="8857c-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="8857c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8857c-108">EXAMPLES</span></span>

### <span data-ttu-id="8857c-109">Beispiel 1: Löschen eines Virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="8857c-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="8857c-110">Löscht das Objekt des Virtuellen Netzwerkgateways mit dem Namen "myGateway" innerhalb der Ressourcengruppe "myRG". Hinweis: Sie müssen zuerst alle Verbindungen mit dem Virtual Network Gateway mithilfe des **Cmdlets Remove-AzVirtualNetworkGatewayConnection** löschen.</span><span class="sxs-lookup"><span data-stu-id="8857c-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="8857c-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8857c-111">PARAMETERS</span></span>

### <span data-ttu-id="8857c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8857c-112">-AsJob</span></span>
<span data-ttu-id="8857c-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8857c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8857c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8857c-114">-DefaultProfile</span></span>
<span data-ttu-id="8857c-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8857c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8857c-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="8857c-116">-Force</span></span>
<span data-ttu-id="8857c-117">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="8857c-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8857c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8857c-118">-Name</span></span>
<span data-ttu-id="8857c-119">Gibt den Namen des virtuellen Netzwerkgateways an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8857c-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8857c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8857c-120">-PassThru</span></span>
<span data-ttu-id="8857c-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8857c-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8857c-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8857c-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8857c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8857c-123">-ResourceGroupName</span></span>
<span data-ttu-id="8857c-124">Gibt den Namen der Ressourcengruppe an, die das Gateway für virtuelle Netzwerke enthält.</span><span class="sxs-lookup"><span data-stu-id="8857c-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="8857c-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8857c-125">-Confirm</span></span>
<span data-ttu-id="8857c-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8857c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8857c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8857c-127">-WhatIf</span></span>
<span data-ttu-id="8857c-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8857c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8857c-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8857c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8857c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8857c-130">CommonParameters</span></span>
<span data-ttu-id="8857c-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8857c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8857c-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8857c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8857c-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8857c-133">INPUTS</span></span>

### <span data-ttu-id="8857c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8857c-134">System.String</span></span>

## <span data-ttu-id="8857c-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8857c-135">OUTPUTS</span></span>

### <span data-ttu-id="8857c-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8857c-136">System.Boolean</span></span>

## <span data-ttu-id="8857c-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8857c-137">NOTES</span></span>

## <span data-ttu-id="8857c-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8857c-138">RELATED LINKS</span></span>

[<span data-ttu-id="8857c-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8857c-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8857c-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8857c-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8857c-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8857c-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8857c-142">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8857c-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8857c-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8857c-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
