---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006788"
---
# <span data-ttu-id="b6779-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b6779-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="b6779-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6779-102">SYNOPSIS</span></span>
<span data-ttu-id="b6779-103">Ruft eine Netzwerksicherheitsgruppe für einen virtuellen Computer, einen Netzwerkadapter oder eine PaaS-Rolle ab.</span><span class="sxs-lookup"><span data-stu-id="b6779-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="b6779-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6779-104">SYNTAX</span></span>

### <span data-ttu-id="b6779-105">GetNetworkSecurityGroupAssociationForSubnet</span><span class="sxs-lookup"><span data-stu-id="b6779-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b6779-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="b6779-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b6779-107">GetNetworkSecurityGroupAssociationForPaaSRole</span><span class="sxs-lookup"><span data-stu-id="b6779-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6779-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6779-108">DESCRIPTION</span></span>
<span data-ttu-id="b6779-109">Das Cmdlet " **Get-AzureNetworkSecurityGroupAssociation** " Ruft die Netzwerksicherheitsgruppe für einen virtuellen Computer, einen Netzwerkadapter oder eine Plattform als Dienst Rolle (PaaS) ab.</span><span class="sxs-lookup"><span data-stu-id="b6779-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="b6779-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6779-110">EXAMPLES</span></span>

### <span data-ttu-id="b6779-111">Beispiel 1: Abrufen der Netzwerksicherheitsgruppe für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="b6779-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="b6779-112">Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6779-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="b6779-113">Das aktuelle Cmdlet ruft die dem virtuellen Computer zugeordnete Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b6779-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="b6779-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6779-114">PARAMETERS</span></span>

### <span data-ttu-id="b6779-115">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="b6779-115">-Detailed</span></span>
<span data-ttu-id="b6779-116">Gibt an, dass dieses Cmdlet Details der Netzwerksicherheitsgruppe zurückgibt, die dem virtuellen Computer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b6779-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="b6779-117">Diese Details umfassen Standort und Regeln.</span><span class="sxs-lookup"><span data-stu-id="b6779-117">These details include location and rules.</span></span>

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

### <span data-ttu-id="b6779-118">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b6779-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="b6779-119">Gibt den Namen des Netzwerkadapters an, für den dieses Cmdlet die Netzwerksicherheitsgruppe abruft.</span><span class="sxs-lookup"><span data-stu-id="b6779-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6779-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="b6779-120">-Profile</span></span>
<span data-ttu-id="b6779-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b6779-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b6779-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b6779-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6779-123">-RoleName</span><span class="sxs-lookup"><span data-stu-id="b6779-123">-RoleName</span></span>
<span data-ttu-id="b6779-124">Gibt den Namen einer PaaS-Rolle an, für die dieses Cmdlet die Netzwerksicherheitsgruppe abruft.</span><span class="sxs-lookup"><span data-stu-id="b6779-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6779-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b6779-125">-ServiceName</span></span>
<span data-ttu-id="b6779-126">Gibt den Namen eines Cloud-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="b6779-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="b6779-127">Die PaaS-Rolle gehört zu dem Dienst, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b6779-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6779-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="b6779-128">-Slot</span></span>
<span data-ttu-id="b6779-129">Gibt einen PaaS-Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="b6779-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="b6779-130">Die PaaS-Rolle, für die dieses Cmdlet die Netzwerksicherheitsgruppe erhält, hat den Slot, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b6779-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="b6779-131">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b6779-131">Valid values are:</span></span> 

- <span data-ttu-id="b6779-132">Produktions</span><span class="sxs-lookup"><span data-stu-id="b6779-132">Production</span></span>
- <span data-ttu-id="b6779-133">Inszenierung</span><span class="sxs-lookup"><span data-stu-id="b6779-133">Staging</span></span> 

<span data-ttu-id="b6779-134">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="b6779-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6779-135">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b6779-135">-SubnetName</span></span>
<span data-ttu-id="b6779-136">Gibt den Namen eines Subnets an, für das dieses Cmdlet die Netzwerksicherheitsgruppe abruft.</span><span class="sxs-lookup"><span data-stu-id="b6779-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6779-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b6779-137">-VirtualNetworkName</span></span>
<span data-ttu-id="b6779-138">Gibt den Namen eines virtuellen Netzwerks an, das das Subnetz enthält, für das dieses Cmdlet die Netzwerksicherheitsgruppe abruft.</span><span class="sxs-lookup"><span data-stu-id="b6779-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6779-139">-VM</span><span class="sxs-lookup"><span data-stu-id="b6779-139">-VM</span></span>
<span data-ttu-id="b6779-140">Gibt den virtuellen Computer an, auf den dieses Cmdlet die Netzwerksicherheitsgruppe anwendet.</span><span class="sxs-lookup"><span data-stu-id="b6779-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6779-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6779-141">CommonParameters</span></span>
<span data-ttu-id="b6779-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6779-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6779-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6779-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6779-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6779-144">INPUTS</span></span>

## <span data-ttu-id="b6779-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6779-145">OUTPUTS</span></span>

### <span data-ttu-id="b6779-146">Microsoft. WindowsAzure. Commands. Servicemanagement. Network. NetworkSecurityGroup. Model. INetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b6779-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="b6779-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6779-147">NOTES</span></span>

## <span data-ttu-id="b6779-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6779-148">RELATED LINKS</span></span>

[<span data-ttu-id="b6779-149">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b6779-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="b6779-150">Satz-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b6779-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


