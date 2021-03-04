---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 430ea183d618779045aaf5d13554edac2ce98626
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941592"
---
# <span data-ttu-id="ce687-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ce687-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="ce687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce687-102">SYNOPSIS</span></span>
<span data-ttu-id="ce687-103">Entfernen Sie die Nat Gateway-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ce687-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="ce687-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce687-104">SYNTAX</span></span>

### <span data-ttu-id="ce687-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce687-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce687-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce687-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce687-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce687-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce687-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce687-108">DESCRIPTION</span></span>
<span data-ttu-id="ce687-109">Entfernen der Nat Gateway-Ressource</span><span class="sxs-lookup"><span data-stu-id="ce687-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="ce687-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce687-110">EXAMPLES</span></span>

### <span data-ttu-id="ce687-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce687-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="ce687-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ce687-112">PARAMETERS</span></span>

### <span data-ttu-id="ce687-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce687-113">-AsJob</span></span>
<span data-ttu-id="ce687-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ce687-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce687-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce687-115">-DefaultProfile</span></span>
<span data-ttu-id="ce687-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce687-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce687-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ce687-117">-Force</span></span>
<span data-ttu-id="ce687-118">Bitten Sie nicht um Bestätigung, wenn Sie die Ressource löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="ce687-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="ce687-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce687-119">-InputObject</span></span>
<span data-ttu-id="ce687-120">Gibt die Nat Gateway-Ressource an.</span><span class="sxs-lookup"><span data-stu-id="ce687-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce687-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ce687-121">-Name</span></span>
<span data-ttu-id="ce687-122">Name der Nat Gateway-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ce687-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce687-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce687-123">-PassThru</span></span>
<span data-ttu-id="ce687-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ce687-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce687-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ce687-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce687-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce687-126">-ResourceGroupName</span></span>
<span data-ttu-id="ce687-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ce687-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce687-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce687-128">-ResourceId</span></span>
<span data-ttu-id="ce687-129">Ressourcen-ID, die dem Nat-Gateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ce687-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce687-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce687-130">-Confirm</span></span>
<span data-ttu-id="ce687-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce687-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce687-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce687-132">-WhatIf</span></span>
<span data-ttu-id="ce687-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce687-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce687-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce687-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce687-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce687-135">CommonParameters</span></span>
<span data-ttu-id="ce687-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce687-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce687-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce687-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce687-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce687-138">INPUTS</span></span>

### <span data-ttu-id="ce687-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="ce687-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="ce687-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ce687-140">System.String</span></span>

## <span data-ttu-id="ce687-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce687-141">OUTPUTS</span></span>

### <span data-ttu-id="ce687-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ce687-142">System.Boolean</span></span>

## <span data-ttu-id="ce687-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ce687-143">NOTES</span></span>

## <span data-ttu-id="ce687-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ce687-144">RELATED LINKS</span></span>
