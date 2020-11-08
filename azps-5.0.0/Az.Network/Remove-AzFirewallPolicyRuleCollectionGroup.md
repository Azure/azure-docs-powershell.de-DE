---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 3c9b307b34d07ff6c9331dc8d72c1149c83ef374
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176297"
---
# <span data-ttu-id="d4fde-101">Remove-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="d4fde-101">Remove-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="d4fde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4fde-102">SYNOPSIS</span></span>
<span data-ttu-id="d4fde-103">Entfernt eine Azure Firewall-Richtlinienregel Sammlungs Gruppe in einer Azure Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d4fde-103">Removes a Azure Firewall Policy Rule Collection Group in a Azure firewall policy</span></span>

## <span data-ttu-id="d4fde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4fde-104">SYNTAX</span></span>

### <span data-ttu-id="d4fde-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4fde-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4fde-106">RemoveByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4fde-106">RemoveByParentInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4fde-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4fde-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4fde-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4fde-108">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4fde-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4fde-109">DESCRIPTION</span></span>
<span data-ttu-id="d4fde-110">Das Cmdlet " **Remove-AzFirewallPolicyRuleCollectionGroup** " entfernt eine Regel Sammlungs Gruppe aus einer Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d4fde-110">The **Remove-AzFirewallPolicyRuleCollectionGroup** cmdlet removes a rule collection group from an Azure Firewall Policy.</span></span>

## <span data-ttu-id="d4fde-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4fde-111">EXAMPLES</span></span>

### <span data-ttu-id="d4fde-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4fde-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -FirewallPolicyObject $fp
```

<span data-ttu-id="d4fde-113">In diesem Beispiel wird die Firewall-Richtlinienregel Colelction Gruppe mit dem Namen "testRcGroup" im Firewall-Richtlinienobjekt entfernt $FP</span><span class="sxs-lookup"><span data-stu-id="d4fde-113">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall policy object $fp</span></span>

### <span data-ttu-id="d4fde-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d4fde-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicyRuleCollectionGroup -Name testRcGroup -ResourceGroupName testRg -AzureFirewallPolicyName fpName 
```

<span data-ttu-id="d4fde-115">In diesem Beispiel wird die Firewall-Richtlinienregel Colelction Gruppe mit dem Namen "testRcGroup" in der Firewall namens "fpName" frpm der Namen der ResourceGroup "testRg" entfernt</span><span class="sxs-lookup"><span data-stu-id="d4fde-115">This example removes the firewall policy rule colelction group named "testRcGroup" in the firewall named "fpName" frpm the resourcegroup names "testRg"</span></span>

## <span data-ttu-id="d4fde-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4fde-116">PARAMETERS</span></span>

### <span data-ttu-id="d4fde-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4fde-117">-AsJob</span></span>
<span data-ttu-id="d4fde-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d4fde-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4fde-119">-DefaultProfile</span></span>
<span data-ttu-id="d4fde-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4fde-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-121">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="d4fde-121">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="d4fde-122">Der Name der Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d4fde-122">The name of the firewall policy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-123">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d4fde-123">-FirewallPolicyObject</span></span>
<span data-ttu-id="d4fde-124">Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d4fde-124">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d4fde-125">-Force</span></span>
<span data-ttu-id="d4fde-126">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="d4fde-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4fde-127">-InputObject</span></span>
<span data-ttu-id="d4fde-128">Gruppenobjekt für Firewall-Richtlinienregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="d4fde-128">Firewall Policy Rule collection group object</span></span>

```yaml
Type: PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d4fde-129">-Name</span></span>
<span data-ttu-id="d4fde-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d4fde-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RemoveByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4fde-131">-PassThru</span></span>
<span data-ttu-id="d4fde-132">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4fde-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d4fde-133">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="d4fde-133">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4fde-134">-ResourceGroupName</span></span>
<span data-ttu-id="d4fde-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4fde-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d4fde-136">-ResourceId</span></span>
<span data-ttu-id="d4fde-137">Die Ressourcen-ID der Regel Sammlungs Gruppe</span><span class="sxs-lookup"><span data-stu-id="d4fde-137">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4fde-138">-Confirm</span></span>
<span data-ttu-id="d4fde-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4fde-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4fde-140">-WhatIf</span></span>
<span data-ttu-id="d4fde-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4fde-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4fde-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4fde-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4fde-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4fde-143">CommonParameters</span></span>
<span data-ttu-id="d4fde-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4fde-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4fde-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4fde-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4fde-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4fde-146">INPUTS</span></span>

### <span data-ttu-id="d4fde-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d4fde-147">System.String</span></span>

### <span data-ttu-id="d4fde-148">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d4fde-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="d4fde-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroupWrapper</span><span class="sxs-lookup"><span data-stu-id="d4fde-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper</span></span>

## <span data-ttu-id="d4fde-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4fde-150">OUTPUTS</span></span>

### <span data-ttu-id="d4fde-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4fde-151">System.Boolean</span></span>

## <span data-ttu-id="d4fde-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4fde-152">NOTES</span></span>

## <span data-ttu-id="d4fde-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4fde-153">RELATED LINKS</span></span>
