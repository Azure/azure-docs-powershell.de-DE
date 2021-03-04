---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: 27822e64c697ace3a69e6faf5f291215a2d89935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940091"
---
# <span data-ttu-id="32f90-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32f90-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="32f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32f90-102">SYNOPSIS</span></span>
<span data-ttu-id="32f90-103">Entfernt eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="32f90-103">Removes a network security group.</span></span>

## <span data-ttu-id="32f90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32f90-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32f90-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32f90-105">DESCRIPTION</span></span>
<span data-ttu-id="32f90-106">Das **Cmdlet Remove-AzNetworkSecurityGroup** entfernt eine Azure-Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="32f90-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="32f90-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32f90-107">EXAMPLES</span></span>

### <span data-ttu-id="32f90-108">Beispiel 1: Entfernen einer Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="32f90-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="32f90-109">Mit diesem Befehl wird die Sicherheitsgruppe NSG-FrontEnd in der Ressourcengruppe "TestRG" entfernt.</span><span class="sxs-lookup"><span data-stu-id="32f90-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="32f90-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="32f90-110">PARAMETERS</span></span>

### <span data-ttu-id="32f90-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32f90-111">-AsJob</span></span>
<span data-ttu-id="32f90-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="32f90-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32f90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f90-113">-DefaultProfile</span></span>
<span data-ttu-id="32f90-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32f90-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32f90-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="32f90-115">-Force</span></span>
<span data-ttu-id="32f90-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="32f90-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32f90-117">-Name</span><span class="sxs-lookup"><span data-stu-id="32f90-117">-Name</span></span>
<span data-ttu-id="32f90-118">Gibt den Namen der Netzwerksicherheitsgruppe an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="32f90-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="32f90-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32f90-119">-PassThru</span></span>
<span data-ttu-id="32f90-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="32f90-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32f90-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="32f90-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32f90-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32f90-122">-ResourceGroupName</span></span>
<span data-ttu-id="32f90-123">Gibt den Namen einer Ressourcengruppe an, aus der durch dieses Cmdlet eine Netzwerksicherheitsgruppe entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="32f90-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="32f90-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32f90-124">-Confirm</span></span>
<span data-ttu-id="32f90-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32f90-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32f90-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32f90-126">-WhatIf</span></span>
<span data-ttu-id="32f90-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32f90-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32f90-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32f90-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32f90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f90-129">CommonParameters</span></span>
<span data-ttu-id="32f90-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32f90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f90-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f90-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f90-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32f90-132">INPUTS</span></span>

### <span data-ttu-id="32f90-133">System.String</span><span class="sxs-lookup"><span data-stu-id="32f90-133">System.String</span></span>

## <span data-ttu-id="32f90-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32f90-134">OUTPUTS</span></span>

### <span data-ttu-id="32f90-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32f90-135">System.Boolean</span></span>

## <span data-ttu-id="32f90-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="32f90-136">NOTES</span></span>

## <span data-ttu-id="32f90-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="32f90-137">RELATED LINKS</span></span>

[<span data-ttu-id="32f90-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32f90-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="32f90-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32f90-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="32f90-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32f90-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


