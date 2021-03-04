---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: e0c8b550b6d9571c3dd55552bab101441085f3ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944854"
---
# <span data-ttu-id="356f3-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="356f3-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="356f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="356f3-102">SYNOPSIS</span></span>
<span data-ttu-id="356f3-103">Aktualisieren Sie die Nat-Gateway-Ressource mit öffentlicher IP-Adresse, öffentlichem Ip-Präfix und IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="356f3-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="356f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="356f3-104">SYNTAX</span></span>

### <span data-ttu-id="356f3-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="356f3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="356f3-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="356f3-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="356f3-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="356f3-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="356f3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="356f3-108">DESCRIPTION</span></span>
<span data-ttu-id="356f3-109">Aktualisieren Sie die Nat-Gateway-Ressource mit öffentlicher IP-Adresse, öffentlichem Ip-Präfix und IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="356f3-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="356f3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="356f3-110">EXAMPLES</span></span>

### <span data-ttu-id="356f3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="356f3-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="356f3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="356f3-112">PARAMETERS</span></span>

### <span data-ttu-id="356f3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="356f3-113">-AsJob</span></span>
<span data-ttu-id="356f3-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="356f3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="356f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356f3-115">-DefaultProfile</span></span>
<span data-ttu-id="356f3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="356f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="356f3-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="356f3-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="356f3-118">Das Leerlauftimeout des nat-Gateways.</span><span class="sxs-lookup"><span data-stu-id="356f3-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="356f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="356f3-119">-InputObject</span></span>
<span data-ttu-id="356f3-120">Gibt Nat Gateway Resource an.</span><span class="sxs-lookup"><span data-stu-id="356f3-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="356f3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="356f3-121">-Name</span></span>
<span data-ttu-id="356f3-122">Name der Nat-Gateway-Ressource.</span><span class="sxs-lookup"><span data-stu-id="356f3-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356f3-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="356f3-123">-PublicIpAddress</span></span>
<span data-ttu-id="356f3-124">Ein Array von öffentlichen IP-Adressen, die der Nat-Gateway-Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="356f3-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="356f3-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="356f3-125">-PublicIpPrefix</span></span>
<span data-ttu-id="356f3-126">Ein Array von öffentlichen IP-Präfixen, die der Nat-Gateway-Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="356f3-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="356f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="356f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="356f3-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="356f3-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356f3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="356f3-129">-ResourceId</span></span>
<span data-ttu-id="356f3-130">Gibt die ID der Nat Gateway-Ressource an.</span><span class="sxs-lookup"><span data-stu-id="356f3-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="356f3-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="356f3-131">-Confirm</span></span>
<span data-ttu-id="356f3-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="356f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="356f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="356f3-133">-WhatIf</span></span>
<span data-ttu-id="356f3-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="356f3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="356f3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="356f3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="356f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356f3-136">CommonParameters</span></span>
<span data-ttu-id="356f3-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="356f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356f3-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="356f3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356f3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="356f3-139">INPUTS</span></span>

### <span data-ttu-id="356f3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="356f3-140">System.String</span></span>

### <span data-ttu-id="356f3-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="356f3-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="356f3-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="356f3-142">OUTPUTS</span></span>

### <span data-ttu-id="356f3-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="356f3-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="356f3-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="356f3-144">NOTES</span></span>

## <span data-ttu-id="356f3-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="356f3-145">RELATED LINKS</span></span>
