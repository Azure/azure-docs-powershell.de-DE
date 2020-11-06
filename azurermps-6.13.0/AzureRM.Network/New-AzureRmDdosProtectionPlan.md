---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 79a9f0cb2b46150c7746112553949b1bbcbaf1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482310"
---
# <span data-ttu-id="bf691-101">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="bf691-101">New-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="bf691-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf691-102">SYNOPSIS</span></span>
<span data-ttu-id="bf691-103">Erstellt einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="bf691-103">Creates a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf691-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf691-104">SYNTAX</span></span>

```
New-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf691-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf691-105">DESCRIPTION</span></span>
<span data-ttu-id="bf691-106">Das New-AzureRmDdosProtectionPlan-Cmdlet erstellt einen DDoS-Schutzplan.</span><span class="sxs-lookup"><span data-stu-id="bf691-106">The New-AzureRmDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="bf691-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf691-107">EXAMPLES</span></span>

### <span data-ttu-id="bf691-108">Beispiel 1: Erstellen und Zuordnen eines DDoS-Schutzplans zu einem neuen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="bf691-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzureRmVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzureRmvirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="bf691-109">Zunächst erstellen wir einen neuen DDoS-Schutzplan mit dem Befehl **New-AzureRmDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="bf691-109">First, we create a new DDoS Protection plan with the **New-AzureRmDdosProtectionPlan** command.</span></span>
<span data-ttu-id="bf691-110">Anschließend erstellen wir ein neues virtuelles Netzwerk mit **New-AzureRmvirtualNetwork** und geben die ID des neu erstellten Plans im Parameter **DdosProtectionPlanId** an.</span><span class="sxs-lookup"><span data-stu-id="bf691-110">Then, we create a new virtual network with **New-AzureRmvirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="bf691-111">Da wir das virtuelle Netzwerk mit einem Plan verknüpfen, können wir in diesem Fall auch den Parameter **EnableDdoSProtection** angeben.</span><span class="sxs-lookup"><span data-stu-id="bf691-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="bf691-112">Beispiel 2: Erstellen und Zuordnen eines DDoS-Schutzplans zu einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="bf691-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzureRmVirtualNetwork


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

<span data-ttu-id="bf691-113">Zunächst erstellen wir einen neuen DDoS-Schutzplan mit dem Befehl **New-AzureRmDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="bf691-113">First, we create a new DDoS Protection plan with the **New-AzureRmDdosProtectionPlan** command.</span></span>
<span data-ttu-id="bf691-114">Zweitens erhalten wir die aktuellste Version des virtuellen Netzwerks, das wir dem Plan zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="bf691-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="bf691-115">Wir aktualisieren die Eigenschaft **DdosProtectionPlan** mit einem **PSResourceId** -Objekt, das einen Verweis auf die ID des neu erstellten Plans enthält.</span><span class="sxs-lookup"><span data-stu-id="bf691-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="bf691-116">In diesem Fall können wir, wenn wir das virtuelle Netzwerk mit einem DDoS-Schutzplan verknüpfen, auch das Flag **EnableDdosProtection** auf "true" festlegen.</span><span class="sxs-lookup"><span data-stu-id="bf691-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="bf691-117">Schließlich wird der neue Zustand beibehalten, indem die lokale Variable in **AzureRmVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="bf691-117">Finally, we persist the new state by piping the local variable into **Set-AzureRmVirtualNetwork**.</span></span>

## <span data-ttu-id="bf691-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf691-118">PARAMETERS</span></span>

### <span data-ttu-id="bf691-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf691-119">-AsJob</span></span>
<span data-ttu-id="bf691-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bf691-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf691-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf691-121">-DefaultProfile</span></span>
<span data-ttu-id="bf691-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf691-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf691-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="bf691-123">-Location</span></span>
<span data-ttu-id="bf691-124">Gibt den Speicherort des zu erstellende DDoS-Schutzplans an.</span><span class="sxs-lookup"><span data-stu-id="bf691-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="bf691-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bf691-125">-Name</span></span>
<span data-ttu-id="bf691-126">Gibt den Namen des DDoS-Schutzplans an, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf691-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="bf691-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf691-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf691-128">Gibt die Ressourcengruppe des zu erstellende DDoS-Schutzplans an.</span><span class="sxs-lookup"><span data-stu-id="bf691-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="bf691-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf691-129">-Tag</span></span>
<span data-ttu-id="bf691-130">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf691-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bf691-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf691-131">-Confirm</span></span>
<span data-ttu-id="bf691-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf691-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf691-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf691-133">-WhatIf</span></span>
<span data-ttu-id="bf691-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf691-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf691-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf691-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf691-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf691-136">CommonParameters</span></span>
<span data-ttu-id="bf691-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf691-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf691-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf691-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf691-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf691-139">INPUTS</span></span>

### <span data-ttu-id="bf691-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bf691-140">System.String</span></span>

### <span data-ttu-id="bf691-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bf691-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bf691-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf691-142">OUTPUTS</span></span>

### <span data-ttu-id="bf691-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="bf691-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="bf691-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf691-144">NOTES</span></span>

## <span data-ttu-id="bf691-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf691-145">RELATED LINKS</span></span>

[<span data-ttu-id="bf691-146">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="bf691-146">Get-AzureRmDdosProtectionPlan</span></span>](./Get-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="bf691-147">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="bf691-147">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="bf691-148">Neu – AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bf691-148">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="bf691-149">Satz-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bf691-149">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="bf691-150">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bf691-150">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
