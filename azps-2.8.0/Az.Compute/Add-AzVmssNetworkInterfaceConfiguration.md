---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 6bc89141d6e822ac8727f40b5b331afa00685e12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652208"
---
# <span data-ttu-id="46079-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="46079-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="46079-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46079-102">SYNOPSIS</span></span>
<span data-ttu-id="46079-103">Fügt der VMSS eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="46079-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="46079-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46079-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46079-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46079-105">DESCRIPTION</span></span>
<span data-ttu-id="46079-106">Das **Add-AzVmssNetworkInterfaceConfiguration-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="46079-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="46079-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46079-107">EXAMPLES</span></span>

### <span data-ttu-id="46079-108">Beispiel 1: Hinzufügen einer Netzwerkschnittstellenkonfiguration zum VMSS</span><span class="sxs-lookup"><span data-stu-id="46079-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="46079-109">Mit diesem Befehl wird der VMSS eine Netzwerkschnittstellenkonfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="46079-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="46079-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46079-110">PARAMETERS</span></span>

### <span data-ttu-id="46079-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46079-111">-DefaultProfile</span></span>
<span data-ttu-id="46079-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46079-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46079-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="46079-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="46079-114">Liste der DNS-Server-IP-Adressen für DNS-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="46079-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="46079-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="46079-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="46079-116">Gibt an, ob die Netzwerkschnittstelle beschleunigtes Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="46079-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="46079-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="46079-117">-EnableIPForwarding</span></span>
<span data-ttu-id="46079-118">Gibt an, ob die IP-Weiterleitung auf dieser NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="46079-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="46079-119">-ID</span><span class="sxs-lookup"><span data-stu-id="46079-119">-Id</span></span>
<span data-ttu-id="46079-120">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="46079-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="46079-121">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="46079-121">-IpConfiguration</span></span>
<span data-ttu-id="46079-122">Gibt die IP-Konfigurationen der Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="46079-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="46079-123">-Name</span><span class="sxs-lookup"><span data-stu-id="46079-123">-Name</span></span>
<span data-ttu-id="46079-124">Gibt den Namen der Netzwerkschnittstellenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="46079-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="46079-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="46079-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="46079-126">Die ID der Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="46079-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="46079-127">– Primär</span><span class="sxs-lookup"><span data-stu-id="46079-127">-Primary</span></span>
<span data-ttu-id="46079-128">Gibt an, ob aus der Netzwerkschnittstellenkonfiguration erstellte Netzwerkschnittstellen das primäre Netzwerk Informationscenter (NIC) des virtuellen Computers sein sollen.</span><span class="sxs-lookup"><span data-stu-id="46079-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="46079-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="46079-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="46079-130">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="46079-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="46079-131">Sie können das Cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="46079-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="46079-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46079-132">-Confirm</span></span>
<span data-ttu-id="46079-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46079-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46079-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46079-134">-WhatIf</span></span>
<span data-ttu-id="46079-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46079-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46079-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46079-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46079-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46079-137">CommonParameters</span></span>
<span data-ttu-id="46079-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46079-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46079-139">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46079-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46079-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46079-140">INPUTS</span></span>

### <span data-ttu-id="46079-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="46079-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="46079-142">System. String</span><span class="sxs-lookup"><span data-stu-id="46079-142">System.String</span></span>

### <span data-ttu-id="46079-143">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="46079-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="46079-144">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="46079-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="46079-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="46079-145">System.String[]</span></span>

## <span data-ttu-id="46079-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46079-146">OUTPUTS</span></span>

### <span data-ttu-id="46079-147">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="46079-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="46079-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="46079-148">NOTES</span></span>

## <span data-ttu-id="46079-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46079-149">RELATED LINKS</span></span>

[<span data-ttu-id="46079-150">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="46079-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
