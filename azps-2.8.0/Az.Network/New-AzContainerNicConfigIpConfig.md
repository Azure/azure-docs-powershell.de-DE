---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 24cbdaebc21456268d050b5c3a56ec9fc443fedf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821635"
---
# <span data-ttu-id="73f74-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="73f74-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="73f74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73f74-102">SYNOPSIS</span></span>
<span data-ttu-id="73f74-103">Erstellt ein IP-Konfigurationsobjekt für die Container-NIC-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="73f74-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="73f74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73f74-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f74-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73f74-105">DESCRIPTION</span></span>
<span data-ttu-id="73f74-106">Das Cmdlet **New-AzContainerNicConfigIpConfig** erstellt eine neue IP-Konfiguration für die Container-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="73f74-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="73f74-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73f74-107">EXAMPLES</span></span>

### <span data-ttu-id="73f74-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73f74-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="73f74-109">Mit den ersten beiden Befehlen wird ein vnet und ein Subnetz erstellt und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="73f74-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="73f74-110">Der dritte Befehl erstellt ein Container-NIC-IP-Konfigurationsprofil, das auf das erstellte Subnetz verweist.</span><span class="sxs-lookup"><span data-stu-id="73f74-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="73f74-111">Der vierte Befehl erstellt eine Container-Netzwerkschnittstellenkonfiguration, die das im vorherigen Befehl erstellte IP-Konfigurationsprofil bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="73f74-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="73f74-112">Schließlich erstellt der fünfte Befehl ein Netzwerkprofil, das mit der in $containerNicConfig gespeicherten Container-Netzwerkschnittstellenkonfiguration initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="73f74-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="73f74-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="73f74-113">PARAMETERS</span></span>

### <span data-ttu-id="73f74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f74-114">-DefaultProfile</span></span>
<span data-ttu-id="73f74-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73f74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f74-116">-Name</span><span class="sxs-lookup"><span data-stu-id="73f74-116">-Name</span></span>
<span data-ttu-id="73f74-117">Name des Konfiguration-IP-Konfigurationsprofils der Container-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="73f74-117">Name of the container network interface configuration ip configuration profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f74-118">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="73f74-118">-Subnet</span></span>
<span data-ttu-id="73f74-119">Subnetz</span><span class="sxs-lookup"><span data-stu-id="73f74-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f74-120">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="73f74-120">-SubnetId</span></span>
<span data-ttu-id="73f74-121">Subnetz</span><span class="sxs-lookup"><span data-stu-id="73f74-121">SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73f74-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73f74-122">-Confirm</span></span>
<span data-ttu-id="73f74-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73f74-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f74-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f74-124">-WhatIf</span></span>
<span data-ttu-id="73f74-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73f74-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73f74-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73f74-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f74-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f74-127">CommonParameters</span></span>
<span data-ttu-id="73f74-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f74-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f74-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73f74-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f74-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73f74-130">INPUTS</span></span>

### <span data-ttu-id="73f74-131">Keine</span><span class="sxs-lookup"><span data-stu-id="73f74-131">None</span></span>

## <span data-ttu-id="73f74-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73f74-132">OUTPUTS</span></span>

### <span data-ttu-id="73f74-133">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="73f74-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="73f74-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="73f74-134">NOTES</span></span>

## <span data-ttu-id="73f74-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73f74-135">RELATED LINKS</span></span>

[<span data-ttu-id="73f74-136">Neu – AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="73f74-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
