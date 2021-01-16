---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 593891c19b9748c7a32019cfdaee0d069329cbea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298283"
---
# <span data-ttu-id="a2b9d-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2b9d-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="a2b9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b9d-103">Erstellt eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-103">Creates a network security group.</span></span>

## <span data-ttu-id="a2b9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2b9d-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2b9d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2b9d-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b9d-106">Das **Cmdlet "New-AzNetworkSecurityGroup"** erstellt eine Azure-Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="a2b9d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2b9d-107">EXAMPLES</span></span>

### <span data-ttu-id="a2b9d-108">Beispiel 1: Erstellen einer neuen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="a2b9d-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="a2b9d-109">Mit diesem Befehl wird eine neue Azure-Netzwerksicherheitsgruppe mit dem Namen "nsg1" in der Ressourcengruppe "rg1" am Standort "westus" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="a2b9d-110">Beispiel 2: Erstellen einer detaillierten Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="a2b9d-110">Example 2: Create a detailed network security group</span></span>
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

<span data-ttu-id="a2b9d-111">Schritt:1 Erstellen Sie eine Sicherheitsregel, die den Zugriff über das Internet auf Port 3389 zu ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="a2b9d-112">Schritt:2 Erstellen Sie eine Sicherheitsregel, die den Zugriff über das Internet auf Port 80 zu ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="a2b9d-113">Schritt:3 Fügen Sie die oben erstellten Regeln einem neuen NSG namens "NSG-FrontEnd" hinzu.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="a2b9d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2b9d-114">PARAMETERS</span></span>

### <span data-ttu-id="a2b9d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2b9d-115">-AsJob</span></span>
<span data-ttu-id="a2b9d-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a2b9d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2b9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b9d-117">-DefaultProfile</span></span>
<span data-ttu-id="a2b9d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b9d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a2b9d-119">-Force</span></span>
<span data-ttu-id="a2b9d-120">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a2b9d-121">-Location</span><span class="sxs-lookup"><span data-stu-id="a2b9d-121">-Location</span></span>
<span data-ttu-id="a2b9d-122">Gibt die Region an, für die eine Netzwerksicherheitsgruppe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="a2b9d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a2b9d-123">-Name</span></span>
<span data-ttu-id="a2b9d-124">Gibt den Namen der zu erstellenden Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="a2b9d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b9d-125">-ResourceGroupName</span></span>
<span data-ttu-id="a2b9d-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a2b9d-127">Dieses Cmdlet erstellt eine Netzwerksicherheitsgruppe in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2b9d-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="a2b9d-128">-SecurityRules</span></span>
<span data-ttu-id="a2b9d-129">Gibt eine Liste der Netzwerksicherheitsregelobjekte an, die in einer Netzwerksicherheitsgruppe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="a2b9d-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a2b9d-130">-Tag</span></span>
<span data-ttu-id="a2b9d-131">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a2b9d-132">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a2b9d-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a2b9d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2b9d-133">-Confirm</span></span>
<span data-ttu-id="a2b9d-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2b9d-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a2b9d-135">-WhatIf</span></span>
<span data-ttu-id="a2b9d-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2b9d-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2b9d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b9d-138">CommonParameters</span></span>
<span data-ttu-id="a2b9d-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b9d-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b9d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b9d-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2b9d-141">INPUTS</span></span>

### <span data-ttu-id="a2b9d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a2b9d-142">System.String</span></span>

### <span data-ttu-id="a2b9d-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span><span class="sxs-lookup"><span data-stu-id="a2b9d-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="a2b9d-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2b9d-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a2b9d-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2b9d-145">OUTPUTS</span></span>

### <span data-ttu-id="a2b9d-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2b9d-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a2b9d-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a2b9d-147">NOTES</span></span>

## <span data-ttu-id="a2b9d-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a2b9d-148">RELATED LINKS</span></span>

[<span data-ttu-id="a2b9d-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2b9d-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a2b9d-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2b9d-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a2b9d-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a2b9d-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
