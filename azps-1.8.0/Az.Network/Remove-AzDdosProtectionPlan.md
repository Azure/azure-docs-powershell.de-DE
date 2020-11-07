---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: b8ce7dac361124129b3261d8ba368852726812ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660394"
---
# <span data-ttu-id="ed8e2-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="ed8e2-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="ed8e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8e2-103">Entfernt einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="ed8e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed8e2-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed8e2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed8e2-105">DESCRIPTION</span></span>
<span data-ttu-id="ed8e2-106">Das Remove-AzDdosProtectionPlan-Cmdlet entfernt einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="ed8e2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed8e2-107">EXAMPLES</span></span>

### <span data-ttu-id="ed8e2-108">Beispiel 1: Entfernen eines leeren DDoS-Schutzplans</span><span class="sxs-lookup"><span data-stu-id="ed8e2-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="ed8e2-109">In diesem Fall entfernen wir einen DDoS-Schutzplan wie angegeben.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="ed8e2-110">Beispiel 2: Entfernen eines mit einem virtuellen Netzwerk verknüpften DDoS-Schutzplans</span><span class="sxs-lookup"><span data-stu-id="ed8e2-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
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

<span data-ttu-id="ed8e2-111">DDoS-schutzpläne können nicht gelöscht werden, wenn Sie einem virtuellen Netzwerk zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="ed8e2-112">Im ersten Schritt wird also die Zuordnung beider Objekte aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="ed8e2-113">Hier erhalten wir die aktuellste Version des virtuellen Netzwerks, das dem Plan zugeordnet ist, und wir setzen die Eigenschaft **DdosProtectionPlan** auf einen leeren Wert und das Flag **EnableDdosProtection** (dieses Flag kann ohne einen Plan nicht wahr sein).</span><span class="sxs-lookup"><span data-stu-id="ed8e2-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="ed8e2-114">Anschließend wird der neue Zustand beibehalten, indem die lokale Variable in **AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="ed8e2-115">An diesem Punkt ist der Plan nicht mehr dem virtuellen Netzwerk zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="ed8e2-116">Wenn dies der letzte mit dem Plan verknüpfte ist, können wir den DDoS-Schutzplan mithilfe des Befehls Remove-AzDdosProtectionPlan entfernen.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="ed8e2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed8e2-117">PARAMETERS</span></span>

### <span data-ttu-id="ed8e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8e2-118">-DefaultProfile</span></span>
<span data-ttu-id="ed8e2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed8e2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ed8e2-120">-Name</span></span>
<span data-ttu-id="ed8e2-121">Gibt den Namen des DDoS-Schutzplans an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="ed8e2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed8e2-122">-PassThru</span></span>
<span data-ttu-id="ed8e2-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed8e2-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed8e2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8e2-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed8e2-126">Gibt die Ressourcengruppe des DDoS-Schutzplans an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="ed8e2-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed8e2-127">-Confirm</span></span>
<span data-ttu-id="ed8e2-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed8e2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed8e2-129">-WhatIf</span></span>
<span data-ttu-id="ed8e2-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed8e2-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed8e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8e2-132">CommonParameters</span></span>
<span data-ttu-id="ed8e2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8e2-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8e2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8e2-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed8e2-135">INPUTS</span></span>

### <span data-ttu-id="ed8e2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ed8e2-136">System.String</span></span>

## <span data-ttu-id="ed8e2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed8e2-137">OUTPUTS</span></span>

### <span data-ttu-id="ed8e2-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed8e2-138">System.Boolean</span></span>

## <span data-ttu-id="ed8e2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed8e2-139">NOTES</span></span>

## <span data-ttu-id="ed8e2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed8e2-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed8e2-141">Neu – AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="ed8e2-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="ed8e2-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="ed8e2-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="ed8e2-143">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed8e2-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="ed8e2-144">Satz-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed8e2-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="ed8e2-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed8e2-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)