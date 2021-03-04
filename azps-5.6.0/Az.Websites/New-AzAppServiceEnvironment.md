---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
ms.openlocfilehash: a922958ec2e15ea9cb4a3b0189f74dda6d71eab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948184"
---
# <span data-ttu-id="36934-101">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="36934-101">New-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="36934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36934-102">SYNOPSIS</span></span>
<span data-ttu-id="36934-103">Erstellt eine App-Dienstumgebung, die die empfohlene Routentabelle und Netzwerksicherheitsgruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="36934-103">Creates an App Service Environment including the recommended Route Table and Network Security Group</span></span>

## <span data-ttu-id="36934-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36934-104">SYNTAX</span></span>

### <span data-ttu-id="36934-105">ASEv2SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36934-105">ASEv2SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> -LoadBalancerMode <String>
 [-SkipRouteTable] [-SkipNetworkSecurityGroup] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36934-106">ASEv3SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36934-106">ASEv3SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36934-107">ASEv2SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36934-107">ASEv2SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> -LoadBalancerMode <String> [-SkipRouteTable] [-SkipNetworkSecurityGroup]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36934-108">ASEv3SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36934-108">ASEv3SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36934-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36934-109">DESCRIPTION</span></span>
<span data-ttu-id="36934-110">Das **Cmdlet New-AzAppServiceEnvironment** erstellt eine App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="36934-110">The **New-AzAppServiceEnvironment** cmdlet creates an App Service Environment.</span></span>

## <span data-ttu-id="36934-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36934-111">EXAMPLES</span></span>

### <span data-ttu-id="36934-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36934-112">Example 1</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
```

<span data-ttu-id="36934-113">Erstellen einer App-Dienstumgebung mit dem Namen MyAseV2, einschließlich empfohlener Routentabelle und Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="36934-113">Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group</span></span>

### <span data-ttu-id="36934-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="36934-114">Example 2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
        -SkipRouteTable -SkipNetworkSecurityGroup
```

<span data-ttu-id="36934-115">Erstellen Sie die App-Dienstumgebung mit dem Namen MyAseV2 ohne empfohlene Routentabelle und Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="36934-115">Create App Service Environment named MyAseV2 without recommended Route Table and Network Security Group.</span></span>
<span data-ttu-id="36934-116">Diese sollten vor oder direkt nach der Bereitstellung der App-Dienstumgebung erstellt werden, um eine funktionierende Instanz sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="36934-116">These should be create before or right after provisioning the App Service Environment to ensure a functional instance.</span></span>

## <span data-ttu-id="36934-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="36934-117">PARAMETERS</span></span>

### <span data-ttu-id="36934-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36934-118">-AsJob</span></span>
<span data-ttu-id="36934-119">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="36934-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="36934-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36934-120">-DefaultProfile</span></span>
<span data-ttu-id="36934-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36934-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36934-122">-Kind</span><span class="sxs-lookup"><span data-stu-id="36934-122">-Kind</span></span>
<span data-ttu-id="36934-123">Die Version der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="36934-123">The version of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ASEv2, ASEv3

Required: False
Position: 3
Default value: ASEv2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-124">-LoadBalancerMode</span><span class="sxs-lookup"><span data-stu-id="36934-124">-LoadBalancerMode</span></span>
<span data-ttu-id="36934-125">Load Balancer-Modus der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="36934-125">Load balancer mode of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:
Accepted values: Internal, External

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-126">-Location</span><span class="sxs-lookup"><span data-stu-id="36934-126">-Location</span></span>
<span data-ttu-id="36934-127">Der Standort der App-Dienstumgebung, z. B. Westeuropa.</span><span class="sxs-lookup"><span data-stu-id="36934-127">The Location of the app service environment eg: West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-128">-Name</span><span class="sxs-lookup"><span data-stu-id="36934-128">-Name</span></span>
<span data-ttu-id="36934-129">Der Name der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="36934-129">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36934-130">-PassThru</span></span>
<span data-ttu-id="36934-131">Geben Sie das App-Dienstumgebungsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="36934-131">Return the app service environment object.</span></span>

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

### <span data-ttu-id="36934-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36934-132">-ResourceGroupName</span></span>
<span data-ttu-id="36934-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="36934-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-134">-SkipNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="36934-134">-SkipNetworkSecurityGroup</span></span>
<span data-ttu-id="36934-135">Erstellen Sie die empfohlene Netzwerksicherheitsgruppe nicht als Teil der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="36934-135">Do not create the recommended network security group as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-136">-SkipRouteTable</span><span class="sxs-lookup"><span data-stu-id="36934-136">-SkipRouteTable</span></span>
<span data-ttu-id="36934-137">Erstellen Sie die empfohlene Routentabelle nicht als Teil der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="36934-137">Do not create the recommended route table as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="36934-138">-SubnetId</span></span>
<span data-ttu-id="36934-139">Die Subnetz-ID.</span><span class="sxs-lookup"><span data-stu-id="36934-139">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetIdParameterSet, ASEv3SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-140">-Subnetzname</span><span class="sxs-lookup"><span data-stu-id="36934-140">-SubnetName</span></span>
<span data-ttu-id="36934-141">Der Subnetzname.</span><span class="sxs-lookup"><span data-stu-id="36934-141">The subnet name.</span></span> <span data-ttu-id="36934-142">Wird in Kombination mit -VirtualNetworkName verwendet und muss in derselben Ressourcengruppe wie ASE enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="36934-142">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="36934-143">Wenn nicht, verwenden Sie -SubnetId.</span><span class="sxs-lookup"><span data-stu-id="36934-143">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="36934-144">-VirtualNetworkName</span></span>
<span data-ttu-id="36934-145">Der vNet-Name.</span><span class="sxs-lookup"><span data-stu-id="36934-145">The vNet name.</span></span> <span data-ttu-id="36934-146">Wird in Kombination mit -SubnetName verwendet und muss sich in derselben Ressourcengruppe wie ASE befinden.</span><span class="sxs-lookup"><span data-stu-id="36934-146">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="36934-147">Wenn nicht, verwenden Sie -SubnetId.</span><span class="sxs-lookup"><span data-stu-id="36934-147">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36934-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36934-148">-Confirm</span></span>
<span data-ttu-id="36934-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36934-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36934-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36934-150">-WhatIf</span></span>
<span data-ttu-id="36934-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36934-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36934-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36934-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36934-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36934-153">CommonParameters</span></span>
<span data-ttu-id="36934-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36934-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36934-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36934-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36934-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36934-156">INPUTS</span></span>

### <span data-ttu-id="36934-157">Keine</span><span class="sxs-lookup"><span data-stu-id="36934-157">None</span></span>

## <span data-ttu-id="36934-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36934-158">OUTPUTS</span></span>

### <span data-ttu-id="36934-159">System.Object</span><span class="sxs-lookup"><span data-stu-id="36934-159">System.Object</span></span>
## <span data-ttu-id="36934-160">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="36934-160">NOTES</span></span>

## <span data-ttu-id="36934-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="36934-161">RELATED LINKS</span></span>

[<span data-ttu-id="36934-162">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="36934-162">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="36934-163">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="36934-163">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="36934-164">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="36934-164">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)
