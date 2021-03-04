---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: d0fcdff243294210449eb32f99faa3d9d74cef0f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931571"
---
# <span data-ttu-id="2ca18-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2ca18-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="2ca18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ca18-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca18-103">Erstellt eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2ca18-103">Creates an application security group.</span></span>

## <span data-ttu-id="2ca18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ca18-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca18-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ca18-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca18-106">Das **Cmdlet New-AzApplicationSecurityGroup** erstellt eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2ca18-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="2ca18-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ca18-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca18-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ca18-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="2ca18-109">In diesem Beispiel wird eine Anwendungssicherheitsgruppe ohne Zuordnungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ca18-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="2ca18-110">Sobald sie erstellt wurde, können DIE IP-Konfigurationen in der Netzwerkschnittstelle in die Gruppe einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="2ca18-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="2ca18-111">Sicherheitsregeln können sich auch auf die Gruppe als ihre Quellen oder Ziele beziehen.</span><span class="sxs-lookup"><span data-stu-id="2ca18-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="2ca18-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2ca18-112">PARAMETERS</span></span>

### <span data-ttu-id="2ca18-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ca18-113">-AsJob</span></span>
<span data-ttu-id="2ca18-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2ca18-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ca18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca18-115">-DefaultProfile</span></span>
<span data-ttu-id="2ca18-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ca18-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ca18-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2ca18-117">-Force</span></span>
<span data-ttu-id="2ca18-118">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="2ca18-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="2ca18-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2ca18-119">-Location</span></span>
<span data-ttu-id="2ca18-120">Der Speicherort.</span><span class="sxs-lookup"><span data-stu-id="2ca18-120">The location.</span></span>

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

### <span data-ttu-id="2ca18-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2ca18-121">-Name</span></span>
<span data-ttu-id="2ca18-122">Der Name der Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2ca18-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="2ca18-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca18-123">-ResourceGroupName</span></span>
<span data-ttu-id="2ca18-124">Der Ressourcengruppenname der Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2ca18-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="2ca18-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ca18-125">-Tag</span></span>
<span data-ttu-id="2ca18-126">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ca18-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca18-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ca18-127">-Confirm</span></span>
<span data-ttu-id="2ca18-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ca18-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca18-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca18-129">-WhatIf</span></span>
<span data-ttu-id="2ca18-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ca18-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca18-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ca18-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca18-132">CommonParameters</span></span>
<span data-ttu-id="2ca18-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ca18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca18-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca18-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca18-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ca18-135">INPUTS</span></span>

### <span data-ttu-id="2ca18-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2ca18-136">System.String</span></span>

### <span data-ttu-id="2ca18-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ca18-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2ca18-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ca18-138">OUTPUTS</span></span>

### <span data-ttu-id="2ca18-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2ca18-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="2ca18-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2ca18-140">NOTES</span></span>

## <span data-ttu-id="2ca18-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2ca18-141">RELATED LINKS</span></span>

[<span data-ttu-id="2ca18-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2ca18-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="2ca18-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2ca18-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="2ca18-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ca18-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2ca18-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ca18-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2ca18-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ca18-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2ca18-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2ca18-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2ca18-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2ca18-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2ca18-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2ca18-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
