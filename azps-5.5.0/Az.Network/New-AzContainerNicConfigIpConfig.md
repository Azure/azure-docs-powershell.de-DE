---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 2e15819fe8b6b21b0f0c0751dc39736408606a7c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169865"
---
# <span data-ttu-id="f52ab-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f52ab-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="f52ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f52ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f52ab-103">Erstellt ein Konfigurations-IP-Konfigurationsobjekt für Container nic.</span><span class="sxs-lookup"><span data-stu-id="f52ab-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="f52ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f52ab-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f52ab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f52ab-105">DESCRIPTION</span></span>
<span data-ttu-id="f52ab-106">Das **Cmdlet "New-AzContainerNicConfigIpConfig"** erstellt eine neue Konfigurations-IP-Konfiguration der Container-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f52ab-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="f52ab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f52ab-107">EXAMPLES</span></span>

### <span data-ttu-id="f52ab-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f52ab-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="f52ab-109">Die ersten beiden Befehle erstellen und initialisieren ein Vnet und ein Subnetz.</span><span class="sxs-lookup"><span data-stu-id="f52ab-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="f52ab-110">Der dritte Befehl erstellt ein Container-nic-IP-Konfigurationsprofil, das auf das erstellte Subnetz bezugt.</span><span class="sxs-lookup"><span data-stu-id="f52ab-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="f52ab-111">Der vierte Befehl erstellt eine Containernetzwerkschnittstellenkonfiguration, die das im vorherigen Befehl erstellte IP-Konfigurationsprofil liefert.</span><span class="sxs-lookup"><span data-stu-id="f52ab-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="f52ab-112">Schließlich erstellt der fünfte Befehl ein Netzwerkprofil, das mit der container-Netzwerkschnittstellenkonfiguration initialisiert wird, die in der $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="f52ab-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="f52ab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f52ab-113">PARAMETERS</span></span>

### <span data-ttu-id="f52ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52ab-114">-DefaultProfile</span></span>
<span data-ttu-id="f52ab-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f52ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f52ab-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f52ab-116">-Name</span></span>
<span data-ttu-id="f52ab-117">Name des Konfigurations-IP-Konfigurationsprofils der Container-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f52ab-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="f52ab-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f52ab-118">-Subnet</span></span>
<span data-ttu-id="f52ab-119">Subnetz</span><span class="sxs-lookup"><span data-stu-id="f52ab-119">Subnet</span></span>

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

### <span data-ttu-id="f52ab-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f52ab-120">-SubnetId</span></span>
<span data-ttu-id="f52ab-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="f52ab-121">SubnetId</span></span>

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

### <span data-ttu-id="f52ab-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f52ab-122">-Confirm</span></span>
<span data-ttu-id="f52ab-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f52ab-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f52ab-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f52ab-124">-WhatIf</span></span>
<span data-ttu-id="f52ab-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f52ab-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f52ab-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f52ab-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f52ab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52ab-127">CommonParameters</span></span>
<span data-ttu-id="f52ab-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f52ab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52ab-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f52ab-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52ab-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f52ab-130">INPUTS</span></span>

### <span data-ttu-id="f52ab-131">Keine</span><span class="sxs-lookup"><span data-stu-id="f52ab-131">None</span></span>

## <span data-ttu-id="f52ab-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f52ab-132">OUTPUTS</span></span>

### <span data-ttu-id="f52ab-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f52ab-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="f52ab-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f52ab-134">NOTES</span></span>

## <span data-ttu-id="f52ab-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f52ab-135">RELATED LINKS</span></span>

[<span data-ttu-id="f52ab-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f52ab-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
