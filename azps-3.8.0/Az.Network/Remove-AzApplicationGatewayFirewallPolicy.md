---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996744"
---
# <span data-ttu-id="ef94c-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ef94c-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="ef94c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef94c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef94c-103">Entfernt eine Firewall-Richtlinie für Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ef94c-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="ef94c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef94c-104">SYNTAX</span></span>

### <span data-ttu-id="ef94c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef94c-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef94c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ef94c-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef94c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef94c-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef94c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef94c-108">DESCRIPTION</span></span>
<span data-ttu-id="ef94c-109">Das Cmdlet " **Remove-AzApplicationGatewayFirewallPolicy** " entfernt eine Firewall-Richtlinie des Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="ef94c-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="ef94c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef94c-110">EXAMPLES</span></span>

### <span data-ttu-id="ef94c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef94c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ef94c-112">Dieser Befehl entfernt die Anwendungs-Gateway-Firewallrichtlinie mit dem Namen ApplicationGatewayFirewallPolicy01 in der Ressourcengruppe mit dem Namen ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ef94c-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="ef94c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef94c-113">PARAMETERS</span></span>

### <span data-ttu-id="ef94c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef94c-114">-AsJob</span></span>
<span data-ttu-id="ef94c-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ef94c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef94c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef94c-116">-DefaultProfile</span></span>
<span data-ttu-id="ef94c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef94c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef94c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ef94c-118">-Force</span></span>
<span data-ttu-id="ef94c-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="ef94c-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ef94c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ef94c-120">-InputObject</span></span>
<span data-ttu-id="ef94c-121">Das Firewall-Richtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="ef94c-121">The firewall policy object</span></span>

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

### <span data-ttu-id="ef94c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ef94c-122">-Name</span></span>
<span data-ttu-id="ef94c-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ef94c-123">The resource name.</span></span>

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

### <span data-ttu-id="ef94c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef94c-124">-PassThru</span></span>
<span data-ttu-id="ef94c-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ef94c-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef94c-126">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ef94c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef94c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef94c-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef94c-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef94c-128">The resource group name.</span></span>

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

### <span data-ttu-id="ef94c-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ef94c-129">-ResourceId</span></span>
<span data-ttu-id="ef94c-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ef94c-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ef94c-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef94c-131">-Confirm</span></span>
<span data-ttu-id="ef94c-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef94c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef94c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef94c-133">-WhatIf</span></span>
<span data-ttu-id="ef94c-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef94c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef94c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef94c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef94c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef94c-136">CommonParameters</span></span>
<span data-ttu-id="ef94c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef94c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef94c-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef94c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef94c-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef94c-139">INPUTS</span></span>

### <span data-ttu-id="ef94c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ef94c-140">System.String</span></span>

## <span data-ttu-id="ef94c-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef94c-141">OUTPUTS</span></span>

### <span data-ttu-id="ef94c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef94c-142">System.Boolean</span></span>

## <span data-ttu-id="ef94c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef94c-143">NOTES</span></span>

## <span data-ttu-id="ef94c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef94c-144">RELATED LINKS</span></span>
