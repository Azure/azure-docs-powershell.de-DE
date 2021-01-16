---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470219"
---
# <span data-ttu-id="141be-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="141be-101">New-AzNatGateway</span></span>

## <span data-ttu-id="141be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="141be-102">SYNOPSIS</span></span>
<span data-ttu-id="141be-103">Erstellen Sie eine neue Nat-Gateway-Ressource mit den Eigenschaften Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes und SKU.</span><span class="sxs-lookup"><span data-stu-id="141be-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="141be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="141be-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="141be-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="141be-105">DESCRIPTION</span></span>
<span data-ttu-id="141be-106">Das **Cmdlet "New-AzNatGateway"** erstellt eine Nat-Gateway-Ressource.</span><span class="sxs-lookup"><span data-stu-id="141be-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="141be-107">Für ein Natgateway ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="141be-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="141be-108">Öffentliche IP-Adresse und/oder Präfix für öffentliche Ip</span><span class="sxs-lookup"><span data-stu-id="141be-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="141be-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="141be-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="141be-110">SKU</span><span class="sxs-lookup"><span data-stu-id="141be-110">Sku</span></span>
- <span data-ttu-id="141be-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="141be-111">ResourceGroupName</span></span>
- <span data-ttu-id="141be-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="141be-112">ResourceName</span></span>
- <span data-ttu-id="141be-113">Position</span><span class="sxs-lookup"><span data-stu-id="141be-113">Location</span></span>

## <span data-ttu-id="141be-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="141be-114">EXAMPLES</span></span>

### <span data-ttu-id="141be-115">Beispiel 1: Nat Gateway mit öffentlicher IP-Adresse erstellen</span><span class="sxs-lookup"><span data-stu-id="141be-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="141be-116">Beispiel 2: Nat Gateway mit öffentlichem Ip-Präfix erstellen</span><span class="sxs-lookup"><span data-stu-id="141be-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="141be-117">Beispiel 3: Nat Gateway mit öffentlicher IP-Adresse in Verfügbarkeitszone 1 erstellen</span><span class="sxs-lookup"><span data-stu-id="141be-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="141be-118">Der erste Befehl erstellt eine standardmäßige öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="141be-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="141be-119">Mit dem zweiten Befehl wird das NAT-Gateway mit der öffentlichen IP-Adresse in der Verfügbarkeitszone 1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="141be-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="141be-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="141be-120">PARAMETERS</span></span>

### <span data-ttu-id="141be-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="141be-121">-AsJob</span></span>
<span data-ttu-id="141be-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="141be-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="141be-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141be-123">-DefaultProfile</span></span>
<span data-ttu-id="141be-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="141be-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="141be-125">-Force</span><span class="sxs-lookup"><span data-stu-id="141be-125">-Force</span></span>
<span data-ttu-id="141be-126">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="141be-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="141be-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="141be-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="141be-128">Das Leerlauftimeout des NAT-Gateways.</span><span class="sxs-lookup"><span data-stu-id="141be-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="141be-129">-Location</span><span class="sxs-lookup"><span data-stu-id="141be-129">-Location</span></span>
<span data-ttu-id="141be-130">Der Speicherort.</span><span class="sxs-lookup"><span data-stu-id="141be-130">The location.</span></span>

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

### <span data-ttu-id="141be-131">-Name</span><span class="sxs-lookup"><span data-stu-id="141be-131">-Name</span></span>
<span data-ttu-id="141be-132">Der Name des NAT-Gateways.</span><span class="sxs-lookup"><span data-stu-id="141be-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="141be-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="141be-133">-PublicIpAddress</span></span>
<span data-ttu-id="141be-134">Ein Array öffentlicher IP-Adressen, die der Nat-Gateway-Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="141be-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="141be-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="141be-135">-PublicIpPrefix</span></span>
<span data-ttu-id="141be-136">Ein Array mit öffentlichen IP-Präfixen, die der Nat-Gateway-Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="141be-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="141be-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="141be-137">-ResourceGroupName</span></span>
<span data-ttu-id="141be-138">Der Ressourcengruppenname des NAT-Gateways.</span><span class="sxs-lookup"><span data-stu-id="141be-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="141be-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="141be-139">-Sku</span></span>
<span data-ttu-id="141be-140">Name einer NAT-Gateway-SKU.</span><span class="sxs-lookup"><span data-stu-id="141be-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="141be-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="141be-141">-Tag</span></span>
<span data-ttu-id="141be-142">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="141be-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="141be-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="141be-143">-Zone</span></span>
<span data-ttu-id="141be-144">Eine Liste der Verfügbarkeitszonen, in denen die Zone aufgeführt ist, in der das Nat Gateway bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="141be-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="141be-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="141be-145">-Confirm</span></span>
<span data-ttu-id="141be-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="141be-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="141be-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="141be-147">-WhatIf</span></span>
<span data-ttu-id="141be-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="141be-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="141be-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="141be-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="141be-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141be-150">CommonParameters</span></span>
<span data-ttu-id="141be-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="141be-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141be-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="141be-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141be-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="141be-153">INPUTS</span></span>

### <span data-ttu-id="141be-154">System.String</span><span class="sxs-lookup"><span data-stu-id="141be-154">System.String</span></span>

### <span data-ttu-id="141be-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="141be-155">System.Int32</span></span>

### <span data-ttu-id="141be-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="141be-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="141be-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="141be-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="141be-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="141be-158">OUTPUTS</span></span>

### <span data-ttu-id="141be-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="141be-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="141be-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="141be-160">NOTES</span></span>

## <span data-ttu-id="141be-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="141be-161">RELATED LINKS</span></span>
