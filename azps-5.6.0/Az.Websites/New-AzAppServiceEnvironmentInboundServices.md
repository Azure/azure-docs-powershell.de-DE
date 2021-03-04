---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironmentinboundservices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
ms.openlocfilehash: 68b2957e959365187ad82980bd2be2f055632a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944380"
---
# <span data-ttu-id="07123-101">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="07123-101">New-AzAppServiceEnvironmentInboundServices</span></span>

## <span data-ttu-id="07123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07123-102">SYNOPSIS</span></span>
<span data-ttu-id="07123-103">Erstellt eingehende Dienste für die App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="07123-103">Creates inbound services for App Service Environment.</span></span> <span data-ttu-id="07123-104">Für ASEv2 ILB wird dadurch eine private Azure-DNS-Zone und -Einträge erstellt, die der internen IP zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07123-104">For ASEv2 ILB, this will create an Azure Private DNS Zone and records to map to the internal IP.</span></span> <span data-ttu-id="07123-105">Für ASEv3 stellt es außerdem sicher, dass das Subnetz die Netzwerkrichtlinie deaktiviert hat, und erstellt einen privaten Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="07123-105">For ASEv3 it will in addition ensure subnet has Network Policy disabled and will create a private endpoint.</span></span>

## <span data-ttu-id="07123-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07123-106">SYNTAX</span></span>

### <span data-ttu-id="07123-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="07123-107">SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkName <String> -SubnetName <String> [-SkipDns] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07123-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07123-108">SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String> -SubnetId <String>
 [-SkipDns] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07123-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07123-109">DESCRIPTION</span></span>
<span data-ttu-id="07123-110">Das **Cmdlet New-AzAppServiceEnvironmentInboundServices** erstellt eingehende Dienste für eine App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="07123-110">The **New-AzAppServiceEnvironmentInboundServices** cmdlet create inbound services for an App Service Environment.</span></span>

## <span data-ttu-id="07123-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07123-111">EXAMPLES</span></span>

### <span data-ttu-id="07123-112">Beispiel 1: Erstellen einer privaten DNS-Zone und Datensätze für ASEv2</span><span class="sxs-lookup"><span data-stu-id="07123-112">Example 1: Create Private DNS Zone and records for ASEv2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="07123-113">Erstellen einer privaten DNS-Zone und Einträge für ASEv2</span><span class="sxs-lookup"><span data-stu-id="07123-113">Create Private DNS Zone and records for ASEv2</span></span>

### <span data-ttu-id="07123-114">Beispiel 2: Erstellen eines privaten Endpunkts, einer privaten DNS-Zone und Datensätzen für ASEv3</span><span class="sxs-lookup"><span data-stu-id="07123-114">Example 2: Create private endpoint, Private DNS Zone and records for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="07123-115">Erstellen von privaten Endpunkten, privater DNS-Zone und Datensätzen für ASEv3</span><span class="sxs-lookup"><span data-stu-id="07123-115">Create private endpoint, Private DNS Zone and records for ASEv3</span></span>

### <span data-ttu-id="07123-116">Beispiel 3: Erstellen eines privaten Endpunkts für ASEv3</span><span class="sxs-lookup"><span data-stu-id="07123-116">Example 3: Create private endpoint for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet -SkipDns
```

<span data-ttu-id="07123-117">Erstellen eines privaten Endpunkts für ASEv3</span><span class="sxs-lookup"><span data-stu-id="07123-117">Create private endpoint for ASEv3</span></span>

## <span data-ttu-id="07123-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="07123-118">PARAMETERS</span></span>

### <span data-ttu-id="07123-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07123-119">-DefaultProfile</span></span>
<span data-ttu-id="07123-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07123-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07123-121">-Name</span><span class="sxs-lookup"><span data-stu-id="07123-121">-Name</span></span>
<span data-ttu-id="07123-122">Der Name der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="07123-122">The name of the app service environment.</span></span>

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

### <span data-ttu-id="07123-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07123-123">-PassThru</span></span>
<span data-ttu-id="07123-124">Rückgabestatus.</span><span class="sxs-lookup"><span data-stu-id="07123-124">Return status.</span></span>

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

### <span data-ttu-id="07123-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07123-125">-ResourceGroupName</span></span>
<span data-ttu-id="07123-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07123-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="07123-127">-SkipDns</span><span class="sxs-lookup"><span data-stu-id="07123-127">-SkipDns</span></span>
<span data-ttu-id="07123-128">Erstellen Sie keine Azure Private DNS Zone und -Einträge.</span><span class="sxs-lookup"><span data-stu-id="07123-128">Do not create Azure Private DNS Zone and records.</span></span>

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

### <span data-ttu-id="07123-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="07123-129">-SubnetId</span></span>
<span data-ttu-id="07123-130">Die Subnetz-ID.</span><span class="sxs-lookup"><span data-stu-id="07123-130">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07123-131">-Subnetzname</span><span class="sxs-lookup"><span data-stu-id="07123-131">-SubnetName</span></span>
<span data-ttu-id="07123-132">Der Subnetzname.</span><span class="sxs-lookup"><span data-stu-id="07123-132">The subnet name.</span></span> <span data-ttu-id="07123-133">Wird in Kombination mit -VirtualNetworkName verwendet und muss in derselben Ressourcengruppe wie ASE enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="07123-133">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="07123-134">Wenn nicht, verwenden Sie -SubnetId.</span><span class="sxs-lookup"><span data-stu-id="07123-134">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07123-135">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="07123-135">-VirtualNetworkName</span></span>
<span data-ttu-id="07123-136">Der vNet-Name.</span><span class="sxs-lookup"><span data-stu-id="07123-136">The vNet name.</span></span> <span data-ttu-id="07123-137">Wird in Kombination mit -SubnetName verwendet und muss sich in derselben Ressourcengruppe wie ASE befinden.</span><span class="sxs-lookup"><span data-stu-id="07123-137">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="07123-138">Wenn nicht, verwenden Sie -SubnetId.</span><span class="sxs-lookup"><span data-stu-id="07123-138">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07123-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07123-139">-Confirm</span></span>
<span data-ttu-id="07123-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07123-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07123-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07123-141">-WhatIf</span></span>
<span data-ttu-id="07123-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07123-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07123-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07123-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07123-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07123-144">CommonParameters</span></span>
<span data-ttu-id="07123-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07123-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07123-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07123-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07123-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07123-147">INPUTS</span></span>

### <span data-ttu-id="07123-148">Keine</span><span class="sxs-lookup"><span data-stu-id="07123-148">None</span></span>

## <span data-ttu-id="07123-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07123-149">OUTPUTS</span></span>

### <span data-ttu-id="07123-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="07123-150">System.Object</span></span>
## <span data-ttu-id="07123-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="07123-151">NOTES</span></span>

## <span data-ttu-id="07123-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="07123-152">RELATED LINKS</span></span>

[<span data-ttu-id="07123-153">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="07123-153">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="07123-154">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="07123-154">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="07123-155">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="07123-155">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)