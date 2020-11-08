---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 271033c39e049a423a15228968ad20c985b57036
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176287"
---
# <span data-ttu-id="a9ea7-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9ea7-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="a9ea7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ea7-103">Entfernt ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-103">Removes a load balancer.</span></span>

## <span data-ttu-id="a9ea7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9ea7-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9ea7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ea7-106">Das Cmdlet **Remove-AzLoadBalancer** entfernt ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="a9ea7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ea7-108">Beispiel 1: Entfernen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="a9ea7-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a9ea7-109">Mit diesem Befehl wird ein Lastenausgleichsmodul mit dem Namen MyLoadBalancer in der Ressourcengruppe "myresourcegroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a9ea7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9ea7-110">PARAMETERS</span></span>

### <span data-ttu-id="a9ea7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9ea7-111">-AsJob</span></span>
<span data-ttu-id="a9ea7-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a9ea7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9ea7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ea7-113">-DefaultProfile</span></span>
<span data-ttu-id="a9ea7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9ea7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a9ea7-115">-Force</span></span>
<span data-ttu-id="a9ea7-116">Gibt an, dass das Load Balancer vom Cmdlet entfernt wird, unabhängig davon, ob ihm Ressourcen zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="a9ea7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a9ea7-117">-Name</span></span>
<span data-ttu-id="a9ea7-118">Gibt den Namen des zu entfernenden Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="a9ea7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9ea7-119">-PassThru</span></span>
<span data-ttu-id="a9ea7-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a9ea7-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a9ea7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ea7-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9ea7-123">Gibt den Namen der Ressourcengruppe an, die das zu entfernende Load Balancer enthält.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="a9ea7-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9ea7-124">-Confirm</span></span>
<span data-ttu-id="a9ea7-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9ea7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9ea7-126">-WhatIf</span></span>
<span data-ttu-id="a9ea7-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9ea7-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9ea7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ea7-129">CommonParameters</span></span>
<span data-ttu-id="a9ea7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ea7-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ea7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ea7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9ea7-132">INPUTS</span></span>

### <span data-ttu-id="a9ea7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a9ea7-133">System.String</span></span>

## <span data-ttu-id="a9ea7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9ea7-134">OUTPUTS</span></span>

### <span data-ttu-id="a9ea7-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9ea7-135">System.Boolean</span></span>

## <span data-ttu-id="a9ea7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9ea7-136">NOTES</span></span>

## <span data-ttu-id="a9ea7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9ea7-137">RELATED LINKS</span></span>

[<span data-ttu-id="a9ea7-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9ea7-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a9ea7-139">Neu – AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9ea7-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="a9ea7-140">Satz-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9ea7-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


