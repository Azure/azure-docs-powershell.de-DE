---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165222"
---
# <span data-ttu-id="c231a-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c231a-101">New-AzNatGateway</span></span>

## <span data-ttu-id="c231a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c231a-102">SYNOPSIS</span></span>
<span data-ttu-id="c231a-103">Erstellen Sie eine neue NAT-Gateway-Ressource mit den Eigenschaften Public IP Address/Public IP Prefix, IdleTimeoutInMinutes und SKU.</span><span class="sxs-lookup"><span data-stu-id="c231a-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="c231a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c231a-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c231a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c231a-105">DESCRIPTION</span></span>
<span data-ttu-id="c231a-106">Das Cmdlet **New-AzNatGateway** erstellt eine NAT-Gateway-Ressource.</span><span class="sxs-lookup"><span data-stu-id="c231a-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="c231a-107">Eine natgateway erfordert Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c231a-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="c231a-108">Öffentliche IP-Adresse und/oder öffentliches IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="c231a-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="c231a-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c231a-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="c231a-110">SKU</span><span class="sxs-lookup"><span data-stu-id="c231a-110">Sku</span></span>
- <span data-ttu-id="c231a-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c231a-111">ResourceGroupName</span></span>
- <span data-ttu-id="c231a-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="c231a-112">ResourceName</span></span>
- <span data-ttu-id="c231a-113">Lage</span><span class="sxs-lookup"><span data-stu-id="c231a-113">Location</span></span>

## <span data-ttu-id="c231a-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c231a-114">EXAMPLES</span></span>

### <span data-ttu-id="c231a-115">Beispiel 1: Erstellen eines NAT-Gateways mit öffentlicher IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="c231a-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="c231a-116">Beispiel 2: Erstellen eines NAT-Gateways mit öffentlichem IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="c231a-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="c231a-117">Beispiel 3: Erstellen eines NAT-Gateways mit öffentlicher IP-Adresse in der Verfügbarkeits Zone 1</span><span class="sxs-lookup"><span data-stu-id="c231a-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="c231a-118">Der erste Befehl erstellt die standardmäßige öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c231a-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="c231a-119">Der zweite Befehl erstellt NAT-Gateway mit öffentlicher IP-Adresse in Availability Zone 1.</span><span class="sxs-lookup"><span data-stu-id="c231a-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="c231a-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c231a-120">PARAMETERS</span></span>

### <span data-ttu-id="c231a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c231a-121">-AsJob</span></span>
<span data-ttu-id="c231a-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c231a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c231a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c231a-123">-DefaultProfile</span></span>
<span data-ttu-id="c231a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c231a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c231a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c231a-125">-Force</span></span>
<span data-ttu-id="c231a-126">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="c231a-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c231a-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c231a-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c231a-128">Das Leerlauftimeout des NAT-Gateways.</span><span class="sxs-lookup"><span data-stu-id="c231a-128">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c231a-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="c231a-129">-Location</span></span>
<span data-ttu-id="c231a-130">Die Position.</span><span class="sxs-lookup"><span data-stu-id="c231a-130">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c231a-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c231a-131">-Name</span></span>
<span data-ttu-id="c231a-132">Der Name des NAT-Gateways.</span><span class="sxs-lookup"><span data-stu-id="c231a-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c231a-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c231a-133">-PublicIpAddress</span></span>
<span data-ttu-id="c231a-134">Ein Array von öffentlichen IP-Adressen, die der NAT-Gateway-Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c231a-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c231a-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c231a-135">-PublicIpPrefix</span></span>
<span data-ttu-id="c231a-136">Ein Array von öffentlichen IP-Präfixen, die der NAT-Gateway-Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c231a-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c231a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c231a-137">-ResourceGroupName</span></span>
<span data-ttu-id="c231a-138">Der Ressourcengruppenname des NAT-Gateways.</span><span class="sxs-lookup"><span data-stu-id="c231a-138">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c231a-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="c231a-139">-Sku</span></span>
<span data-ttu-id="c231a-140">Name einer NAT-Gateway-SKU</span><span class="sxs-lookup"><span data-stu-id="c231a-140">Name of a NAT gateway SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c231a-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="c231a-141">-Tag</span></span>
<span data-ttu-id="c231a-142">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="c231a-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c231a-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="c231a-143">-Zone</span></span>
<span data-ttu-id="c231a-144">Eine Liste der Verfügbarkeits Zonen, die die Zone kennzeichnen, in der NAT-Gateway bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c231a-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c231a-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c231a-145">-Confirm</span></span>
<span data-ttu-id="c231a-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c231a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c231a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c231a-147">-WhatIf</span></span>
<span data-ttu-id="c231a-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c231a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c231a-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c231a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c231a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c231a-150">CommonParameters</span></span>
<span data-ttu-id="c231a-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c231a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c231a-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c231a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c231a-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c231a-153">INPUTS</span></span>

### <span data-ttu-id="c231a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="c231a-154">System.String</span></span>

### <span data-ttu-id="c231a-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c231a-155">System.Int32</span></span>

### <span data-ttu-id="c231a-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c231a-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c231a-157">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="c231a-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="c231a-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c231a-158">OUTPUTS</span></span>

### <span data-ttu-id="c231a-159">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="c231a-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="c231a-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="c231a-160">NOTES</span></span>

## <span data-ttu-id="c231a-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c231a-161">RELATED LINKS</span></span>
