---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006358"
---
# <span data-ttu-id="9b7d4-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="9b7d4-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="9b7d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="9b7d4-103">Entfernt eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-103">Removes a network security group.</span></span>

## <span data-ttu-id="9b7d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b7d4-104">SYNTAX</span></span>

### <span data-ttu-id="9b7d4-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="9b7d4-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9b7d4-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="9b7d4-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9b7d4-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="9b7d4-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b7d4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b7d4-108">DESCRIPTION</span></span>
<span data-ttu-id="9b7d4-109">Das Cmdlet " **Remove-AzureNetworkSecurityGroupAssociation** " entfernt eine Netzwerksicherheitsgruppe von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="9b7d4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b7d4-110">EXAMPLES</span></span>

### <span data-ttu-id="9b7d4-111">Beispiel 1: Entfernen eines virtuellen Computers zu einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="9b7d4-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="9b7d4-112">Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="9b7d4-113">Das aktuelle Cmdlet entfernt die Netzwerksicherheitsgruppe namens ContosoNetworkSecurityGroup von diesem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="9b7d4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b7d4-114">PARAMETERS</span></span>

### <span data-ttu-id="9b7d4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9b7d4-115">-Force</span></span>
<span data-ttu-id="9b7d4-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9b7d4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9b7d4-117">-Name</span></span>
<span data-ttu-id="9b7d4-118">Gibt den Namen der Netzwerksicherheitsgruppe an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7d4-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="9b7d4-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="9b7d4-120">Gibt den Namen des Netzwerkadapters an, von dem dieses Cmdlet die Netzwerksicherheitsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7d4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b7d4-121">-PassThru</span></span>
<span data-ttu-id="9b7d4-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9b7d4-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9b7d4-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="9b7d4-124">-Profile</span></span>
<span data-ttu-id="9b7d4-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b7d4-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7d4-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="9b7d4-127">-RoleName</span></span>
<span data-ttu-id="9b7d4-128">Gibt den Namen einer PaaS-Rolle an, aus der dieses Cmdlet die Netzwerksicherheitsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7d4-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9b7d4-129">-ServiceName</span></span>
<span data-ttu-id="9b7d4-130">Gibt den Namen eines Cloud-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="9b7d4-131">Die PaaS-Rolle, aus der dieses Cmdlet eine Netzwerksicherheitsgruppe entfernt, gehört zu dem Dienst, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7d4-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="9b7d4-132">-Slot</span></span>
<span data-ttu-id="9b7d4-133">Gibt einen PaaS-Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="9b7d4-134">Die PaaS-Rolle, aus der dieses Cmdlet eine Netzwerksicherheitsgruppe entfernt, verfügt über den Slot, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="9b7d4-135">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9b7d4-135">Valid values are:</span></span>

- <span data-ttu-id="9b7d4-136">Produktions</span><span class="sxs-lookup"><span data-stu-id="9b7d4-136">Production</span></span>
- <span data-ttu-id="9b7d4-137">Inszenierung</span><span class="sxs-lookup"><span data-stu-id="9b7d4-137">Staging</span></span>

<span data-ttu-id="9b7d4-138">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7d4-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="9b7d4-139">-SubnetName</span></span>
<span data-ttu-id="9b7d4-140">Gibt den Namen eines Subnets an, aus dem dieses Cmdlet die Netzwerksicherheitsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7d4-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="9b7d4-141">-VirtualNetworkName</span></span>
<span data-ttu-id="9b7d4-142">Gibt den Namen eines virtuellen Netzwerks an, das das Subnetz enthält, aus dem dieses Cmdlet die Netzwerksicherheitsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b7d4-143">-VM</span><span class="sxs-lookup"><span data-stu-id="9b7d4-143">-VM</span></span>
<span data-ttu-id="9b7d4-144">Gibt den virtuellen Computer an, auf den dieses Cmdlet die Netzwerksicherheitsgruppe anwendet.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b7d4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b7d4-145">CommonParameters</span></span>
<span data-ttu-id="9b7d4-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b7d4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b7d4-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b7d4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b7d4-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b7d4-148">INPUTS</span></span>

## <span data-ttu-id="9b7d4-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b7d4-149">OUTPUTS</span></span>

### <span data-ttu-id="9b7d4-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b7d4-150">System.Boolean</span></span>

## <span data-ttu-id="9b7d4-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b7d4-151">NOTES</span></span>

## <span data-ttu-id="9b7d4-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b7d4-152">RELATED LINKS</span></span>

[<span data-ttu-id="9b7d4-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="9b7d4-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="9b7d4-154">Satz-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="9b7d4-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)
