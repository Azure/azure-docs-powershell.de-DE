---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 001023fd313db4228d7fb1f155b5a686f9649277
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919579"
---
# <span data-ttu-id="9b4b8-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b4b8-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="9b4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4b8-103">Erstellt eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-103">Creates a network security group.</span></span>

## <span data-ttu-id="9b4b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b4b8-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b4b8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="9b4b8-106">Das **Cmdlet New-AzNetworkSecurityGroup** erstellt eine Azure-Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="9b4b8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b4b8-107">EXAMPLES</span></span>

### <span data-ttu-id="9b4b8-108">Beispiel 1: Erstellen einer neuen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="9b4b8-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="9b4b8-109">Mit diesem Befehl wird eine neue Azure-Netzwerksicherheitsgruppe mit dem Namen "nsg1" in der Ressourcengruppe "rg1" am Speicherort "westus" erstellt.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="9b4b8-110">Beispiel 2: Erstellen einer detaillierten Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="9b4b8-110">Example 2: Create a detailed network security group</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name `
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="9b4b8-111">Schritt:1 Erstellen Sie eine Sicherheitsregel, die den Zugriff aus dem Internet auf Port 3389 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="9b4b8-112">Schritt:2 Erstellen Sie eine Sicherheitsregel, die den Zugriff aus dem Internet auf Port 80 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="9b4b8-113">Schritt:3 Fügen Sie die oben erstellten Regeln einem neuen NSG namens NSG-FrontEnd hinzu.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="9b4b8-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9b4b8-114">PARAMETERS</span></span>

### <span data-ttu-id="9b4b8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b4b8-115">-AsJob</span></span>
<span data-ttu-id="9b4b8-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9b4b8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b4b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4b8-117">-DefaultProfile</span></span>
<span data-ttu-id="9b4b8-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b4b8-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="9b4b8-119">-Force</span></span>
<span data-ttu-id="9b4b8-120">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9b4b8-121">-Location</span><span class="sxs-lookup"><span data-stu-id="9b4b8-121">-Location</span></span>
<span data-ttu-id="9b4b8-122">Gibt die Region an, für die eine Netzwerksicherheitsgruppe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="9b4b8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9b4b8-123">-Name</span></span>
<span data-ttu-id="9b4b8-124">Gibt den Namen der zu erstellenden Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="9b4b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b4b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b4b8-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9b4b8-127">Dieses Cmdlet erstellt eine Netzwerksicherheitsgruppe in der Ressourcengruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b4b8-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="9b4b8-128">-SecurityRules</span></span>
<span data-ttu-id="9b4b8-129">Gibt eine Liste der Netzwerksicherheitsregelobjekte an, die in einer Netzwerksicherheitsgruppe erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b4b8-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b4b8-130">-Tag</span></span>
<span data-ttu-id="9b4b8-131">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9b4b8-132">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9b4b8-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9b4b8-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b4b8-133">-Confirm</span></span>
<span data-ttu-id="9b4b8-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b4b8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b4b8-135">-WhatIf</span></span>
<span data-ttu-id="9b4b8-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b4b8-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b4b8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4b8-138">CommonParameters</span></span>
<span data-ttu-id="9b4b8-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4b8-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b4b8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4b8-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b4b8-141">INPUTS</span></span>

### <span data-ttu-id="9b4b8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9b4b8-142">System.String</span></span>

### <span data-ttu-id="9b4b8-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span><span class="sxs-lookup"><span data-stu-id="9b4b8-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="9b4b8-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b4b8-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b4b8-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b4b8-145">OUTPUTS</span></span>

### <span data-ttu-id="9b4b8-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b4b8-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="9b4b8-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9b4b8-147">NOTES</span></span>

## <span data-ttu-id="9b4b8-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9b4b8-148">RELATED LINKS</span></span>

[<span data-ttu-id="9b4b8-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b4b8-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="9b4b8-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b4b8-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="9b4b8-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b4b8-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
