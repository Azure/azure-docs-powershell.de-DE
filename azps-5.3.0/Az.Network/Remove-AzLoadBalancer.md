---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468928"
---
# <span data-ttu-id="7b8e6-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b8e6-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="7b8e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b8e6-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8e6-103">Entfernt einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-103">Removes a load balancer.</span></span>

## <span data-ttu-id="7b8e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b8e6-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b8e6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b8e6-105">DESCRIPTION</span></span>
<span data-ttu-id="7b8e6-106">Das **Cmdlet "Remove-AzLoadBalancer"** entfernt einen Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="7b8e6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7b8e6-107">EXAMPLES</span></span>

### <span data-ttu-id="7b8e6-108">Beispiel 1: Entfernen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="7b8e6-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7b8e6-109">Mit diesem Befehl wird ein Lastenausgleich mit dem Namen "MyLoadBalancer" in der Ressourcengruppe "MyResourceGroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7b8e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b8e6-110">PARAMETERS</span></span>

### <span data-ttu-id="7b8e6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b8e6-111">-AsJob</span></span>
<span data-ttu-id="7b8e6-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7b8e6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b8e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8e6-113">-DefaultProfile</span></span>
<span data-ttu-id="7b8e6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b8e6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7b8e6-115">-Force</span></span>
<span data-ttu-id="7b8e6-116">Gibt an, dass mit diesem Cmdlet der Lastenausgleich entfernt wird, unabhängig davon, ob ihm Ressourcen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="7b8e6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7b8e6-117">-Name</span></span>
<span data-ttu-id="7b8e6-118">Gibt den Namen des zu entfernenden Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8e6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b8e6-119">-PassThru</span></span>
<span data-ttu-id="7b8e6-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7b8e6-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7b8e6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b8e6-122">-ResourceGroupName</span></span>
<span data-ttu-id="7b8e6-123">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden Lastenausgleich enthält.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b8e6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b8e6-124">-Confirm</span></span>
<span data-ttu-id="7b8e6-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8e6-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7b8e6-126">-WhatIf</span></span>
<span data-ttu-id="7b8e6-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b8e6-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b8e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8e6-129">CommonParameters</span></span>
<span data-ttu-id="7b8e6-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b8e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8e6-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b8e6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8e6-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7b8e6-132">INPUTS</span></span>

### <span data-ttu-id="7b8e6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7b8e6-133">System.String</span></span>

## <span data-ttu-id="7b8e6-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7b8e6-134">OUTPUTS</span></span>

### <span data-ttu-id="7b8e6-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b8e6-135">System.Boolean</span></span>

## <span data-ttu-id="7b8e6-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7b8e6-136">NOTES</span></span>

## <span data-ttu-id="7b8e6-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7b8e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="7b8e6-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b8e6-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="7b8e6-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b8e6-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="7b8e6-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b8e6-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


