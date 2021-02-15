---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: c565c78e7f95e02d3449a04f0a53f4b84ef7a9f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172556"
---
# <span data-ttu-id="835c6-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="835c6-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="835c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="835c6-102">SYNOPSIS</span></span>
<span data-ttu-id="835c6-103">Entfernt einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="835c6-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="835c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="835c6-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="835c6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="835c6-105">DESCRIPTION</span></span>
<span data-ttu-id="835c6-106">Das Remove-AzDdosProtectionPlan entfernt einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="835c6-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="835c6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="835c6-107">EXAMPLES</span></span>

### <span data-ttu-id="835c6-108">Beispiel 1: Entfernen eines leeren DDoS-Schutzplans</span><span class="sxs-lookup"><span data-stu-id="835c6-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="835c6-109">In diesem Fall entfernen wir wie angegeben einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="835c6-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="835c6-110">Beispiel 2: Entfernen eines DDoS-Schutzplans, der einem virtuellen Netzwerk zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="835c6-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="835c6-111">DDoS-Schutzpläne können nicht gelöscht werden, wenn sie einem virtuellen Netzwerk zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="835c6-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="835c6-112">Der erste Schritt besteht also im Entfernen der Zuordnung beider Objekte.</span><span class="sxs-lookup"><span data-stu-id="835c6-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="835c6-113">Hier erhalten wir die neueste Version des virtuellen Netzwerks, das dem Plan zugeordnet ist, und wir legen die Eigenschaft **"DdosProtectionPlan"** auf einen leeren Wert und das Kennzeichen **"EnableDdosProtection"** (dieses Kennzeichen kann ohne einen Plan nicht wahr sein) ab.</span><span class="sxs-lookup"><span data-stu-id="835c6-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="835c6-114">Anschließend speichern wir den neuen Zustand, indem wir die lokale Variable in **Set-AzVirtualNetwork verwenden.**</span><span class="sxs-lookup"><span data-stu-id="835c6-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="835c6-115">An diesem Punkt ist der Plan nicht mehr mit dem virtuellen Netzwerk verknüpft.</span><span class="sxs-lookup"><span data-stu-id="835c6-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="835c6-116">Wenn dies der letzte ist, der dem Plan zugeordnet ist, können Sie den DDoS-Schutzplan mithilfe des Befehls "Remove-AzDdosProtectionPlan" entfernen.</span><span class="sxs-lookup"><span data-stu-id="835c6-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="835c6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="835c6-117">PARAMETERS</span></span>

### <span data-ttu-id="835c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="835c6-118">-DefaultProfile</span></span>
<span data-ttu-id="835c6-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="835c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="835c6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="835c6-120">-Name</span></span>
<span data-ttu-id="835c6-121">Gibt den Namen des DDoS-Schutzplans an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="835c6-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="835c6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="835c6-122">-PassThru</span></span>
<span data-ttu-id="835c6-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="835c6-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="835c6-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="835c6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="835c6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="835c6-125">-ResourceGroupName</span></span>
<span data-ttu-id="835c6-126">Gibt die Ressourcengruppe des DDoS-Schutzplans an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="835c6-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="835c6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="835c6-127">-Confirm</span></span>
<span data-ttu-id="835c6-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="835c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="835c6-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="835c6-129">-WhatIf</span></span>
<span data-ttu-id="835c6-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="835c6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="835c6-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="835c6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="835c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="835c6-132">CommonParameters</span></span>
<span data-ttu-id="835c6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="835c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="835c6-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="835c6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="835c6-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="835c6-135">INPUTS</span></span>

### <span data-ttu-id="835c6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="835c6-136">System.String</span></span>

## <span data-ttu-id="835c6-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="835c6-137">OUTPUTS</span></span>

### <span data-ttu-id="835c6-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="835c6-138">System.Boolean</span></span>

## <span data-ttu-id="835c6-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="835c6-139">NOTES</span></span>

## <span data-ttu-id="835c6-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="835c6-140">RELATED LINKS</span></span>

[<span data-ttu-id="835c6-141">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="835c6-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="835c6-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="835c6-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="835c6-143">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="835c6-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="835c6-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="835c6-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="835c6-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="835c6-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)