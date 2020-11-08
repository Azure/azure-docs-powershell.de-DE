---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174294"
---
# <span data-ttu-id="4312f-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4312f-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="4312f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4312f-102">SYNOPSIS</span></span>
<span data-ttu-id="4312f-103">Entfernt eine ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="4312f-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="4312f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4312f-104">SYNTAX</span></span>

### <span data-ttu-id="4312f-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4312f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4312f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4312f-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4312f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4312f-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4312f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4312f-108">DESCRIPTION</span></span>
<span data-ttu-id="4312f-109">Mit dem Cmdlet **Remove-AzExpressRoutePort** wird ein ExpressRoutePort entfernt.</span><span class="sxs-lookup"><span data-stu-id="4312f-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="4312f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4312f-110">EXAMPLES</span></span>

### <span data-ttu-id="4312f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4312f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="4312f-112">Entfernt $Portname ExpressRoutePort-Ressource in $RG Ressourcengruppe in Ihrem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4312f-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="4312f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4312f-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="4312f-114">Entfernt die ExpressRoutePort-Ressource in Inputobject.</span><span class="sxs-lookup"><span data-stu-id="4312f-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="4312f-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4312f-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="4312f-116">Entfernt die ExpressRoutePort-Ressource mit der Ressourcen-$ID.</span><span class="sxs-lookup"><span data-stu-id="4312f-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="4312f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="4312f-117">PARAMETERS</span></span>

### <span data-ttu-id="4312f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4312f-118">-AsJob</span></span>
<span data-ttu-id="4312f-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4312f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4312f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4312f-120">-DefaultProfile</span></span>
<span data-ttu-id="4312f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4312f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4312f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4312f-122">-Force</span></span>
<span data-ttu-id="4312f-123">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="4312f-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="4312f-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4312f-124">-InputObject</span></span>
<span data-ttu-id="4312f-125">Das Express-Route-Port-Objekt</span><span class="sxs-lookup"><span data-stu-id="4312f-125">The express route port object</span></span>

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

### <span data-ttu-id="4312f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4312f-126">-Name</span></span>
<span data-ttu-id="4312f-127">Der Name des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="4312f-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="4312f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4312f-128">-PassThru</span></span>
<span data-ttu-id="4312f-129">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4312f-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="4312f-130">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="4312f-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4312f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4312f-131">-ResourceGroupName</span></span>
<span data-ttu-id="4312f-132">Der Ressourcengruppenname des ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="4312f-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="4312f-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4312f-133">-ResourceId</span></span>
<span data-ttu-id="4312f-134">Die Quelle des Express-Route-Ports.</span><span class="sxs-lookup"><span data-stu-id="4312f-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="4312f-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4312f-135">-Confirm</span></span>
<span data-ttu-id="4312f-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4312f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4312f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4312f-137">-WhatIf</span></span>
<span data-ttu-id="4312f-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4312f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4312f-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4312f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4312f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4312f-140">CommonParameters</span></span>
<span data-ttu-id="4312f-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4312f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4312f-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4312f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4312f-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4312f-143">INPUTS</span></span>

### <span data-ttu-id="4312f-144">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4312f-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="4312f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4312f-145">System.String</span></span>

## <span data-ttu-id="4312f-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4312f-146">OUTPUTS</span></span>

### <span data-ttu-id="4312f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4312f-147">System.Boolean</span></span>

## <span data-ttu-id="4312f-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="4312f-148">NOTES</span></span>

## <span data-ttu-id="4312f-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4312f-149">RELATED LINKS</span></span>

[<span data-ttu-id="4312f-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4312f-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="4312f-151">Neu – AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4312f-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="4312f-152">Satz-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4312f-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
