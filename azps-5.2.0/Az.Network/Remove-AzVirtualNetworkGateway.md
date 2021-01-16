---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305432"
---
# <span data-ttu-id="4aba3-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4aba3-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="4aba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aba3-102">SYNOPSIS</span></span>
<span data-ttu-id="4aba3-103">Löscht ein virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="4aba3-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="4aba3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aba3-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aba3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aba3-105">DESCRIPTION</span></span>
<span data-ttu-id="4aba3-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="4aba3-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="4aba3-107">Das **Cmdlet "Get-AzVirtualNetworkGateway"** gibt das Objekt Ihres Gateways in Azure basierend auf "Name" und "Ressourcengruppenname" zurück.</span><span class="sxs-lookup"><span data-stu-id="4aba3-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="4aba3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4aba3-108">EXAMPLES</span></span>

### <span data-ttu-id="4aba3-109">Beispiel 1: Löschen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="4aba3-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="4aba3-110">Löscht das Objekt des virtuellen Netzwerkgateways mit dem Namen "myGateway" in der Ressourcengruppe "myRG". Hinweis: Sie müssen zuerst alle Verbindungen mit dem virtuellen Netzwerkgateway mithilfe des **Cmdlets "Remove-AzVirtualNetworkGatewayConnection"** löschen.</span><span class="sxs-lookup"><span data-stu-id="4aba3-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="4aba3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aba3-111">PARAMETERS</span></span>

### <span data-ttu-id="4aba3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4aba3-112">-AsJob</span></span>
<span data-ttu-id="4aba3-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4aba3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4aba3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aba3-114">-DefaultProfile</span></span>
<span data-ttu-id="4aba3-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4aba3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aba3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4aba3-116">-Force</span></span>
<span data-ttu-id="4aba3-117">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="4aba3-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4aba3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4aba3-118">-Name</span></span>
<span data-ttu-id="4aba3-119">Gibt den Namen des virtuellen Netzwerkgateways an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4aba3-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4aba3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4aba3-120">-PassThru</span></span>
<span data-ttu-id="4aba3-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4aba3-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4aba3-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="4aba3-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4aba3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aba3-123">-ResourceGroupName</span></span>
<span data-ttu-id="4aba3-124">Gibt den Namen der Ressourcengruppe an, die das virtuelle Netzwerkgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="4aba3-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="4aba3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aba3-125">-Confirm</span></span>
<span data-ttu-id="4aba3-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aba3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aba3-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4aba3-127">-WhatIf</span></span>
<span data-ttu-id="4aba3-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4aba3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aba3-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4aba3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aba3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aba3-130">CommonParameters</span></span>
<span data-ttu-id="4aba3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aba3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aba3-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aba3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aba3-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4aba3-133">INPUTS</span></span>

### <span data-ttu-id="4aba3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4aba3-134">System.String</span></span>

## <span data-ttu-id="4aba3-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4aba3-135">OUTPUTS</span></span>

### <span data-ttu-id="4aba3-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4aba3-136">System.Boolean</span></span>

## <span data-ttu-id="4aba3-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4aba3-137">NOTES</span></span>

## <span data-ttu-id="4aba3-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4aba3-138">RELATED LINKS</span></span>

[<span data-ttu-id="4aba3-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4aba3-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4aba3-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4aba3-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4aba3-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4aba3-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4aba3-142">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4aba3-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="4aba3-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4aba3-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
