---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176164"
---
# <span data-ttu-id="b00eb-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="b00eb-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="b00eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b00eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b00eb-103">Entfernen Sie die NAT-Gateway-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b00eb-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="b00eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b00eb-104">SYNTAX</span></span>

### <span data-ttu-id="b00eb-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b00eb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b00eb-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b00eb-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b00eb-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b00eb-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b00eb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b00eb-108">DESCRIPTION</span></span>
<span data-ttu-id="b00eb-109">Entfernen der NAT-Gateway-Ressource</span><span class="sxs-lookup"><span data-stu-id="b00eb-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="b00eb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b00eb-110">EXAMPLES</span></span>

### <span data-ttu-id="b00eb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b00eb-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="b00eb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b00eb-112">PARAMETERS</span></span>

### <span data-ttu-id="b00eb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b00eb-113">-AsJob</span></span>
<span data-ttu-id="b00eb-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b00eb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b00eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00eb-115">-DefaultProfile</span></span>
<span data-ttu-id="b00eb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b00eb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b00eb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b00eb-117">-Force</span></span>
<span data-ttu-id="b00eb-118">Bitten Sie nicht um Bestätigung, wenn Sie die Ressource löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="b00eb-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="b00eb-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b00eb-119">-InputObject</span></span>
<span data-ttu-id="b00eb-120">Gibt die NAT-Gateway-Ressource an.</span><span class="sxs-lookup"><span data-stu-id="b00eb-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="b00eb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b00eb-121">-Name</span></span>
<span data-ttu-id="b00eb-122">Der Name der NAT-Gateway-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b00eb-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="b00eb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b00eb-123">-PassThru</span></span>
<span data-ttu-id="b00eb-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b00eb-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b00eb-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b00eb-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b00eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="b00eb-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b00eb-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="b00eb-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b00eb-128">-ResourceId</span></span>
<span data-ttu-id="b00eb-129">Ressourcen-ID, die dem NAT-Gateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b00eb-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="b00eb-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b00eb-130">-Confirm</span></span>
<span data-ttu-id="b00eb-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b00eb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00eb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00eb-132">-WhatIf</span></span>
<span data-ttu-id="b00eb-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b00eb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00eb-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b00eb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00eb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00eb-135">CommonParameters</span></span>
<span data-ttu-id="b00eb-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00eb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00eb-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b00eb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00eb-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b00eb-138">INPUTS</span></span>

### <span data-ttu-id="b00eb-139">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="b00eb-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="b00eb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b00eb-140">System.String</span></span>

## <span data-ttu-id="b00eb-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b00eb-141">OUTPUTS</span></span>

### <span data-ttu-id="b00eb-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b00eb-142">System.Boolean</span></span>

## <span data-ttu-id="b00eb-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b00eb-143">NOTES</span></span>

## <span data-ttu-id="b00eb-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b00eb-144">RELATED LINKS</span></span>
