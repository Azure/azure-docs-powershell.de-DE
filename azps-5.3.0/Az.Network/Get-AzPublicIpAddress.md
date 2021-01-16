---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 7a369fafec712d23c7ac2aac30d3aa6928877355
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468139"
---
# <span data-ttu-id="b71ca-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b71ca-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="b71ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b71ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b71ca-103">Ruft eine öffentliche IP-Adresse ab.</span><span class="sxs-lookup"><span data-stu-id="b71ca-103">Gets a public IP address.</span></span>

## <span data-ttu-id="b71ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b71ca-104">SYNTAX</span></span>

### <span data-ttu-id="b71ca-105">NoExpandStandAloneIp (Standard)</span><span class="sxs-lookup"><span data-stu-id="b71ca-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b71ca-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="b71ca-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b71ca-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="b71ca-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b71ca-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="b71ca-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b71ca-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b71ca-109">DESCRIPTION</span></span>
<span data-ttu-id="b71ca-110">Das **Cmdlet "Get-AzPublicIPAddress"** ruft eine oder mehrere öffentliche IP-Adressen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b71ca-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="b71ca-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b71ca-111">EXAMPLES</span></span>

### <span data-ttu-id="b71ca-112">Beispiel 1: Erhalten einer öffentlichen IP-Ressource</span><span class="sxs-lookup"><span data-stu-id="b71ca-112">Example 1: Get a public IP resource</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic", 
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="b71ca-113">Dieser Befehl ruft eine öffentliche IP-Adressressource mit dem Namen "myPublicIp" in der Ressourcengruppe "myRg" ab.</span><span class="sxs-lookup"><span data-stu-id="b71ca-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="b71ca-114">Beispiel 2: Erhalten öffentlicher IP-Ressourcen mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="b71ca-114">Example 2: Get public IP resources using filtering</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="b71ca-115">Dieser Befehl ruft alle öffentlichen IP-Adressressourcen ab, deren Name mit "myPublicIp" beginnt.</span><span class="sxs-lookup"><span data-stu-id="b71ca-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="b71ca-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b71ca-116">PARAMETERS</span></span>

### <span data-ttu-id="b71ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71ca-117">-DefaultProfile</span></span>
<span data-ttu-id="b71ca-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b71ca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b71ca-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b71ca-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71ca-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b71ca-120">-IpConfigurationName</span></span>
<span data-ttu-id="b71ca-121">IP-Konfigurationsname der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b71ca-121">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71ca-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b71ca-122">-Name</span></span>
<span data-ttu-id="b71ca-123">Gibt den Namen der öffentlichen IP-Adresse an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b71ca-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b71ca-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b71ca-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="b71ca-125">Name der Virtual Machine Network Interface.</span><span class="sxs-lookup"><span data-stu-id="b71ca-125">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="b71ca-127">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b71ca-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b71ca-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="b71ca-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="b71ca-129">Virtual Machine Index.</span><span class="sxs-lookup"><span data-stu-id="b71ca-129">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71ca-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b71ca-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="b71ca-131">Name des virtuellen Skalierungssatzs.</span><span class="sxs-lookup"><span data-stu-id="b71ca-131">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b71ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71ca-132">CommonParameters</span></span>
<span data-ttu-id="b71ca-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b71ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71ca-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b71ca-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71ca-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b71ca-135">INPUTS</span></span>

### <span data-ttu-id="b71ca-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b71ca-136">System.String</span></span>

## <span data-ttu-id="b71ca-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b71ca-137">OUTPUTS</span></span>

### <span data-ttu-id="b71ca-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b71ca-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b71ca-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b71ca-139">NOTES</span></span>

## <span data-ttu-id="b71ca-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b71ca-140">RELATED LINKS</span></span>

[<span data-ttu-id="b71ca-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b71ca-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="b71ca-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b71ca-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="b71ca-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b71ca-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


