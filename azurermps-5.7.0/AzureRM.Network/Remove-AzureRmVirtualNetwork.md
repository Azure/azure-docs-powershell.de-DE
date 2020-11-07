---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 945f1d8d12b4a493ca361c04ae14cd899f91956f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664903"
---
# <span data-ttu-id="1f675-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f675-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="1f675-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f675-102">SYNOPSIS</span></span>
<span data-ttu-id="1f675-103">Entfernt ein virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1f675-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f675-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f675-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f675-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f675-105">DESCRIPTION</span></span>
<span data-ttu-id="1f675-106">Das Cmdlet **Remove-AzureRmVirtualNetwork** entfernt ein Azure-virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1f675-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="1f675-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f675-107">EXAMPLES</span></span>

### <span data-ttu-id="1f675-108">1: Erstellen und Löschen eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="1f675-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="1f675-109">In diesem Beispiel wird ein virtuelles Netzwerk in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1f675-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="1f675-110">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Netzwerks zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="1f675-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="1f675-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f675-111">PARAMETERS</span></span>

### <span data-ttu-id="1f675-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f675-112">-AsJob</span></span>
<span data-ttu-id="1f675-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1f675-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f675-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f675-114">-DefaultProfile</span></span>
<span data-ttu-id="1f675-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f675-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f675-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1f675-116">-Force</span></span>
<span data-ttu-id="1f675-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1f675-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f675-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1f675-118">-Name</span></span>
<span data-ttu-id="1f675-119">Gibt den Namen des virtuellen Netzwerks an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1f675-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1f675-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f675-120">-PassThru</span></span>
<span data-ttu-id="1f675-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1f675-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f675-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="1f675-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f675-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f675-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f675-124">Gibt den Namen der Ressourcengruppe an, die das virtuelle Netzwerk enthält, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1f675-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1f675-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f675-125">-Confirm</span></span>
<span data-ttu-id="1f675-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f675-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f675-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f675-127">-WhatIf</span></span>
<span data-ttu-id="1f675-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f675-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f675-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f675-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f675-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f675-130">CommonParameters</span></span>
<span data-ttu-id="1f675-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f675-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f675-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f675-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f675-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f675-133">INPUTS</span></span>

### <span data-ttu-id="1f675-134">Keine</span><span class="sxs-lookup"><span data-stu-id="1f675-134">None</span></span>
<span data-ttu-id="1f675-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1f675-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f675-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f675-136">OUTPUTS</span></span>

## <span data-ttu-id="1f675-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f675-137">NOTES</span></span>

## <span data-ttu-id="1f675-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f675-138">RELATED LINKS</span></span>

[<span data-ttu-id="1f675-139">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f675-139">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="1f675-140">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f675-140">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="1f675-141">Satz-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f675-141">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


