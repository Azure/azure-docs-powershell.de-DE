---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472227"
---
# <span data-ttu-id="a2e55-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a2e55-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="a2e55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2e55-102">SYNOPSIS</span></span>
<span data-ttu-id="a2e55-103">Entfernt eine Firewallrichtlinie für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a2e55-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="a2e55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2e55-104">SYNTAX</span></span>

### <span data-ttu-id="a2e55-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2e55-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2e55-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a2e55-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2e55-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2e55-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2e55-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2e55-108">DESCRIPTION</span></span>
<span data-ttu-id="a2e55-109">Das **Cmdlet "Remove-AzApplicationGatewayFirewallPolicy"** entfernt eine Firewallrichtlinie für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a2e55-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="a2e55-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2e55-110">EXAMPLES</span></span>

### <span data-ttu-id="a2e55-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2e55-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a2e55-112">Mit diesem Befehl wird die Anwendungsgatewayfirewallrichtlinie mit dem Namen ApplicationGatewayFirewallPolicy01 in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="a2e55-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a2e55-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2e55-113">PARAMETERS</span></span>

### <span data-ttu-id="a2e55-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2e55-114">-AsJob</span></span>
<span data-ttu-id="a2e55-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a2e55-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2e55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2e55-116">-DefaultProfile</span></span>
<span data-ttu-id="a2e55-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2e55-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2e55-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a2e55-118">-Force</span></span>
<span data-ttu-id="a2e55-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="a2e55-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a2e55-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2e55-120">-InputObject</span></span>
<span data-ttu-id="a2e55-121">Das Firewallrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="a2e55-121">The firewall policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e55-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a2e55-122">-Name</span></span>
<span data-ttu-id="a2e55-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a2e55-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e55-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2e55-124">-PassThru</span></span>
<span data-ttu-id="a2e55-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a2e55-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a2e55-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a2e55-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a2e55-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2e55-127">-ResourceGroupName</span></span>
<span data-ttu-id="a2e55-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a2e55-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e55-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2e55-129">-ResourceId</span></span>
<span data-ttu-id="a2e55-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a2e55-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2e55-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2e55-131">-Confirm</span></span>
<span data-ttu-id="a2e55-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2e55-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2e55-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a2e55-133">-WhatIf</span></span>
<span data-ttu-id="a2e55-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2e55-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2e55-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2e55-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2e55-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2e55-136">CommonParameters</span></span>
<span data-ttu-id="a2e55-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2e55-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2e55-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2e55-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2e55-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2e55-139">INPUTS</span></span>

### <span data-ttu-id="a2e55-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a2e55-140">System.String</span></span>

## <span data-ttu-id="a2e55-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2e55-141">OUTPUTS</span></span>

### <span data-ttu-id="a2e55-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2e55-142">System.Boolean</span></span>

## <span data-ttu-id="a2e55-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a2e55-143">NOTES</span></span>

## <span data-ttu-id="a2e55-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a2e55-144">RELATED LINKS</span></span>
