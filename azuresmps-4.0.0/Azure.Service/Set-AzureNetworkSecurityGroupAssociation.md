---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 64639A35-0573-48C8-AB21-19FEB09537BA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b1b251a5fef3ad91f830e18714796421d2abca7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005964"
---
# <span data-ttu-id="51b1b-101">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="51b1b-101">Set-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="51b1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="51b1b-103">Ordnet eine Netzwerksicherheitsgruppe einem virtuellen Computer, einer PaaS-Rolle oder einem Netzwerkadapter zu.</span><span class="sxs-lookup"><span data-stu-id="51b1b-103">Associates a network security group to a virtual machine, PaaS role, or network adapter.</span></span>

## <span data-ttu-id="51b1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51b1b-104">SYNTAX</span></span>

### <span data-ttu-id="51b1b-105">AddNetworkSecurityGroupAssociationToSubnet</span><span class="sxs-lookup"><span data-stu-id="51b1b-105">AddNetworkSecurityGroupAssociationToSubnet</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VirtualNetworkName <String>
 -SubnetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="51b1b-106">AddNetworkSecurityGroupAssociationToIaaSRole</span><span class="sxs-lookup"><span data-stu-id="51b1b-106">AddNetworkSecurityGroupAssociationToIaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VM <PersistentVMRoleContext>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="51b1b-107">AddNetworkSecurityGroupAssociationToPaaSRole</span><span class="sxs-lookup"><span data-stu-id="51b1b-107">AddNetworkSecurityGroupAssociationToPaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] [-Slot <String>]
 -RoleName <String> -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="51b1b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51b1b-108">DESCRIPTION</span></span>
<span data-ttu-id="51b1b-109">Das Cmdlet " **Satz-AzureNetworkSecurityGroupAssociation** " ordnet eine Netzwerksicherheitsgruppe einem virtuellen Computer, einer Plattform als Dienst (PaaS) oder einem Netzwerkadapter zu.</span><span class="sxs-lookup"><span data-stu-id="51b1b-109">The **Set-AzureNetworkSecurityGroupAssociation** cmdlet associates a network security group to a virtual machine, platform as a service (PaaS) role, or network adapter.</span></span>

## <span data-ttu-id="51b1b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51b1b-110">EXAMPLES</span></span>

### <span data-ttu-id="51b1b-111">Beispiel 1: Zuweisen eines virtuellen Computers zu einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="51b1b-111">Example 1: Assign a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="51b1b-112">Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51b1b-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="51b1b-113">Das aktuelle Cmdlet weist dem virtuellen Computer die Netzwerksicherheitsgruppe mit dem Namen ContosoNetworkSecurityGroup zu.</span><span class="sxs-lookup"><span data-stu-id="51b1b-113">The current cmdlet assigns the network security group named ContosoNetworkSecurityGroup to that virtual machine.</span></span>

## <span data-ttu-id="51b1b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="51b1b-114">PARAMETERS</span></span>

### <span data-ttu-id="51b1b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="51b1b-115">-Force</span></span>
<span data-ttu-id="51b1b-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="51b1b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51b1b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="51b1b-117">-Name</span></span>
<span data-ttu-id="51b1b-118">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet festlegt.</span><span class="sxs-lookup"><span data-stu-id="51b1b-118">Specifies the name of the network security group that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b1b-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="51b1b-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="51b1b-120">Gibt den Namen des Netzwerkadapters an, auf den dieses Cmdlet die Netzwerksicherheitsgruppe anwendet.</span><span class="sxs-lookup"><span data-stu-id="51b1b-120">Specifies the name of the network adapter to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b1b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51b1b-121">-PassThru</span></span>
<span data-ttu-id="51b1b-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="51b1b-122">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="51b1b-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="51b1b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51b1b-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="51b1b-124">-Profile</span></span>
<span data-ttu-id="51b1b-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="51b1b-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="51b1b-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="51b1b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51b1b-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="51b1b-127">-RoleName</span></span>
<span data-ttu-id="51b1b-128">Gibt den Namen einer PaaS-Rolle an, auf die dieses Cmdlet die Netzwerksicherheitsgruppe anwendet.</span><span class="sxs-lookup"><span data-stu-id="51b1b-128">Specifies the name of a PaaS role to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b1b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="51b1b-129">-ServiceName</span></span>
<span data-ttu-id="51b1b-130">Gibt den Namen eines Cloud-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="51b1b-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="51b1b-131">Die PaaS-Rolle gehört zu dem Dienst, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="51b1b-131">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51b1b-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="51b1b-132">-Slot</span></span>
<span data-ttu-id="51b1b-133">Gibt einen PaaS-Steckplatz an.</span><span class="sxs-lookup"><span data-stu-id="51b1b-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="51b1b-134">Die PaaS-Rolle, für die dieses Cmdlet die Netzwerksicherheitsgruppe festlegt, weist den Slot auf, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="51b1b-134">The PaaS role for which this cmdlet sets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="51b1b-135">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="51b1b-135">Valid values are:</span></span> 

- <span data-ttu-id="51b1b-136">Produktions</span><span class="sxs-lookup"><span data-stu-id="51b1b-136">Production</span></span>
- <span data-ttu-id="51b1b-137">Inszenierung</span><span class="sxs-lookup"><span data-stu-id="51b1b-137">Staging</span></span> 

<span data-ttu-id="51b1b-138">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="51b1b-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b1b-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="51b1b-139">-SubnetName</span></span>
<span data-ttu-id="51b1b-140">Gibt den Namen eines Subnetzes an, dem dieses Cmdlet die Netzwerksicherheitsgruppe anordnet.</span><span class="sxs-lookup"><span data-stu-id="51b1b-140">Specifies the name of a subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b1b-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="51b1b-141">-VirtualNetworkName</span></span>
<span data-ttu-id="51b1b-142">Gibt den Namen eines virtuellen Netzwerks an, das das Subnetz enthält, dem dieses Cmdlet die Netzwerksicherheitsgruppe anordnet.</span><span class="sxs-lookup"><span data-stu-id="51b1b-142">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51b1b-143">-VM</span><span class="sxs-lookup"><span data-stu-id="51b1b-143">-VM</span></span>
<span data-ttu-id="51b1b-144">Gibt den virtuellen Computer an, auf den dieses Cmdlet die Netzwerksicherheitsgruppe anwendet.</span><span class="sxs-lookup"><span data-stu-id="51b1b-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51b1b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b1b-145">CommonParameters</span></span>
<span data-ttu-id="51b1b-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b1b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b1b-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51b1b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b1b-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51b1b-148">INPUTS</span></span>

## <span data-ttu-id="51b1b-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51b1b-149">OUTPUTS</span></span>

### <span data-ttu-id="51b1b-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51b1b-150">System.Boolean</span></span>

## <span data-ttu-id="51b1b-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="51b1b-151">NOTES</span></span>

## <span data-ttu-id="51b1b-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51b1b-152">RELATED LINKS</span></span>

[<span data-ttu-id="51b1b-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="51b1b-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="51b1b-154">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="51b1b-154">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)


