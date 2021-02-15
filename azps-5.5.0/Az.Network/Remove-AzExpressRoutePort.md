---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151540"
---
# <span data-ttu-id="b4dc7-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b4dc7-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="b4dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="b4dc7-103">Entfernt einen ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="b4dc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4dc7-104">SYNTAX</span></span>

### <span data-ttu-id="b4dc7-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4dc7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4dc7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4dc7-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4dc7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4dc7-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4dc7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4dc7-108">DESCRIPTION</span></span>
<span data-ttu-id="b4dc7-109">Das **Cmdlet "Remove-AzExpressRoutePort"** entfernt einen ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="b4dc7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4dc7-110">EXAMPLES</span></span>

### <span data-ttu-id="b4dc7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4dc7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="b4dc7-112">Entfernt $PortName "ExpressRoutePort"-Ressource in $rg Ressourcengruppe in Ihrem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="b4dc7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b4dc7-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="b4dc7-114">Entfernt die "ExpressRoutePort"-Ressource in InputObject.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="b4dc7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b4dc7-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="b4dc7-116">Entfernt die Ressource "ExpressRoutePort" mit "ResourceId" $id.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="b4dc7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4dc7-117">PARAMETERS</span></span>

### <span data-ttu-id="b4dc7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4dc7-118">-AsJob</span></span>
<span data-ttu-id="b4dc7-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b4dc7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4dc7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4dc7-120">-DefaultProfile</span></span>
<span data-ttu-id="b4dc7-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4dc7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b4dc7-122">-Force</span></span>
<span data-ttu-id="b4dc7-123">Bestätigen Sie nicht, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="b4dc7-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b4dc7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4dc7-124">-InputObject</span></span>
<span data-ttu-id="b4dc7-125">Das Expressroutenportobjekt</span><span class="sxs-lookup"><span data-stu-id="b4dc7-125">The express route port object</span></span>

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

### <span data-ttu-id="b4dc7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b4dc7-126">-Name</span></span>
<span data-ttu-id="b4dc7-127">Der Name des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="b4dc7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4dc7-128">-PassThru</span></span>
<span data-ttu-id="b4dc7-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b4dc7-130">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4dc7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4dc7-131">-ResourceGroupName</span></span>
<span data-ttu-id="b4dc7-132">Der Ressourcengruppenname des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="b4dc7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4dc7-133">-ResourceId</span></span>
<span data-ttu-id="b4dc7-134">ResourceId des Expressroutenports.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="b4dc7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4dc7-135">-Confirm</span></span>
<span data-ttu-id="b4dc7-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4dc7-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b4dc7-137">-WhatIf</span></span>
<span data-ttu-id="b4dc7-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4dc7-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4dc7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4dc7-140">CommonParameters</span></span>
<span data-ttu-id="b4dc7-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4dc7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4dc7-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4dc7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4dc7-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4dc7-143">INPUTS</span></span>

### <span data-ttu-id="b4dc7-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b4dc7-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="b4dc7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="b4dc7-145">System.String</span></span>

## <span data-ttu-id="b4dc7-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4dc7-146">OUTPUTS</span></span>

### <span data-ttu-id="b4dc7-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4dc7-147">System.Boolean</span></span>

## <span data-ttu-id="b4dc7-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b4dc7-148">NOTES</span></span>

## <span data-ttu-id="b4dc7-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b4dc7-149">RELATED LINKS</span></span>

[<span data-ttu-id="b4dc7-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b4dc7-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="b4dc7-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b4dc7-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="b4dc7-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b4dc7-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
