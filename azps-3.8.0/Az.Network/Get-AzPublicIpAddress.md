---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: dbcd9d67587e1a7e968dedf664a053c1c64dbb46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003506"
---
# <span data-ttu-id="c2b95-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2b95-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="c2b95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2b95-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b95-103">Ruft eine öffentliche IP-Adresse ab.</span><span class="sxs-lookup"><span data-stu-id="c2b95-103">Gets a public IP address.</span></span>

## <span data-ttu-id="c2b95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2b95-104">SYNTAX</span></span>

### <span data-ttu-id="c2b95-105">NoExpandStandAloneIp (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2b95-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2b95-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="c2b95-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2b95-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="c2b95-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2b95-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="c2b95-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2b95-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2b95-109">DESCRIPTION</span></span>
<span data-ttu-id="c2b95-110">Das Cmdlet " **Get-AzPublicIPAddress** " ruft mindestens eine öffentliche IP-Adresse in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="c2b95-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="c2b95-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2b95-111">EXAMPLES</span></span>

### <span data-ttu-id="c2b95-112">1: Abrufen einer öffentlichen IP-Ressource</span><span class="sxs-lookup"><span data-stu-id="c2b95-112">1: Get a public IP resource</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="c2b95-113">Dieser Befehl ruft eine öffentliche IP-Adressen Ressource mit dem Namen myPublicIp in der Ressourcengruppe myRg.</span><span class="sxs-lookup"><span data-stu-id="c2b95-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="c2b95-114">2: Abrufen öffentlicher IP-Ressourcen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="c2b95-114">2: Get public IP resources using filtering</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="c2b95-115">Dieser Befehl ruft alle öffentlichen IP-Adressen Ressourcen ab, deren Name mit myPublicIp beginnt.</span><span class="sxs-lookup"><span data-stu-id="c2b95-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="c2b95-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2b95-116">PARAMETERS</span></span>

### <span data-ttu-id="c2b95-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b95-117">-DefaultProfile</span></span>
<span data-ttu-id="c2b95-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2b95-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2b95-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c2b95-119">-ExpandResource</span></span>
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

### <span data-ttu-id="c2b95-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c2b95-120">-IpConfigurationName</span></span>
<span data-ttu-id="c2b95-121">IP-Konfigurations Name der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c2b95-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="c2b95-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c2b95-122">-Name</span></span>
<span data-ttu-id="c2b95-123">Gibt den Namen der öffentlichen IP-Adresse an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c2b95-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c2b95-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="c2b95-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="c2b95-125">Name der Netzwerkschnittstelle der virtuellen Maschine</span><span class="sxs-lookup"><span data-stu-id="c2b95-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="c2b95-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b95-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2b95-127">Gibt den Namen der Ressourcengruppe an, die die öffentliche IP-Adresse enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c2b95-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c2b95-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="c2b95-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="c2b95-129">Virtueller Computer-Index.</span><span class="sxs-lookup"><span data-stu-id="c2b95-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="c2b95-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c2b95-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="c2b95-131">Name des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="c2b95-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="c2b95-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b95-132">CommonParameters</span></span>
<span data-ttu-id="c2b95-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b95-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b95-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2b95-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b95-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2b95-135">INPUTS</span></span>

### <span data-ttu-id="c2b95-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b95-136">System.String</span></span>

## <span data-ttu-id="c2b95-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2b95-137">OUTPUTS</span></span>

### <span data-ttu-id="c2b95-138">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2b95-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="c2b95-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2b95-139">NOTES</span></span>

## <span data-ttu-id="c2b95-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2b95-140">RELATED LINKS</span></span>

[<span data-ttu-id="c2b95-141">Neu – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2b95-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="c2b95-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2b95-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="c2b95-143">Satz-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2b95-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


