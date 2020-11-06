---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: d78cf9d28c453626c26656b9f9280f5c52695434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482733"
---
# <span data-ttu-id="8fdc8-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8fdc8-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="8fdc8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fdc8-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdc8-103">Entfernt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fdc8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fdc8-104">SYNTAX</span></span>

### <span data-ttu-id="8fdc8-105">RemoveByPolicyAssignmentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8fdc8-105">RemoveByPolicyAssignmentName (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fdc8-106">RemoveByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="8fdc8-106">RemoveByPolicyAssignmentId</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fdc8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fdc8-107">DESCRIPTION</span></span>
<span data-ttu-id="8fdc8-108">Das Cmdlet **Remove-AzureRmPolicyAssignment** entfernt die angegebene Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="8fdc8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fdc8-109">EXAMPLES</span></span>

### <span data-ttu-id="8fdc8-110">Beispiel 1: Entfernen der Richtlinienzuweisung nach Name und Bereich</span><span class="sxs-lookup"><span data-stu-id="8fdc8-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="8fdc8-111">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="8fdc8-112">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-112">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="8fdc8-113">Der zweite Befehl entfernt die Richtlinienzuweisung mit dem Namen PolicyAssignment07, die auf einer Ressourcengruppen Ebene zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="8fdc8-114">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="8fdc8-115">Beispiel 2: Entfernen der Richtlinienzuweisung nach ID</span><span class="sxs-lookup"><span data-stu-id="8fdc8-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="8fdc8-116">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="8fdc8-117">Der zweite Befehl ruft die Richtlinienzuweisung auf einer Ressourcengruppen Ebene ab und speichert Sie dann in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="8fdc8-118">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="8fdc8-119">Mit dem letzten Befehl wird die Richtlinienzuweisung entfernt, die von der Eigenschaft " **Resourcen** " von $PolicyAssignment identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="8fdc8-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fdc8-120">PARAMETERS</span></span>

### <span data-ttu-id="8fdc8-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8fdc8-121">-ApiVersion</span></span>
<span data-ttu-id="8fdc8-122">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8fdc8-123">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdc8-124">-DefaultProfile</span></span>
<span data-ttu-id="8fdc8-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8fdc8-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc8-126">-ID</span><span class="sxs-lookup"><span data-stu-id="8fdc8-126">-Id</span></span>
<span data-ttu-id="8fdc8-127">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc8-128">-Information</span><span class="sxs-lookup"><span data-stu-id="8fdc8-128">-InformationAction</span></span>
<span data-ttu-id="8fdc8-129">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8fdc8-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8fdc8-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8fdc8-131">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8fdc8-131">Continue</span></span>
- <span data-ttu-id="8fdc8-132">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8fdc8-132">Ignore</span></span>
- <span data-ttu-id="8fdc8-133">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8fdc8-133">Inquire</span></span>
- <span data-ttu-id="8fdc8-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8fdc8-134">SilentlyContinue</span></span>
- <span data-ttu-id="8fdc8-135">Beenden</span><span class="sxs-lookup"><span data-stu-id="8fdc8-135">Stop</span></span>
- <span data-ttu-id="8fdc8-136">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8fdc8-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc8-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8fdc8-137">-InformationVariable</span></span>
<span data-ttu-id="8fdc8-138">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc8-139">-Name</span><span class="sxs-lookup"><span data-stu-id="8fdc8-139">-Name</span></span>
<span data-ttu-id="8fdc8-140">Gibt den Namen der Richtlinien Aufgabe an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc8-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="8fdc8-141">-Pre</span></span>
<span data-ttu-id="8fdc8-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8fdc8-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="8fdc8-143">-Scope</span></span>
<span data-ttu-id="8fdc8-144">Gibt den Bereich an, auf dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc8-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8fdc8-145">-Confirm</span></span>
<span data-ttu-id="8fdc8-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fdc8-147">-WhatIf</span></span>
<span data-ttu-id="8fdc8-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fdc8-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdc8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdc8-150">CommonParameters</span></span>
<span data-ttu-id="8fdc8-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdc8-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fdc8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdc8-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fdc8-153">INPUTS</span></span>

### <span data-ttu-id="8fdc8-154">Keine</span><span class="sxs-lookup"><span data-stu-id="8fdc8-154">None</span></span>
<span data-ttu-id="8fdc8-155">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8fdc8-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fdc8-156">OUTPUTS</span></span>

### <span data-ttu-id="8fdc8-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8fdc8-157">System.Boolean</span></span>

## <span data-ttu-id="8fdc8-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fdc8-158">NOTES</span></span>

## <span data-ttu-id="8fdc8-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fdc8-159">RELATED LINKS</span></span>

[<span data-ttu-id="8fdc8-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8fdc8-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="8fdc8-161">Neu – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8fdc8-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="8fdc8-162">Satz-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="8fdc8-162">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


