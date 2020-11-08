---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 593891c19b9748c7a32019cfdaee0d069329cbea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173209"
---
# <span data-ttu-id="a862c-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a862c-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="a862c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a862c-102">SYNOPSIS</span></span>
<span data-ttu-id="a862c-103">Erstellt eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a862c-103">Creates a network security group.</span></span>

## <span data-ttu-id="a862c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a862c-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a862c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a862c-105">DESCRIPTION</span></span>
<span data-ttu-id="a862c-106">Das Cmdlet **New-AzNetworkSecurityGroup** erstellt eine Azure Network Security-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a862c-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="a862c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a862c-107">EXAMPLES</span></span>

### <span data-ttu-id="a862c-108">Beispiel 1: Erstellen einer neuen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="a862c-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="a862c-109">Mit diesem Befehl wird eine neue Azure Network Security-Gruppe mit dem Namen "nsg1" in der Ressourcengruppe "RG1" an der Position "westus" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a862c-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="a862c-110">Beispiel 2: Erstellen einer detaillierten Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="a862c-110">Example 2: Create a detailed network security group</span></span>
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

<span data-ttu-id="a862c-111">Schritt: 1 erstellen Sie eine Sicherheitsregel, die den Zugriff vom Internet auf Port 3389 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a862c-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="a862c-112">Schritt: 2 Erstellen einer Sicherheitsregel, die den Zugriff aus dem Internet auf Port 80 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a862c-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="a862c-113">Schritt: 3 Fügen Sie die oben erstellten Regeln zu einem neuen NSG mit dem Namen NSG-Frontend hinzu.</span><span class="sxs-lookup"><span data-stu-id="a862c-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="a862c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a862c-114">PARAMETERS</span></span>

### <span data-ttu-id="a862c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a862c-115">-AsJob</span></span>
<span data-ttu-id="a862c-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a862c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a862c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a862c-117">-DefaultProfile</span></span>
<span data-ttu-id="a862c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a862c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a862c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a862c-119">-Force</span></span>
<span data-ttu-id="a862c-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a862c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a862c-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="a862c-121">-Location</span></span>
<span data-ttu-id="a862c-122">Gibt den Bereich an, für den eine Netzwerksicherheitsgruppe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a862c-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="a862c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a862c-123">-Name</span></span>
<span data-ttu-id="a862c-124">Gibt den Namen der zu erstellende Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a862c-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="a862c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a862c-125">-ResourceGroupName</span></span>
<span data-ttu-id="a862c-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a862c-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a862c-127">Mit diesem Cmdlet wird in der Ressourcengruppe, die dieser Parameter angibt, eine Netzwerksicherheitsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="a862c-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a862c-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="a862c-128">-SecurityRules</span></span>
<span data-ttu-id="a862c-129">Gibt eine Liste der Netzwerk Sicherheitsregel Objekte an, die in einer Netzwerksicherheitsgruppe erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a862c-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="a862c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a862c-130">-Tag</span></span>
<span data-ttu-id="a862c-131">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="a862c-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a862c-132">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="a862c-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a862c-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a862c-133">-Confirm</span></span>
<span data-ttu-id="a862c-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a862c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a862c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a862c-135">-WhatIf</span></span>
<span data-ttu-id="a862c-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a862c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a862c-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a862c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a862c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a862c-138">CommonParameters</span></span>
<span data-ttu-id="a862c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a862c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a862c-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a862c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a862c-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a862c-141">INPUTS</span></span>

### <span data-ttu-id="a862c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a862c-142">System.String</span></span>

### <span data-ttu-id="a862c-143">Microsoft. Azure. Commands. Network. Models. PSSecurityRule []</span><span class="sxs-lookup"><span data-stu-id="a862c-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="a862c-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a862c-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a862c-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a862c-145">OUTPUTS</span></span>

### <span data-ttu-id="a862c-146">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a862c-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a862c-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="a862c-147">NOTES</span></span>

## <span data-ttu-id="a862c-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a862c-148">RELATED LINKS</span></span>

[<span data-ttu-id="a862c-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a862c-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a862c-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a862c-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a862c-151">Satz-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a862c-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
