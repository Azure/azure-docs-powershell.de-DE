---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662243"
---
# <span data-ttu-id="192c7-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="192c7-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="192c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="192c7-102">SYNOPSIS</span></span>
<span data-ttu-id="192c7-103">Fügt der VMSS eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="192c7-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="192c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="192c7-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="192c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="192c7-105">DESCRIPTION</span></span>
<span data-ttu-id="192c7-106">Das **Add-AzureRmVmssNetworkInterfaceConfiguration-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="192c7-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="192c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="192c7-107">EXAMPLES</span></span>

### <span data-ttu-id="192c7-108">Beispiel 1: Hinzufügen einer Netzwerkschnittstellenkonfiguration zum VMSS</span><span class="sxs-lookup"><span data-stu-id="192c7-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="192c7-109">Mit diesem Befehl wird der VMSS eine Netzwerkschnittstellenkonfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="192c7-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="192c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="192c7-110">PARAMETERS</span></span>

### <span data-ttu-id="192c7-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="192c7-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="192c7-112">Liste der DNS-Server-IP-Adressen für DNS-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="192c7-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="192c7-113">-ID</span><span class="sxs-lookup"><span data-stu-id="192c7-113">-Id</span></span>
<span data-ttu-id="192c7-114">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="192c7-114">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="192c7-115">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="192c7-115">-IpConfiguration</span></span>
<span data-ttu-id="192c7-116">Gibt die IP-Konfigurationen der Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="192c7-116">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="192c7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="192c7-117">-Name</span></span>
<span data-ttu-id="192c7-118">Gibt den Namen der Netzwerkschnittstellenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="192c7-118">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="192c7-119">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="192c7-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="192c7-120">Die ID der Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="192c7-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="192c7-121">– Primär</span><span class="sxs-lookup"><span data-stu-id="192c7-121">-Primary</span></span>
<span data-ttu-id="192c7-122">Gibt an, ob aus der Netzwerkschnittstellenkonfiguration erstellte Netzwerkschnittstellen das primäre Netzwerk Informationscenter (NIC) des virtuellen Computers sein sollen.</span><span class="sxs-lookup"><span data-stu-id="192c7-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="192c7-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="192c7-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="192c7-124">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="192c7-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="192c7-125">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="192c7-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="192c7-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="192c7-126">-Confirm</span></span>
<span data-ttu-id="192c7-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="192c7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="192c7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="192c7-128">-WhatIf</span></span>
<span data-ttu-id="192c7-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="192c7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="192c7-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="192c7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="192c7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192c7-131">CommonParameters</span></span>
<span data-ttu-id="192c7-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="192c7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192c7-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="192c7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192c7-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="192c7-134">INPUTS</span></span>

### <span data-ttu-id="192c7-135">Keine</span><span class="sxs-lookup"><span data-stu-id="192c7-135">None</span></span>
<span data-ttu-id="192c7-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="192c7-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="192c7-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="192c7-137">OUTPUTS</span></span>

###  
<span data-ttu-id="192c7-138">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="192c7-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="192c7-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="192c7-139">NOTES</span></span>

## <span data-ttu-id="192c7-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="192c7-140">RELATED LINKS</span></span>

[<span data-ttu-id="192c7-141">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="192c7-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
