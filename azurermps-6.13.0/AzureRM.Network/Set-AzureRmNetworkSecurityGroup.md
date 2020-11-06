---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 3ef8248f90e24da8818a0fa1a8ff6b05970be397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475998"
---
# <span data-ttu-id="0a483-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a483-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="0a483-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a483-102">SYNOPSIS</span></span>
<span data-ttu-id="0a483-103">Legt den Zielstatus für eine Netzwerksicherheitsgruppe fest.</span><span class="sxs-lookup"><span data-stu-id="0a483-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a483-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a483-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a483-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a483-105">DESCRIPTION</span></span>
<span data-ttu-id="0a483-106">Das Cmdlet " **Set-AzureRmNetworkSecurityGroup** " legt den Zielstatus für eine Azure Network Security-Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="0a483-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="0a483-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a483-107">EXAMPLES</span></span>

### <span data-ttu-id="0a483-108">Beispiel 1: Festlegung des Zielstatus für eine Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="0a483-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="0a483-109">Dieser Befehl ruft die Azure Network Security-Gruppe mit dem Namen Nsg1 ab und fügt eine Netzwerk Sicherheitsregel mit dem Namen Rdp-Rule hinzu, um den Internet Datenverkehr auf Port 3389 dem abgerufenen Netzwerk Sicherheitsgruppenobjekt mithilfe von Add-AzureRmNetworkSecurityRuleConfig zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0a483-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="0a483-110">Der Befehl behält die geänderte Azure Network Security-Gruppe mithilfe von " **AzureRmNetworkSecurityGroup** " bei.</span><span class="sxs-lookup"><span data-stu-id="0a483-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="0a483-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a483-111">PARAMETERS</span></span>

### <span data-ttu-id="0a483-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a483-112">-AsJob</span></span>
<span data-ttu-id="0a483-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0a483-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a483-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a483-114">-DefaultProfile</span></span>
<span data-ttu-id="0a483-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a483-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a483-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a483-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0a483-117">Ein Netzwerk Sicherheitsgruppenobjekt, das den Zielstatus darstellt, zu dem das Cmdlet die Netzwerksicherheitsgruppe festlegt.</span><span class="sxs-lookup"><span data-stu-id="0a483-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a483-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a483-118">-Confirm</span></span>
<span data-ttu-id="0a483-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a483-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a483-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a483-120">-WhatIf</span></span>
<span data-ttu-id="0a483-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a483-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a483-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a483-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a483-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a483-123">CommonParameters</span></span>
<span data-ttu-id="0a483-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a483-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a483-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a483-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a483-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a483-126">INPUTS</span></span>

### <span data-ttu-id="0a483-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a483-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="0a483-128">Parameter: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0a483-128">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="0a483-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a483-129">OUTPUTS</span></span>

### <span data-ttu-id="0a483-130">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a483-130">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0a483-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a483-131">NOTES</span></span>

## <span data-ttu-id="0a483-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a483-132">RELATED LINKS</span></span>

[<span data-ttu-id="0a483-133">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a483-133">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="0a483-134">Neu – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a483-134">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="0a483-135">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a483-135">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


