---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 7665170d5ca71e73e787dbe22e84f3372497c687
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660510"
---
# <span data-ttu-id="2d8ec-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d8ec-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="2d8ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="2d8ec-103">Erstellt eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-103">Creates a network security group.</span></span>

## <span data-ttu-id="2d8ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d8ec-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d8ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d8ec-105">DESCRIPTION</span></span>
<span data-ttu-id="2d8ec-106">Das Cmdlet **New-AzNetworkSecurityGroup** erstellt eine Azure Network Security-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="2d8ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d8ec-107">EXAMPLES</span></span>

### <span data-ttu-id="2d8ec-108">1: Erstellen einer neuen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="2d8ec-108">1: Create a new network security group</span></span>
```
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="2d8ec-109">Mit diesem Befehl wird eine neue Azure Network Security-Gruppe mit dem Namen "nsg1" in der Ressourcengruppe "RG1" an der Position "westus" erstellt.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="2d8ec-110">2: Erstellen einer detaillierten Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="2d8ec-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="2d8ec-111">Schritt: 1 erstellen Sie eine Sicherheitsregel, die den Zugriff vom Internet auf Port 3389 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="2d8ec-112">Schritt: 2 Erstellen einer Sicherheitsregel, die den Zugriff aus dem Internet auf Port 80 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="2d8ec-113">Schritt: 3 Fügen Sie die oben erstellten Regeln zu einem neuen NSG mit dem Namen NSG-Frontend hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="2d8ec-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d8ec-114">PARAMETERS</span></span>

### <span data-ttu-id="2d8ec-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d8ec-115">-AsJob</span></span>
<span data-ttu-id="2d8ec-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2d8ec-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d8ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d8ec-117">-DefaultProfile</span></span>
<span data-ttu-id="2d8ec-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d8ec-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2d8ec-119">-Force</span></span>
<span data-ttu-id="2d8ec-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d8ec-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="2d8ec-121">-Location</span></span>
<span data-ttu-id="2d8ec-122">Gibt den Bereich an, für den eine Netzwerksicherheitsgruppe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="2d8ec-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2d8ec-123">-Name</span></span>
<span data-ttu-id="2d8ec-124">Gibt den Namen der zu erstellende Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="2d8ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d8ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d8ec-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2d8ec-127">Mit diesem Cmdlet wird in der Ressourcengruppe, die dieser Parameter angibt, eine Netzwerksicherheitsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2d8ec-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="2d8ec-128">-SecurityRules</span></span>
<span data-ttu-id="2d8ec-129">Gibt eine Liste der Netzwerk Sicherheitsregel Objekte an, die in einer Netzwerksicherheitsgruppe erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="2d8ec-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d8ec-130">-Tag</span></span>
<span data-ttu-id="2d8ec-131">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2d8ec-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2d8ec-132">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2d8ec-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2d8ec-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d8ec-133">-Confirm</span></span>
<span data-ttu-id="2d8ec-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d8ec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d8ec-135">-WhatIf</span></span>
<span data-ttu-id="2d8ec-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d8ec-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d8ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d8ec-138">CommonParameters</span></span>
<span data-ttu-id="2d8ec-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d8ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d8ec-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d8ec-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d8ec-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d8ec-141">INPUTS</span></span>

### <span data-ttu-id="2d8ec-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2d8ec-142">System.String</span></span>

### <span data-ttu-id="2d8ec-143">Microsoft. Azure. Commands. Network. Models. PSSecurityRule []</span><span class="sxs-lookup"><span data-stu-id="2d8ec-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="2d8ec-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d8ec-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d8ec-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d8ec-145">OUTPUTS</span></span>

### <span data-ttu-id="2d8ec-146">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d8ec-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="2d8ec-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d8ec-147">NOTES</span></span>

## <span data-ttu-id="2d8ec-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d8ec-148">RELATED LINKS</span></span>

[<span data-ttu-id="2d8ec-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d8ec-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="2d8ec-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d8ec-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="2d8ec-151">Satz-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d8ec-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
