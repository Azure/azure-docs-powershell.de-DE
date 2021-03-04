---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: c0110186277df7e41b9110b1cfdf2fa7b948b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941664"
---
# <span data-ttu-id="d6c79-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d6c79-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="d6c79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6c79-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c79-103">Entfernt einen ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d6c79-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="d6c79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6c79-104">SYNTAX</span></span>

### <span data-ttu-id="d6c79-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6c79-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6c79-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6c79-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6c79-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6c79-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6c79-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6c79-108">DESCRIPTION</span></span>
<span data-ttu-id="d6c79-109">Das **Cmdlet Remove-AzExpressRoutePort** entfernt einen ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d6c79-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="d6c79-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6c79-110">EXAMPLES</span></span>

### <span data-ttu-id="d6c79-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6c79-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="d6c79-112">Entfernt $PortName ExpressRoutePort-Ressource in $rg Ressourcengruppe in Ihrem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6c79-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="d6c79-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d6c79-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="d6c79-114">Entfernt die ExpressRoutePort-Ressource in InputObject.</span><span class="sxs-lookup"><span data-stu-id="d6c79-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="d6c79-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d6c79-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="d6c79-116">Entfernt die ExpressRoutePort-Ressource mit ResourceId-$id.</span><span class="sxs-lookup"><span data-stu-id="d6c79-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="d6c79-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d6c79-117">PARAMETERS</span></span>

### <span data-ttu-id="d6c79-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6c79-118">-AsJob</span></span>
<span data-ttu-id="d6c79-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d6c79-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6c79-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c79-120">-DefaultProfile</span></span>
<span data-ttu-id="d6c79-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6c79-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6c79-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d6c79-122">-Force</span></span>
<span data-ttu-id="d6c79-123">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="d6c79-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="d6c79-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6c79-124">-InputObject</span></span>
<span data-ttu-id="d6c79-125">Das Expressroutenportobjekt</span><span class="sxs-lookup"><span data-stu-id="d6c79-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6c79-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d6c79-126">-Name</span></span>
<span data-ttu-id="d6c79-127">Der Name des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d6c79-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6c79-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6c79-128">-PassThru</span></span>
<span data-ttu-id="d6c79-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d6c79-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d6c79-130">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d6c79-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d6c79-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c79-131">-ResourceGroupName</span></span>
<span data-ttu-id="d6c79-132">Der Ressourcengruppenname des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d6c79-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6c79-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6c79-133">-ResourceId</span></span>
<span data-ttu-id="d6c79-134">ResourceId des Expressroutenports.</span><span class="sxs-lookup"><span data-stu-id="d6c79-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6c79-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6c79-135">-Confirm</span></span>
<span data-ttu-id="d6c79-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6c79-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6c79-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6c79-137">-WhatIf</span></span>
<span data-ttu-id="d6c79-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6c79-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6c79-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6c79-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6c79-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c79-140">CommonParameters</span></span>
<span data-ttu-id="d6c79-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6c79-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c79-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6c79-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c79-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6c79-143">INPUTS</span></span>

### <span data-ttu-id="d6c79-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d6c79-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="d6c79-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d6c79-145">System.String</span></span>

## <span data-ttu-id="d6c79-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6c79-146">OUTPUTS</span></span>

### <span data-ttu-id="d6c79-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6c79-147">System.Boolean</span></span>

## <span data-ttu-id="d6c79-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d6c79-148">NOTES</span></span>

## <span data-ttu-id="d6c79-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d6c79-149">RELATED LINKS</span></span>

[<span data-ttu-id="d6c79-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d6c79-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="d6c79-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d6c79-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="d6c79-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d6c79-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
