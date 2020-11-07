---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 9a238515b0482b36dcebd3bdcdf6976aebc64448
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664448"
---
# <span data-ttu-id="f7078-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f7078-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="f7078-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7078-102">SYNOPSIS</span></span>
<span data-ttu-id="f7078-103">Entfernt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="f7078-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7078-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7078-104">SYNTAX</span></span>

### <span data-ttu-id="f7078-105">Der Parametersatz für den Richtlinien Zuordnungsnamen.</span><span class="sxs-lookup"><span data-stu-id="f7078-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="f7078-106">Standard</span><span class="sxs-lookup"><span data-stu-id="f7078-106">(Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7078-107">Der Parametersatz für die Richtlinien Zuweisungs-ID.</span><span class="sxs-lookup"><span data-stu-id="f7078-107">The policy assignment Id parameter set.</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7078-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7078-108">DESCRIPTION</span></span>
<span data-ttu-id="f7078-109">Das Cmdlet **Remove-AzureRmPolicyAssignment** entfernt die angegebene Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="f7078-109">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="f7078-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7078-110">EXAMPLES</span></span>

### <span data-ttu-id="f7078-111">Beispiel 1: Entfernen der Richtlinienzuweisung nach Name und Bereich</span><span class="sxs-lookup"><span data-stu-id="f7078-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="f7078-112">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f7078-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="f7078-113">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="f7078-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f7078-114">Der zweite Befehl entfernt die Richtlinienzuweisung mit dem Namen PolicyAssignment07, die auf einer Ressourcengruppen Ebene zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="f7078-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="f7078-115">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7078-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="f7078-116">Beispiel 2: Entfernen der Richtlinienzuweisung nach ID</span><span class="sxs-lookup"><span data-stu-id="f7078-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="f7078-117">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="f7078-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f7078-118">Der zweite Befehl ruft die Richtlinienzuweisung auf einer Ressourcengruppen Ebene ab und speichert Sie dann in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="f7078-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="f7078-119">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7078-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="f7078-120">Mit dem letzten Befehl wird die Richtlinienzuweisung entfernt, die von der Eigenschaft " **Resourcen** " von $PolicyAssignment identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f7078-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="f7078-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7078-121">PARAMETERS</span></span>

### <span data-ttu-id="f7078-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f7078-122">-ApiVersion</span></span>
<span data-ttu-id="f7078-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="f7078-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f7078-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="f7078-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f7078-125">-ID</span><span class="sxs-lookup"><span data-stu-id="f7078-125">-Id</span></span>
<span data-ttu-id="f7078-126">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="f7078-126">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7078-127">-Information</span><span class="sxs-lookup"><span data-stu-id="f7078-127">-InformationAction</span></span>
<span data-ttu-id="f7078-128">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="f7078-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f7078-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f7078-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7078-130">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="f7078-130">Continue</span></span>
- <span data-ttu-id="f7078-131">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="f7078-131">Ignore</span></span>
- <span data-ttu-id="f7078-132">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="f7078-132">Inquire</span></span>
- <span data-ttu-id="f7078-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f7078-133">SilentlyContinue</span></span>
- <span data-ttu-id="f7078-134">Beenden</span><span class="sxs-lookup"><span data-stu-id="f7078-134">Stop</span></span>
- <span data-ttu-id="f7078-135">Anhalten</span><span class="sxs-lookup"><span data-stu-id="f7078-135">Suspend</span></span>

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

### <span data-ttu-id="f7078-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f7078-136">-InformationVariable</span></span>
<span data-ttu-id="f7078-137">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="f7078-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f7078-138">-Name</span><span class="sxs-lookup"><span data-stu-id="f7078-138">-Name</span></span>
<span data-ttu-id="f7078-139">Gibt den Namen der Richtlinien Aufgabe an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f7078-139">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7078-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="f7078-140">-Pre</span></span>
<span data-ttu-id="f7078-141">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f7078-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f7078-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="f7078-142">-Scope</span></span>
<span data-ttu-id="f7078-143">Gibt den Bereich an, auf dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7078-143">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7078-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7078-144">-Confirm</span></span>
<span data-ttu-id="f7078-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7078-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7078-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7078-146">-WhatIf</span></span>
<span data-ttu-id="f7078-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7078-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7078-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7078-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7078-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7078-149">-DefaultProfile</span></span>
<span data-ttu-id="f7078-150">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7078-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7078-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7078-151">CommonParameters</span></span>
<span data-ttu-id="f7078-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7078-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7078-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7078-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7078-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7078-154">INPUTS</span></span>

## <span data-ttu-id="f7078-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7078-155">OUTPUTS</span></span>

### <span data-ttu-id="f7078-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7078-156">System.Boolean</span></span>

## <span data-ttu-id="f7078-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7078-157">NOTES</span></span>

## <span data-ttu-id="f7078-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7078-158">RELATED LINKS</span></span>

[<span data-ttu-id="f7078-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f7078-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f7078-160">Neu – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f7078-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f7078-161">Satz-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f7078-161">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


