---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: f2d9781f205df70e5becbc53f597f27791ca6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662908"
---
# <span data-ttu-id="255ac-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="255ac-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="255ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="255ac-102">SYNOPSIS</span></span>
<span data-ttu-id="255ac-103">Erstellt eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="255ac-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="255ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="255ac-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="255ac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="255ac-105">DESCRIPTION</span></span>
<span data-ttu-id="255ac-106">Das Cmdlet **New-AzureRmNetworkSecurityGroup** erstellt eine Azure Network Security-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="255ac-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="255ac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="255ac-107">EXAMPLES</span></span>

### <span data-ttu-id="255ac-108">1: Erstellen einer neuen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="255ac-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="255ac-109">Mit diesem Befehl wird eine neue Azure Network Security-Gruppe mit dem Namen "nsg1" in der Ressourcengruppe "RG1" an der Position "westus" erstellt.</span><span class="sxs-lookup"><span data-stu-id="255ac-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="255ac-110">2: Erstellen einer detaillierten Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="255ac-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="255ac-111">Schritt: 1 erstellen Sie eine Sicherheitsregel, die den Zugriff vom Internet auf Port 3389 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="255ac-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="255ac-112">Schritt: 2 Erstellen einer Sicherheitsregel, die den Zugriff aus dem Internet auf Port 80 ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="255ac-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="255ac-113">Schritt: 3 Fügen Sie die oben erstellten Regeln zu einem neuen NSG mit dem Namen NSG-Frontend hinzu.</span><span class="sxs-lookup"><span data-stu-id="255ac-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="255ac-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="255ac-114">PARAMETERS</span></span>

### <span data-ttu-id="255ac-115">-Force</span><span class="sxs-lookup"><span data-stu-id="255ac-115">-Force</span></span>
<span data-ttu-id="255ac-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="255ac-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="255ac-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="255ac-117">-Location</span></span>
<span data-ttu-id="255ac-118">Gibt den Bereich an, für den eine Netzwerksicherheitsgruppe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="255ac-118">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="255ac-119">-Name</span><span class="sxs-lookup"><span data-stu-id="255ac-119">-Name</span></span>
<span data-ttu-id="255ac-120">Gibt den Namen der zu erstellende Netzwerksicherheitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="255ac-120">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="255ac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="255ac-121">-ResourceGroupName</span></span>
<span data-ttu-id="255ac-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="255ac-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="255ac-123">Mit diesem Cmdlet wird in der Ressourcengruppe, die dieser Parameter angibt, eine Netzwerksicherheitsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="255ac-123">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="255ac-124">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="255ac-124">-SecurityRules</span></span>
<span data-ttu-id="255ac-125">Gibt eine Liste der Netzwerk Sicherheitsregel Objekte an, die in einer Netzwerksicherheitsgruppe erstellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="255ac-125">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255ac-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="255ac-126">-Tag</span></span>
<span data-ttu-id="255ac-127">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="255ac-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="255ac-128">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="255ac-128">For example:</span></span>

<span data-ttu-id="255ac-129">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="255ac-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="255ac-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="255ac-130">-Confirm</span></span>
<span data-ttu-id="255ac-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="255ac-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="255ac-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="255ac-132">-WhatIf</span></span>
<span data-ttu-id="255ac-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="255ac-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="255ac-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="255ac-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="255ac-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255ac-135">-DefaultProfile</span></span>
<span data-ttu-id="255ac-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="255ac-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255ac-137">CommonParameters</span></span>
<span data-ttu-id="255ac-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="255ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255ac-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="255ac-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255ac-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="255ac-140">INPUTS</span></span>

## <span data-ttu-id="255ac-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="255ac-141">OUTPUTS</span></span>

### <span data-ttu-id="255ac-142">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="255ac-142">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="255ac-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="255ac-143">NOTES</span></span>

## <span data-ttu-id="255ac-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="255ac-144">RELATED LINKS</span></span>

[<span data-ttu-id="255ac-145">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="255ac-145">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="255ac-146">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="255ac-146">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="255ac-147">Satz-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="255ac-147">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
