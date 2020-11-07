---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 8fbf6c16dce1f8d96dcc9546c801e389493e7bcd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843255"
---
# <span data-ttu-id="1105d-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1105d-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="1105d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1105d-102">SYNOPSIS</span></span>
<span data-ttu-id="1105d-103">Entfernt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="1105d-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="1105d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1105d-104">SYNTAX</span></span>

### <span data-ttu-id="1105d-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1105d-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1105d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1105d-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1105d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1105d-107">DESCRIPTION</span></span>
<span data-ttu-id="1105d-108">Das Cmdlet **Remove-AzPolicyAssignment** entfernt die angegebene Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="1105d-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="1105d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1105d-109">EXAMPLES</span></span>

### <span data-ttu-id="1105d-110">Beispiel 1: Entfernen der Richtlinienzuweisung nach Name und Bereich</span><span class="sxs-lookup"><span data-stu-id="1105d-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="1105d-111">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="1105d-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1105d-112">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="1105d-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1105d-113">Der zweite Befehl entfernt die Richtlinienzuweisung mit dem Namen PolicyAssignment07, die auf einer Ressourcengruppen Ebene zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="1105d-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="1105d-114">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1105d-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="1105d-115">Beispiel 2: Entfernen der Richtlinienzuweisung nach ID</span><span class="sxs-lookup"><span data-stu-id="1105d-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="1105d-116">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="1105d-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1105d-117">Der zweite Befehl ruft die Richtlinienzuweisung auf einer Ressourcengruppen Ebene ab und speichert Sie dann in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="1105d-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1105d-118">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1105d-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="1105d-119">Mit dem letzten Befehl wird die Richtlinienzuweisung entfernt, die von der Eigenschaft " **Resourcen** " von $PolicyAssignment identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="1105d-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="1105d-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1105d-120">PARAMETERS</span></span>

### <span data-ttu-id="1105d-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1105d-121">-ApiVersion</span></span>
<span data-ttu-id="1105d-122">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="1105d-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1105d-123">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="1105d-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1105d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1105d-124">-DefaultProfile</span></span>
<span data-ttu-id="1105d-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1105d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1105d-126">-ID</span><span class="sxs-lookup"><span data-stu-id="1105d-126">-Id</span></span>
<span data-ttu-id="1105d-127">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="1105d-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1105d-128">-Information</span><span class="sxs-lookup"><span data-stu-id="1105d-128">-InformationAction</span></span>
<span data-ttu-id="1105d-129">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="1105d-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="1105d-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1105d-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1105d-131">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="1105d-131">Continue</span></span>
- <span data-ttu-id="1105d-132">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="1105d-132">Ignore</span></span>
- <span data-ttu-id="1105d-133">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="1105d-133">Inquire</span></span>
- <span data-ttu-id="1105d-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1105d-134">SilentlyContinue</span></span>
- <span data-ttu-id="1105d-135">Beenden</span><span class="sxs-lookup"><span data-stu-id="1105d-135">Stop</span></span>
- <span data-ttu-id="1105d-136">Anhalten</span><span class="sxs-lookup"><span data-stu-id="1105d-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1105d-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1105d-137">-InformationVariable</span></span>
<span data-ttu-id="1105d-138">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="1105d-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1105d-139">-Name</span><span class="sxs-lookup"><span data-stu-id="1105d-139">-Name</span></span>
<span data-ttu-id="1105d-140">Gibt den Namen der Richtlinien Aufgabe an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1105d-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1105d-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="1105d-141">-Pre</span></span>
<span data-ttu-id="1105d-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1105d-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1105d-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="1105d-143">-Scope</span></span>
<span data-ttu-id="1105d-144">Gibt den Bereich an, auf dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1105d-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="1105d-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1105d-145">-Confirm</span></span>
<span data-ttu-id="1105d-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1105d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1105d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1105d-147">-WhatIf</span></span>
<span data-ttu-id="1105d-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1105d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1105d-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1105d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1105d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1105d-150">CommonParameters</span></span>
<span data-ttu-id="1105d-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1105d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1105d-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1105d-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1105d-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1105d-153">INPUTS</span></span>

## <span data-ttu-id="1105d-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1105d-154">OUTPUTS</span></span>

## <span data-ttu-id="1105d-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="1105d-155">NOTES</span></span>

## <span data-ttu-id="1105d-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1105d-156">RELATED LINKS</span></span>

[<span data-ttu-id="1105d-157">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1105d-157">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="1105d-158">Neu – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1105d-158">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="1105d-159">Satz-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1105d-159">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


