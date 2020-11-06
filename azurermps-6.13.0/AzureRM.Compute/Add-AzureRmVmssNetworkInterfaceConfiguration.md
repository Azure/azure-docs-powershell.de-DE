---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 6789b2a0f3309e8011cc6e87a27dbf9f28579d05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496342"
---
# <span data-ttu-id="05d19-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="05d19-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="05d19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05d19-102">SYNOPSIS</span></span>
<span data-ttu-id="05d19-103">Fügt der VMSS eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="05d19-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05d19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05d19-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05d19-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05d19-105">DESCRIPTION</span></span>
<span data-ttu-id="05d19-106">Das **Add-AzureRmVmssNetworkInterfaceConfiguration-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="05d19-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="05d19-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05d19-107">EXAMPLES</span></span>

### <span data-ttu-id="05d19-108">Beispiel 1: Hinzufügen einer Netzwerkschnittstellenkonfiguration zum VMSS</span><span class="sxs-lookup"><span data-stu-id="05d19-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="05d19-109">Mit diesem Befehl wird der VMSS eine Netzwerkschnittstellenkonfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="05d19-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="05d19-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="05d19-110">PARAMETERS</span></span>

### <span data-ttu-id="05d19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d19-111">-DefaultProfile</span></span>
<span data-ttu-id="05d19-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05d19-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05d19-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="05d19-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="05d19-114">Liste der DNS-Server-IP-Adressen für DNS-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="05d19-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="05d19-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="05d19-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="05d19-116">Gibt an, ob die Netzwerkschnittstelle beschleunigtes Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="05d19-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="05d19-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="05d19-117">-EnableIPForwarding</span></span>
<span data-ttu-id="05d19-118">Gibt an, ob die IP-Weiterleitung auf dieser NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="05d19-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="05d19-119">-ID</span><span class="sxs-lookup"><span data-stu-id="05d19-119">-Id</span></span>
<span data-ttu-id="05d19-120">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="05d19-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="05d19-121">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="05d19-121">-IpConfiguration</span></span>
<span data-ttu-id="05d19-122">Gibt die IP-Konfigurationen der Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="05d19-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="05d19-123">-Name</span><span class="sxs-lookup"><span data-stu-id="05d19-123">-Name</span></span>
<span data-ttu-id="05d19-124">Gibt den Namen der Netzwerkschnittstellenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="05d19-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="05d19-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="05d19-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="05d19-126">Die ID der Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="05d19-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="05d19-127">– Primär</span><span class="sxs-lookup"><span data-stu-id="05d19-127">-Primary</span></span>
<span data-ttu-id="05d19-128">Gibt an, ob aus der Netzwerkschnittstellenkonfiguration erstellte Netzwerkschnittstellen das primäre Netzwerk Informationscenter (NIC) des virtuellen Computers sein sollen.</span><span class="sxs-lookup"><span data-stu-id="05d19-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="05d19-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="05d19-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="05d19-130">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="05d19-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="05d19-131">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="05d19-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="05d19-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05d19-132">-Confirm</span></span>
<span data-ttu-id="05d19-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05d19-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05d19-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05d19-134">-WhatIf</span></span>
<span data-ttu-id="05d19-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05d19-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05d19-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05d19-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05d19-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d19-137">CommonParameters</span></span>
<span data-ttu-id="05d19-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d19-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d19-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d19-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d19-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05d19-140">INPUTS</span></span>

### <span data-ttu-id="05d19-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="05d19-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="05d19-142">System. String</span><span class="sxs-lookup"><span data-stu-id="05d19-142">System.String</span></span>

### <span data-ttu-id="05d19-143">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="05d19-143">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="05d19-144">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="05d19-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="05d19-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="05d19-145">System.String[]</span></span>

## <span data-ttu-id="05d19-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05d19-146">OUTPUTS</span></span>

### <span data-ttu-id="05d19-147">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="05d19-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="05d19-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="05d19-148">NOTES</span></span>

## <span data-ttu-id="05d19-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05d19-149">RELATED LINKS</span></span>

[<span data-ttu-id="05d19-150">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="05d19-150">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
