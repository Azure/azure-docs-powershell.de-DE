---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 9e52131bd5f53d48b4c958c26a0ef37b5ebd23ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370766"
---
# <span data-ttu-id="8a9c4-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a9c4-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="8a9c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a9c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9c4-103">Fügt dem VMSS eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="8a9c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a9c4-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a9c4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a9c4-105">DESCRIPTION</span></span>
<span data-ttu-id="8a9c4-106">Das **Cmdlet "Add-AzVmssNetworkInterfaceConfiguration"** fügt dem Virtual Machine Scale Set (VMSS) eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8a9c4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a9c4-107">EXAMPLES</span></span>

### <span data-ttu-id="8a9c4-108">Beispiel 1: Hinzufügen einer Netzwerkschnittstellenkonfiguration zu VMSS</span><span class="sxs-lookup"><span data-stu-id="8a9c4-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="8a9c4-109">Dieser Befehl fügt dem VMSS eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="8a9c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a9c4-110">PARAMETERS</span></span>

### <span data-ttu-id="8a9c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9c4-111">-DefaultProfile</span></span>
<span data-ttu-id="8a9c4-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a9c4-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="8a9c4-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="8a9c4-114">Liste der DNS-Server-IP-Adressen für dns-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c4-115">-EnableAcce 2010Networking</span><span class="sxs-lookup"><span data-stu-id="8a9c4-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="8a9c4-116">Gibt an, ob die Netzwerkschnittstelle netzwerkfähig ist.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="8a9c4-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="8a9c4-117">-EnableIPForwarding</span></span>
<span data-ttu-id="8a9c4-118">Gibt an, ob die IP-Weiterleitung auf dieser NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="8a9c4-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8a9c4-119">-Id</span></span>
<span data-ttu-id="8a9c4-120">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c4-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a9c4-121">-IpConfiguration</span></span>
<span data-ttu-id="8a9c4-122">Gibt die IP-Konfigurationen der Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8a9c4-123">-Name</span></span>
<span data-ttu-id="8a9c4-124">Gibt den Namen der Netzwerkschnittstellenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c4-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8a9c4-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="8a9c4-126">DIE ID der Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-126">Id of the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c4-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="8a9c4-127">-Primary</span></span>
<span data-ttu-id="8a9c4-128">Gibt an, ob Netzwerkschnittstellen, die aus der Konfiguration der Netzwerkschnittstelle erstellt werden, das primäre Netzwerkinformationscenter (Network Information Center, NIC) des virtuellen Computers sein.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c4-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a9c4-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8a9c4-130">Gibt das "VMSS"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="8a9c4-131">Sie können das [Cmdlet "New-AzVmssConfig"](./New-AzVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9c4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a9c4-132">-Confirm</span></span>
<span data-ttu-id="8a9c4-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a9c4-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8a9c4-134">-WhatIf</span></span>
<span data-ttu-id="8a9c4-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a9c4-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a9c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9c4-137">CommonParameters</span></span>
<span data-ttu-id="8a9c4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a9c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9c4-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a9c4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9c4-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a9c4-140">INPUTS</span></span>

### <span data-ttu-id="8a9c4-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a9c4-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8a9c4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8a9c4-142">System.String</span></span>

### <span data-ttu-id="8a9c4-143">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8a9c4-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8a9c4-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="8a9c4-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="8a9c4-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8a9c4-145">System.String[]</span></span>

## <span data-ttu-id="8a9c4-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a9c4-146">OUTPUTS</span></span>

### <span data-ttu-id="8a9c4-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a9c4-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8a9c4-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8a9c4-148">NOTES</span></span>

## <span data-ttu-id="8a9c4-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8a9c4-149">RELATED LINKS</span></span>

[<span data-ttu-id="8a9c4-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8a9c4-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
