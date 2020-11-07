---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: cda87de466ba3cf3c2a1f73798a2bed21f48206e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849407"
---
# <span data-ttu-id="192ea-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="192ea-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="192ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="192ea-102">SYNOPSIS</span></span>
<span data-ttu-id="192ea-103">Fügt der VMSS eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="192ea-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="192ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="192ea-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="192ea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="192ea-105">DESCRIPTION</span></span>
<span data-ttu-id="192ea-106">Das **Add-AzureRmVmssNetworkInterfaceConfiguration-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="192ea-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="192ea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="192ea-107">EXAMPLES</span></span>

### <span data-ttu-id="192ea-108">Beispiel 1: Hinzufügen einer Netzwerkschnittstellenkonfiguration zum VMSS</span><span class="sxs-lookup"><span data-stu-id="192ea-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="192ea-109">Mit diesem Befehl wird der VMSS eine Netzwerkschnittstellenkonfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="192ea-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="192ea-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="192ea-110">PARAMETERS</span></span>

### <span data-ttu-id="192ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192ea-111">-DefaultProfile</span></span>
<span data-ttu-id="192ea-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="192ea-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="192ea-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="192ea-114">Liste der DNS-Server-IP-Adressen für DNS-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="192ea-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="192ea-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="192ea-116">Gibt an, ob die Netzwerkschnittstelle beschleunigtes Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="192ea-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="192ea-117">-EnableIPForwarding</span></span>
<span data-ttu-id="192ea-118">Gibt an, ob die IP-Weiterleitung auf dieser NIC aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="192ea-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-119">-ID</span><span class="sxs-lookup"><span data-stu-id="192ea-119">-Id</span></span>
<span data-ttu-id="192ea-120">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="192ea-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-121">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="192ea-121">-IpConfiguration</span></span>
<span data-ttu-id="192ea-122">Gibt die IP-Konfigurationen der Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="192ea-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-123">-Name</span><span class="sxs-lookup"><span data-stu-id="192ea-123">-Name</span></span>
<span data-ttu-id="192ea-124">Gibt den Namen der Netzwerkschnittstellenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="192ea-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="192ea-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="192ea-126">Die ID der Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="192ea-126">Id of the network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-127">– Primär</span><span class="sxs-lookup"><span data-stu-id="192ea-127">-Primary</span></span>
<span data-ttu-id="192ea-128">Gibt an, ob aus der Netzwerkschnittstellenkonfiguration erstellte Netzwerkschnittstellen das primäre Netzwerk Informationscenter (NIC) des virtuellen Computers sein sollen.</span><span class="sxs-lookup"><span data-stu-id="192ea-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="192ea-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="192ea-130">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="192ea-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="192ea-131">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="192ea-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="192ea-132">-Confirm</span></span>
<span data-ttu-id="192ea-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="192ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="192ea-134">-WhatIf</span></span>
<span data-ttu-id="192ea-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="192ea-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="192ea-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="192ea-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="192ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192ea-137">CommonParameters</span></span>
<span data-ttu-id="192ea-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="192ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192ea-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="192ea-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192ea-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="192ea-140">INPUTS</span></span>

### <span data-ttu-id="192ea-141">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="192ea-141">VirtualMachineScaleSet</span></span>
<span data-ttu-id="192ea-142">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="192ea-142">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="192ea-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="192ea-143">OUTPUTS</span></span>

###  
<span data-ttu-id="192ea-144">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="192ea-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="192ea-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="192ea-145">NOTES</span></span>

## <span data-ttu-id="192ea-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="192ea-146">RELATED LINKS</span></span>

[<span data-ttu-id="192ea-147">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="192ea-147">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
