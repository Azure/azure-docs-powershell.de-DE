---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 6757c9c0b9eeb0b3408a07713c62812d361d814a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504825"
---
# <span data-ttu-id="720b8-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720b8-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="720b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="720b8-102">SYNOPSIS</span></span>
<span data-ttu-id="720b8-103">Entfernt ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="720b8-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="720b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="720b8-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="720b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="720b8-105">DESCRIPTION</span></span>
<span data-ttu-id="720b8-106">Das Cmdlet **Remove-AzureRmLoadBalancer** entfernt ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="720b8-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="720b8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="720b8-107">EXAMPLES</span></span>

### <span data-ttu-id="720b8-108">Beispiel 1: Entfernen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="720b8-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="720b8-109">Mit diesem Befehl wird ein Lastenausgleichsmodul mit dem Namen MyLoadBalancer in der Ressourcengruppe "myresourcegroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="720b8-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="720b8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="720b8-110">PARAMETERS</span></span>

### <span data-ttu-id="720b8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="720b8-111">-Force</span></span>
<span data-ttu-id="720b8-112">Gibt an, dass das Load Balancer vom Cmdlet entfernt wird, unabhängig davon, ob ihm Ressourcen zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="720b8-112">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="720b8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="720b8-113">-Name</span></span>
<span data-ttu-id="720b8-114">Gibt den Namen des zu entfernenden Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="720b8-114">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="720b8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="720b8-115">-PassThru</span></span>
<span data-ttu-id="720b8-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="720b8-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="720b8-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="720b8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="720b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="720b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="720b8-119">Gibt den Namen der Ressourcengruppe an, die das zu entfernende Load Balancer enthält.</span><span class="sxs-lookup"><span data-stu-id="720b8-119">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="720b8-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="720b8-120">-Confirm</span></span>
<span data-ttu-id="720b8-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="720b8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="720b8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="720b8-122">-WhatIf</span></span>
<span data-ttu-id="720b8-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="720b8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="720b8-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="720b8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="720b8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720b8-125">-DefaultProfile</span></span>
<span data-ttu-id="720b8-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="720b8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="720b8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720b8-127">CommonParameters</span></span>
<span data-ttu-id="720b8-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="720b8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720b8-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="720b8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720b8-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="720b8-130">INPUTS</span></span>

## <span data-ttu-id="720b8-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="720b8-131">OUTPUTS</span></span>

## <span data-ttu-id="720b8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="720b8-132">NOTES</span></span>

## <span data-ttu-id="720b8-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="720b8-133">RELATED LINKS</span></span>

[<span data-ttu-id="720b8-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720b8-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="720b8-135">Neu – AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720b8-135">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="720b8-136">Satz-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="720b8-136">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


