---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: d725735caf7806233688e6f0bcdddb4edb0f62b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482245"
---
# <span data-ttu-id="84052-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84052-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="84052-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84052-102">SYNOPSIS</span></span>
<span data-ttu-id="84052-103">Entfernt ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="84052-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84052-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84052-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84052-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84052-105">DESCRIPTION</span></span>
<span data-ttu-id="84052-106">Das Cmdlet **Remove-AzureRmLoadBalancer** entfernt ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="84052-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="84052-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84052-107">EXAMPLES</span></span>

### <span data-ttu-id="84052-108">Beispiel 1: Entfernen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="84052-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="84052-109">Mit diesem Befehl wird ein Lastenausgleichsmodul mit dem Namen MyLoadBalancer in der Ressourcengruppe "myresourcegroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="84052-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="84052-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="84052-110">PARAMETERS</span></span>

### <span data-ttu-id="84052-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84052-111">-AsJob</span></span>
<span data-ttu-id="84052-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="84052-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84052-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84052-113">-DefaultProfile</span></span>
<span data-ttu-id="84052-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84052-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84052-115">-Force</span><span class="sxs-lookup"><span data-stu-id="84052-115">-Force</span></span>
<span data-ttu-id="84052-116">Gibt an, dass das Load Balancer vom Cmdlet entfernt wird, unabhängig davon, ob ihm Ressourcen zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="84052-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="84052-117">-Name</span><span class="sxs-lookup"><span data-stu-id="84052-117">-Name</span></span>
<span data-ttu-id="84052-118">Gibt den Namen des zu entfernenden Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="84052-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="84052-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84052-119">-PassThru</span></span>
<span data-ttu-id="84052-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="84052-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84052-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="84052-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="84052-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84052-122">-ResourceGroupName</span></span>
<span data-ttu-id="84052-123">Gibt den Namen der Ressourcengruppe an, die das zu entfernende Load Balancer enthält.</span><span class="sxs-lookup"><span data-stu-id="84052-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="84052-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84052-124">-Confirm</span></span>
<span data-ttu-id="84052-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84052-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84052-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84052-126">-WhatIf</span></span>
<span data-ttu-id="84052-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84052-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84052-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84052-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84052-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84052-129">CommonParameters</span></span>
<span data-ttu-id="84052-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84052-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84052-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84052-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84052-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84052-132">INPUTS</span></span>

### <span data-ttu-id="84052-133">System. String</span><span class="sxs-lookup"><span data-stu-id="84052-133">System.String</span></span>

### <span data-ttu-id="84052-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="84052-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84052-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84052-135">OUTPUTS</span></span>

### <span data-ttu-id="84052-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84052-136">System.Boolean</span></span>

## <span data-ttu-id="84052-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="84052-137">NOTES</span></span>

## <span data-ttu-id="84052-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84052-138">RELATED LINKS</span></span>

[<span data-ttu-id="84052-139">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84052-139">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="84052-140">Neu – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84052-140">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="84052-141">Satz-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84052-141">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


