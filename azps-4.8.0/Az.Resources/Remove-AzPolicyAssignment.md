---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165651"
---
# <span data-ttu-id="2fc46-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fc46-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="2fc46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fc46-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc46-103">Entfernt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="2fc46-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="2fc46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fc46-104">SYNTAX</span></span>

### <span data-ttu-id="2fc46-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fc46-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc46-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fc46-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc46-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fc46-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc46-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fc46-108">DESCRIPTION</span></span>
<span data-ttu-id="2fc46-109">Das Cmdlet **Remove-AzPolicyAssignment** entfernt die angegebene Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="2fc46-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="2fc46-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fc46-110">EXAMPLES</span></span>

### <span data-ttu-id="2fc46-111">Beispiel 1: Entfernen der Richtlinienzuweisung nach Name und Bereich</span><span class="sxs-lookup"><span data-stu-id="2fc46-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="2fc46-112">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="2fc46-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="2fc46-113">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="2fc46-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2fc46-114">Der zweite Befehl entfernt die Richtlinienzuweisung mit dem Namen PolicyAssignment07, die auf einer Ressourcengruppen Ebene zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="2fc46-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="2fc46-115">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2fc46-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="2fc46-116">Beispiel 2: Entfernen der Richtlinienzuweisung nach ID</span><span class="sxs-lookup"><span data-stu-id="2fc46-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="2fc46-117">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="2fc46-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2fc46-118">Der zweite Befehl ruft die Richtlinienzuweisung auf einer Ressourcengruppen Ebene ab und speichert Sie dann in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="2fc46-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="2fc46-119">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2fc46-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="2fc46-120">Mit dem letzten Befehl wird die Richtlinienzuweisung entfernt, die von der Eigenschaft " **Resourcen** " von $PolicyAssignment identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2fc46-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="2fc46-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fc46-121">PARAMETERS</span></span>

### <span data-ttu-id="2fc46-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2fc46-122">-ApiVersion</span></span>
<span data-ttu-id="2fc46-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="2fc46-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2fc46-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="2fc46-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc46-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc46-125">-DefaultProfile</span></span>
<span data-ttu-id="2fc46-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2fc46-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fc46-127">-ID</span><span class="sxs-lookup"><span data-stu-id="2fc46-127">-Id</span></span>
<span data-ttu-id="2fc46-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="2fc46-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc46-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2fc46-129">-InputObject</span></span>
<span data-ttu-id="2fc46-130">Das zu entfernende Richtlinien Zuordnungsobjekt, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2fc46-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc46-131">-Name</span><span class="sxs-lookup"><span data-stu-id="2fc46-131">-Name</span></span>
<span data-ttu-id="2fc46-132">Gibt den Namen der Richtlinien Aufgabe an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2fc46-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc46-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="2fc46-133">-Pre</span></span>
<span data-ttu-id="2fc46-134">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2fc46-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2fc46-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="2fc46-135">-Scope</span></span>
<span data-ttu-id="2fc46-136">Gibt den Bereich an, auf dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2fc46-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc46-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fc46-137">-Confirm</span></span>
<span data-ttu-id="2fc46-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fc46-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fc46-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc46-139">-WhatIf</span></span>
<span data-ttu-id="2fc46-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fc46-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc46-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fc46-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fc46-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc46-142">CommonParameters</span></span>
<span data-ttu-id="2fc46-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc46-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc46-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fc46-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc46-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fc46-145">INPUTS</span></span>

### <span data-ttu-id="2fc46-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2fc46-146">System.String</span></span>

## <span data-ttu-id="2fc46-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fc46-147">OUTPUTS</span></span>

### <span data-ttu-id="2fc46-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2fc46-148">System.Boolean</span></span>

## <span data-ttu-id="2fc46-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fc46-149">NOTES</span></span>

## <span data-ttu-id="2fc46-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fc46-150">RELATED LINKS</span></span>

[<span data-ttu-id="2fc46-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fc46-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="2fc46-152">Neu – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fc46-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="2fc46-153">Satz-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2fc46-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


