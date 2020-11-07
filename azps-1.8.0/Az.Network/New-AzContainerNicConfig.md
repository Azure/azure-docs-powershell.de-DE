---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 18d5891e07dd9d0f9916ebf43e8967152e2c9cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660570"
---
# <span data-ttu-id="0d831-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0d831-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="0d831-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d831-102">SYNOPSIS</span></span>
<span data-ttu-id="0d831-103">Erstellt ein neues Configuration-Objekt der Container-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0d831-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="0d831-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d831-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d831-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d831-105">DESCRIPTION</span></span>
<span data-ttu-id="0d831-106">Das Cmdlet **New-AzContainerNicConfig** erstellt ein neues Configuration-Objekt für die Container-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0d831-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="0d831-107">Dieses Objekt bestimmt die Eigenschaften von Container Netzwerk-interfacs, die auf das übergeordnete Netzwerkprofil verweisen.</span><span class="sxs-lookup"><span data-stu-id="0d831-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="0d831-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d831-108">EXAMPLES</span></span>

### <span data-ttu-id="0d831-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0d831-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="0d831-110">Der erste Befehl erstellt eine leere Container-Netzwerkschnittstellenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d831-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="0d831-111">Die zweite erstellt ein neues Netzwerkprofil und übergibt die zuvor erstellte Container-Netzwerkschnittstellenkonfiguration als Argument an das New-NetworkProfile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d831-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="0d831-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d831-112">PARAMETERS</span></span>

### <span data-ttu-id="0d831-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d831-113">-DefaultProfile</span></span>
<span data-ttu-id="0d831-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d831-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d831-115">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="0d831-115">-IpConfiguration</span></span>
<span data-ttu-id="0d831-116">Sammlung von IP-Konfigurationsprofilen, die ermitteln, welche IP-Konfigurationen erstellt werden, wenn eine Container-NIC aus dieser Container-Netzwerkschnittstellenkonfiguration instanziiert wird</span><span class="sxs-lookup"><span data-stu-id="0d831-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d831-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0d831-117">-Name</span></span>
<span data-ttu-id="0d831-118">Name der Konfiguration der Container-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0d831-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="0d831-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d831-119">-Confirm</span></span>
<span data-ttu-id="0d831-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d831-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d831-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d831-121">-WhatIf</span></span>
<span data-ttu-id="0d831-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d831-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d831-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d831-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d831-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d831-124">CommonParameters</span></span>
<span data-ttu-id="0d831-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d831-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d831-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d831-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d831-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d831-127">INPUTS</span></span>

### <span data-ttu-id="0d831-128">Microsoft. Azure. Commands. Network. Models. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="0d831-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="0d831-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d831-129">OUTPUTS</span></span>

### <span data-ttu-id="0d831-130">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d831-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="0d831-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d831-131">NOTES</span></span>

## <span data-ttu-id="0d831-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d831-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d831-133">Neu – AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0d831-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
