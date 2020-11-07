---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 626e2fbfdbe4b305772817a2f9b11f0e14fd90f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821632"
---
# <span data-ttu-id="f1ad1-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f1ad1-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="f1ad1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ad1-103">Erstellt einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="f1ad1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1ad1-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1ad1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1ad1-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ad1-106">Das New-AzDdosProtectionPlan-Cmdlet erstellt einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="f1ad1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1ad1-107">EXAMPLES</span></span>

### <span data-ttu-id="f1ad1-108">Beispiel 1: Erstellen und Zuordnen eines DDoS-Schutzplans zu einem neuen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f1ad1-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="f1ad1-109">Zunächst erstellen wir einen neuen DDoS-Schutzplan mit dem Befehl **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="f1ad1-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="f1ad1-110">Anschließend erstellen wir ein neues virtuelles Netzwerk mit **New-AzVirtualNetwork** und geben die ID des neu erstellten Plans im Parameter **DdosProtectionPlanId** an.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="f1ad1-111">Da wir das virtuelle Netzwerk mit einem Plan verknüpfen, können wir in diesem Fall auch den Parameter **EnableDdoSProtection** angeben.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="f1ad1-112">Beispiel 2: Erstellen und Zuordnen eines DDoS-Schutzplans zu einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f1ad1-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
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
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="f1ad1-113">Zunächst erstellen wir einen neuen DDoS-Schutzplan mit dem Befehl **New-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="f1ad1-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="f1ad1-114">Zweitens erhalten wir die aktuellste Version des virtuellen Netzwerks, das wir dem Plan zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="f1ad1-115">Wir aktualisieren die Eigenschaft **DdosProtectionPlan** mit einem **PSResourceId** -Objekt, das einen Verweis auf die ID des neu erstellten Plans enthält.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="f1ad1-116">In diesem Fall können wir, wenn wir das virtuelle Netzwerk mit einem DDoS-Schutzplan verknüpfen, auch das Flag **EnableDdosProtection** auf "true" festlegen.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="f1ad1-117">Schließlich wird der neue Zustand beibehalten, indem die lokale Variable in **AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="f1ad1-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1ad1-118">PARAMETERS</span></span>

### <span data-ttu-id="f1ad1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1ad1-119">-AsJob</span></span>
<span data-ttu-id="f1ad1-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1ad1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1ad1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ad1-121">-DefaultProfile</span></span>
<span data-ttu-id="f1ad1-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1ad1-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="f1ad1-123">-Location</span></span>
<span data-ttu-id="f1ad1-124">Gibt den Speicherort des zu erstellende DDoS-Schutzplans an.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="f1ad1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f1ad1-125">-Name</span></span>
<span data-ttu-id="f1ad1-126">Gibt den Namen des DDoS-Schutzplans an, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="f1ad1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ad1-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1ad1-128">Gibt die Ressourcengruppe des zu erstellende DDoS-Schutzplans an.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="f1ad1-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1ad1-129">-Tag</span></span>
<span data-ttu-id="f1ad1-130">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ad1-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1ad1-131">-Confirm</span></span>
<span data-ttu-id="f1ad1-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ad1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ad1-133">-WhatIf</span></span>
<span data-ttu-id="f1ad1-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1ad1-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ad1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ad1-136">CommonParameters</span></span>
<span data-ttu-id="f1ad1-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1ad1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ad1-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1ad1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ad1-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1ad1-139">INPUTS</span></span>

### <span data-ttu-id="f1ad1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f1ad1-140">System.String</span></span>

### <span data-ttu-id="f1ad1-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1ad1-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f1ad1-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1ad1-142">OUTPUTS</span></span>

### <span data-ttu-id="f1ad1-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f1ad1-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="f1ad1-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1ad1-144">NOTES</span></span>

## <span data-ttu-id="f1ad1-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1ad1-145">RELATED LINKS</span></span>

[<span data-ttu-id="f1ad1-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f1ad1-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="f1ad1-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f1ad1-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="f1ad1-148">Neu – AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f1ad1-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="f1ad1-149">Satz-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f1ad1-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="f1ad1-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f1ad1-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)