---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459975"
---
# <span data-ttu-id="80dbf-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="80dbf-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="80dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="80dbf-103">Erstellt eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="80dbf-103">Creates an application security group.</span></span>

## <span data-ttu-id="80dbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80dbf-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80dbf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="80dbf-106">Das **Cmdlet "New-AzApplicationSecurityGroup"** erstellt eine Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="80dbf-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="80dbf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80dbf-107">EXAMPLES</span></span>

### <span data-ttu-id="80dbf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80dbf-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="80dbf-109">In diesem Beispiel wird eine Anwendungssicherheitsgruppe ohne Zuordnungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="80dbf-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="80dbf-110">Nachdem sie erstellt wurde, können die IP-Konfigurationen in der Netzwerkschnittstelle in die Gruppe eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="80dbf-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="80dbf-111">Sicherheitsregeln können sich auch als Quellen oder Ziele auf die Gruppe beziehen.</span><span class="sxs-lookup"><span data-stu-id="80dbf-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="80dbf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80dbf-112">PARAMETERS</span></span>

### <span data-ttu-id="80dbf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80dbf-113">-AsJob</span></span>
<span data-ttu-id="80dbf-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="80dbf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80dbf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80dbf-115">-DefaultProfile</span></span>
<span data-ttu-id="80dbf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80dbf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80dbf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="80dbf-117">-Force</span></span>
<span data-ttu-id="80dbf-118">Fordern Sie keine Bestätigung an, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="80dbf-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="80dbf-119">-Location</span><span class="sxs-lookup"><span data-stu-id="80dbf-119">-Location</span></span>
<span data-ttu-id="80dbf-120">Der Ort.</span><span class="sxs-lookup"><span data-stu-id="80dbf-120">The location.</span></span>

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

### <span data-ttu-id="80dbf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="80dbf-121">-Name</span></span>
<span data-ttu-id="80dbf-122">Der Name der Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="80dbf-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="80dbf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80dbf-123">-ResourceGroupName</span></span>
<span data-ttu-id="80dbf-124">Der Ressourcengruppenname der Anwendungssicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="80dbf-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="80dbf-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="80dbf-125">-Tag</span></span>
<span data-ttu-id="80dbf-126">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="80dbf-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="80dbf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80dbf-127">-Confirm</span></span>
<span data-ttu-id="80dbf-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80dbf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80dbf-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="80dbf-129">-WhatIf</span></span>
<span data-ttu-id="80dbf-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80dbf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80dbf-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80dbf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80dbf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80dbf-132">CommonParameters</span></span>
<span data-ttu-id="80dbf-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80dbf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80dbf-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80dbf-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80dbf-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80dbf-135">INPUTS</span></span>

### <span data-ttu-id="80dbf-136">System.String</span><span class="sxs-lookup"><span data-stu-id="80dbf-136">System.String</span></span>

### <span data-ttu-id="80dbf-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="80dbf-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="80dbf-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80dbf-138">OUTPUTS</span></span>

### <span data-ttu-id="80dbf-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="80dbf-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="80dbf-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="80dbf-140">NOTES</span></span>

## <span data-ttu-id="80dbf-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="80dbf-141">RELATED LINKS</span></span>

[<span data-ttu-id="80dbf-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="80dbf-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="80dbf-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="80dbf-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="80dbf-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80dbf-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="80dbf-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80dbf-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="80dbf-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80dbf-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="80dbf-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="80dbf-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="80dbf-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="80dbf-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="80dbf-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="80dbf-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
