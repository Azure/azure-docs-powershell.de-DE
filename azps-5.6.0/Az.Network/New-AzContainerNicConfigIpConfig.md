---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 6ed82377de2a87b3bc40d3d4e8dff6af751ed1f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921912"
---
# <span data-ttu-id="282ce-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="282ce-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="282ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="282ce-102">SYNOPSIS</span></span>
<span data-ttu-id="282ce-103">Erstellt ein Ip-Konfigurationsobjekt für containernic configuration.</span><span class="sxs-lookup"><span data-stu-id="282ce-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="282ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="282ce-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="282ce-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="282ce-105">DESCRIPTION</span></span>
<span data-ttu-id="282ce-106">Das **Cmdlet New-AzContainerNicConfigIpConfig** erstellt eine neue Ip-Konfiguration der Containernetzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="282ce-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="282ce-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="282ce-107">EXAMPLES</span></span>

### <span data-ttu-id="282ce-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="282ce-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="282ce-109">Die ersten beiden Befehle erstellen und initialisieren ein Vnet und ein Subnetz.</span><span class="sxs-lookup"><span data-stu-id="282ce-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="282ce-110">Mit dem dritten Befehl wird ein Containernic-IP-Konfigurationsprofil erstellt, das auf das erstellte Subnetz bezugt.</span><span class="sxs-lookup"><span data-stu-id="282ce-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="282ce-111">Der vierte Befehl erstellt eine Containernetzwerkschnittstellenkonfiguration, die das im vorherigen Befehl erstellte IP-Konfigurationsprofil liefert.</span><span class="sxs-lookup"><span data-stu-id="282ce-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="282ce-112">Schließlich erstellt der fünfte Befehl ein Netzwerkprofil, das mit der Containernetzwerkschnittstellenkonfiguration initialisiert wurde, die in $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="282ce-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="282ce-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="282ce-113">PARAMETERS</span></span>

### <span data-ttu-id="282ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="282ce-114">-DefaultProfile</span></span>
<span data-ttu-id="282ce-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="282ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="282ce-116">-Name</span><span class="sxs-lookup"><span data-stu-id="282ce-116">-Name</span></span>
<span data-ttu-id="282ce-117">Name des Ip-Konfigurationsprofils der Containernetzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="282ce-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="282ce-118">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="282ce-118">-Subnet</span></span>
<span data-ttu-id="282ce-119">Subnetz</span><span class="sxs-lookup"><span data-stu-id="282ce-119">Subnet</span></span>

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

### <span data-ttu-id="282ce-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="282ce-120">-SubnetId</span></span>
<span data-ttu-id="282ce-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="282ce-121">SubnetId</span></span>

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

### <span data-ttu-id="282ce-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="282ce-122">-Confirm</span></span>
<span data-ttu-id="282ce-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="282ce-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="282ce-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="282ce-124">-WhatIf</span></span>
<span data-ttu-id="282ce-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="282ce-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="282ce-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="282ce-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="282ce-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="282ce-127">CommonParameters</span></span>
<span data-ttu-id="282ce-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="282ce-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="282ce-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="282ce-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="282ce-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="282ce-130">INPUTS</span></span>

### <span data-ttu-id="282ce-131">Keine</span><span class="sxs-lookup"><span data-stu-id="282ce-131">None</span></span>

## <span data-ttu-id="282ce-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="282ce-132">OUTPUTS</span></span>

### <span data-ttu-id="282ce-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="282ce-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="282ce-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="282ce-134">NOTES</span></span>

## <span data-ttu-id="282ce-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="282ce-135">RELATED LINKS</span></span>

[<span data-ttu-id="282ce-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="282ce-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
