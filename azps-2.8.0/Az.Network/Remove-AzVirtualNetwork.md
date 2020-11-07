---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 37dfce09dfcfc2dac3e561abc5957245d844763a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821331"
---
# <span data-ttu-id="6610b-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6610b-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="6610b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6610b-102">SYNOPSIS</span></span>
<span data-ttu-id="6610b-103">Entfernt ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6610b-103">Removes a virtual network.</span></span>

## <span data-ttu-id="6610b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6610b-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6610b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6610b-105">DESCRIPTION</span></span>
<span data-ttu-id="6610b-106">Das Cmdlet **Remove-AzVirtualNetwork** entfernt ein Azure-virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6610b-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="6610b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6610b-107">EXAMPLES</span></span>

### <span data-ttu-id="6610b-108">1: Erstellen und Löschen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="6610b-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="6610b-109">In diesem Beispiel wird ein virtuelles Netzwerk in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6610b-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="6610b-110">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Netzwerks zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="6610b-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="6610b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6610b-111">PARAMETERS</span></span>

### <span data-ttu-id="6610b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6610b-112">-AsJob</span></span>
<span data-ttu-id="6610b-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6610b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6610b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6610b-114">-DefaultProfile</span></span>
<span data-ttu-id="6610b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6610b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6610b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6610b-116">-Force</span></span>
<span data-ttu-id="6610b-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6610b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6610b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6610b-118">-Name</span></span>
<span data-ttu-id="6610b-119">Gibt den Namen des virtuellen Netzwerks an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6610b-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6610b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6610b-120">-PassThru</span></span>
<span data-ttu-id="6610b-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6610b-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6610b-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6610b-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6610b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6610b-123">-ResourceGroupName</span></span>
<span data-ttu-id="6610b-124">Gibt den Namen der Ressourcengruppe an, die das virtuelle Netzwerk enthält, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6610b-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6610b-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6610b-125">-Confirm</span></span>
<span data-ttu-id="6610b-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6610b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6610b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6610b-127">-WhatIf</span></span>
<span data-ttu-id="6610b-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6610b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6610b-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6610b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6610b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6610b-130">CommonParameters</span></span>
<span data-ttu-id="6610b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6610b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6610b-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6610b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6610b-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6610b-133">INPUTS</span></span>

### <span data-ttu-id="6610b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6610b-134">System.String</span></span>

## <span data-ttu-id="6610b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6610b-135">OUTPUTS</span></span>

### <span data-ttu-id="6610b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6610b-136">System.Boolean</span></span>

## <span data-ttu-id="6610b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="6610b-137">NOTES</span></span>

## <span data-ttu-id="6610b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6610b-138">RELATED LINKS</span></span>

[<span data-ttu-id="6610b-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6610b-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="6610b-140">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6610b-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="6610b-141">Satz-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6610b-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


