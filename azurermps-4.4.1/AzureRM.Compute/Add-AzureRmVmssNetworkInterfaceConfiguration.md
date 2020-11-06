---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 651e339de5782d288350535ba1b0527d7a3eb0de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499197"
---
# <span data-ttu-id="df1be-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="df1be-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="df1be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df1be-102">SYNOPSIS</span></span>
<span data-ttu-id="df1be-103">Fügt der VMSS eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="df1be-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df1be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df1be-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df1be-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df1be-105">DESCRIPTION</span></span>
<span data-ttu-id="df1be-106">Das **Add-AzureRmVmssNetworkInterfaceConfiguration-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) eine Netzwerkschnittstellenkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="df1be-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="df1be-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df1be-107">EXAMPLES</span></span>

### <span data-ttu-id="df1be-108">Beispiel 1: Hinzufügen einer Netzwerkschnittstellenkonfiguration zum VMSS</span><span class="sxs-lookup"><span data-stu-id="df1be-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="df1be-109">Mit diesem Befehl wird der VMSS eine Netzwerkschnittstellenkonfiguration hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="df1be-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="df1be-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="df1be-110">PARAMETERS</span></span>

### <span data-ttu-id="df1be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1be-111">-DefaultProfile</span></span>
<span data-ttu-id="df1be-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df1be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df1be-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="df1be-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="df1be-114">Liste der DNS-Server-IP-Adressen für DNS-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="df1be-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="df1be-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="df1be-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="df1be-116">Gibt an, ob die Netzwerkschnittstelle beschleunigtes Netzwerk aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="df1be-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df1be-117">-ID</span><span class="sxs-lookup"><span data-stu-id="df1be-117">-Id</span></span>
<span data-ttu-id="df1be-118">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="df1be-118">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="df1be-119">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="df1be-119">-IpConfiguration</span></span>
<span data-ttu-id="df1be-120">Gibt die IP-Konfigurationen der Netzwerkschnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="df1be-120">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="df1be-121">-Name</span><span class="sxs-lookup"><span data-stu-id="df1be-121">-Name</span></span>
<span data-ttu-id="df1be-122">Gibt den Namen der Netzwerkschnittstellenkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="df1be-122">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="df1be-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="df1be-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="df1be-124">Die ID der Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="df1be-124">Id of the network security group.</span></span>

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

### <span data-ttu-id="df1be-125">– Primär</span><span class="sxs-lookup"><span data-stu-id="df1be-125">-Primary</span></span>
<span data-ttu-id="df1be-126">Gibt an, ob aus der Netzwerkschnittstellenkonfiguration erstellte Netzwerkschnittstellen das primäre Netzwerk Informationscenter (NIC) des virtuellen Computers sein sollen.</span><span class="sxs-lookup"><span data-stu-id="df1be-126">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="df1be-127">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="df1be-127">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="df1be-128">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="df1be-128">Specifies the VMSS object.</span></span>
<span data-ttu-id="df1be-129">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df1be-129">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="df1be-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df1be-130">-Confirm</span></span>
<span data-ttu-id="df1be-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df1be-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df1be-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df1be-132">-WhatIf</span></span>
<span data-ttu-id="df1be-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df1be-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df1be-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df1be-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df1be-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1be-135">CommonParameters</span></span>
<span data-ttu-id="df1be-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1be-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1be-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1be-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1be-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df1be-138">INPUTS</span></span>

## <span data-ttu-id="df1be-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df1be-139">OUTPUTS</span></span>

###  
<span data-ttu-id="df1be-140">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="df1be-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="df1be-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="df1be-141">NOTES</span></span>

## <span data-ttu-id="df1be-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df1be-142">RELATED LINKS</span></span>

[<span data-ttu-id="df1be-143">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="df1be-143">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
