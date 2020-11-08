---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009070"
---
# <span data-ttu-id="08329-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="08329-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="08329-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08329-102">SYNOPSIS</span></span>
<span data-ttu-id="08329-103">Löschen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="08329-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="08329-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08329-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08329-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08329-105">DESCRIPTION</span></span>
<span data-ttu-id="08329-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="08329-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="08329-107">Das Cmdlet " **Get-AzVirtualNetworkGateway** " gibt das Objekt Ihres Gateways in Azure basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="08329-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="08329-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08329-108">EXAMPLES</span></span>

### <span data-ttu-id="08329-109">Beispiel 1: Löschen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="08329-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="08329-110">Löscht das Objekt des virtuellen Netzwerkgateways mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG" Hinweis: Sie müssen zunächst alle Verbindungen mit dem virtuellen Netzwerkgateway mithilfe des Cmdlets **Remove-AzVirtualNetworkGatewayConnection** löschen.</span><span class="sxs-lookup"><span data-stu-id="08329-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="08329-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="08329-111">PARAMETERS</span></span>

### <span data-ttu-id="08329-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08329-112">-AsJob</span></span>
<span data-ttu-id="08329-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="08329-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08329-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08329-114">-DefaultProfile</span></span>
<span data-ttu-id="08329-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08329-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08329-116">-Force</span><span class="sxs-lookup"><span data-stu-id="08329-116">-Force</span></span>
<span data-ttu-id="08329-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="08329-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08329-118">-Name</span><span class="sxs-lookup"><span data-stu-id="08329-118">-Name</span></span>
<span data-ttu-id="08329-119">Gibt den Namen des virtuellen Netzwerkgateways an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="08329-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="08329-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08329-120">-PassThru</span></span>
<span data-ttu-id="08329-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="08329-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="08329-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="08329-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08329-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08329-123">-ResourceGroupName</span></span>
<span data-ttu-id="08329-124">Gibt den Namen der Ressourcengruppe an, die das virtuelle Netzwerkgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="08329-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="08329-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08329-125">-Confirm</span></span>
<span data-ttu-id="08329-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08329-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08329-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08329-127">-WhatIf</span></span>
<span data-ttu-id="08329-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08329-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08329-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08329-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08329-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08329-130">CommonParameters</span></span>
<span data-ttu-id="08329-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08329-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08329-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08329-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08329-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08329-133">INPUTS</span></span>

### <span data-ttu-id="08329-134">System. String</span><span class="sxs-lookup"><span data-stu-id="08329-134">System.String</span></span>

## <span data-ttu-id="08329-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08329-135">OUTPUTS</span></span>

### <span data-ttu-id="08329-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08329-136">System.Boolean</span></span>

## <span data-ttu-id="08329-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="08329-137">NOTES</span></span>

## <span data-ttu-id="08329-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08329-138">RELATED LINKS</span></span>

[<span data-ttu-id="08329-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="08329-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="08329-140">Neu – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="08329-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="08329-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="08329-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="08329-142">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="08329-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="08329-143">Satz-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="08329-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
