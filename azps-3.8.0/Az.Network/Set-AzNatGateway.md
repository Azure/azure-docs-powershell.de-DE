---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997197"
---
# <span data-ttu-id="28fed-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="28fed-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="28fed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28fed-102">SYNOPSIS</span></span>
<span data-ttu-id="28fed-103">Aktualisieren Sie die NAT-Gateway-Ressource mit der öffentlichen IP-Adresse, dem öffentlichen IP-Präfix und IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="28fed-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="28fed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28fed-104">SYNTAX</span></span>

### <span data-ttu-id="28fed-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="28fed-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28fed-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28fed-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28fed-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28fed-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28fed-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28fed-108">DESCRIPTION</span></span>
<span data-ttu-id="28fed-109">Aktualisieren Sie die NAT-Gateway-Ressource mit der öffentlichen IP-Adresse, dem öffentlichen IP-Präfix und IdleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="28fed-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="28fed-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28fed-110">EXAMPLES</span></span>

### <span data-ttu-id="28fed-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28fed-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="28fed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="28fed-112">PARAMETERS</span></span>

### <span data-ttu-id="28fed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28fed-113">-AsJob</span></span>
<span data-ttu-id="28fed-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="28fed-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28fed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28fed-115">-DefaultProfile</span></span>
<span data-ttu-id="28fed-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28fed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28fed-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="28fed-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="28fed-118">Das Leerlauftimeout des NAT-Gateways.</span><span class="sxs-lookup"><span data-stu-id="28fed-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="28fed-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28fed-119">-InputObject</span></span>
<span data-ttu-id="28fed-120">Gibt die NAT-Gateway-Ressource an.</span><span class="sxs-lookup"><span data-stu-id="28fed-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="28fed-121">-Name</span><span class="sxs-lookup"><span data-stu-id="28fed-121">-Name</span></span>
<span data-ttu-id="28fed-122">Der Name der NAT-Gateway-Ressource.</span><span class="sxs-lookup"><span data-stu-id="28fed-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="28fed-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="28fed-123">-PublicIpAddress</span></span>
<span data-ttu-id="28fed-124">Ein Array von öffentlichen IP-Adressen, die der NAT-Gateway-Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="28fed-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="28fed-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="28fed-125">-PublicIpPrefix</span></span>
<span data-ttu-id="28fed-126">Ein Array von öffentlichen IP-Präfixen, die der NAT-Gateway-Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="28fed-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="28fed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28fed-127">-ResourceGroupName</span></span>
<span data-ttu-id="28fed-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="28fed-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="28fed-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="28fed-129">-ResourceId</span></span>
<span data-ttu-id="28fed-130">Gibt die ID der NAT-Gateway-Ressource an.</span><span class="sxs-lookup"><span data-stu-id="28fed-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="28fed-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28fed-131">-Confirm</span></span>
<span data-ttu-id="28fed-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28fed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28fed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28fed-133">-WhatIf</span></span>
<span data-ttu-id="28fed-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28fed-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28fed-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28fed-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28fed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28fed-136">CommonParameters</span></span>
<span data-ttu-id="28fed-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28fed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28fed-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28fed-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28fed-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28fed-139">INPUTS</span></span>

### <span data-ttu-id="28fed-140">System. String</span><span class="sxs-lookup"><span data-stu-id="28fed-140">System.String</span></span>

### <span data-ttu-id="28fed-141">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="28fed-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="28fed-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28fed-142">OUTPUTS</span></span>

### <span data-ttu-id="28fed-143">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="28fed-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="28fed-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="28fed-144">NOTES</span></span>

## <span data-ttu-id="28fed-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28fed-145">RELATED LINKS</span></span>
