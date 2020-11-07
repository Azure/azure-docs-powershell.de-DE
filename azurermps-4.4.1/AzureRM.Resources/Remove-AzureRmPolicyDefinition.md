---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 46323b260330ca84ee1ac2426ee7b6e2ab474f21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664445"
---
# <span data-ttu-id="66fa4-101">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66fa4-101">Remove-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="66fa4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="66fa4-103">Entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="66fa4-103">Removes a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66fa4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66fa4-104">SYNTAX</span></span>

### <span data-ttu-id="66fa4-105">Der Parametersatz für den Richtlinien Definitionsnamen.</span><span class="sxs-lookup"><span data-stu-id="66fa4-105">The policy definition name parameter set.</span></span> <span data-ttu-id="66fa4-106">Standard</span><span class="sxs-lookup"><span data-stu-id="66fa4-106">(Default)</span></span>
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66fa4-107">Der Parametersatz für die Richtlinien Definitions-ID.</span><span class="sxs-lookup"><span data-stu-id="66fa4-107">The policy definition Id parameter set.</span></span>
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66fa4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66fa4-108">DESCRIPTION</span></span>
<span data-ttu-id="66fa4-109">Das Cmdlet **Remove-AzureRmPolicyDefinition** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="66fa4-109">The **Remove-AzureRmPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="66fa4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66fa4-110">EXAMPLES</span></span>

### <span data-ttu-id="66fa4-111">Beispiel 1: Entfernen der Richtliniendefinition nach Name</span><span class="sxs-lookup"><span data-stu-id="66fa4-111">Example 1: Remove the policy definition by name</span></span>
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="66fa4-112">Mit diesem Befehl wird die angegebene Richtliniendefinition entfernt.</span><span class="sxs-lookup"><span data-stu-id="66fa4-112">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="66fa4-113">Beispiel 2: Entfernen der Richtliniendefinition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="66fa4-113">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="66fa4-114">Der erste Befehl ruft mithilfe des Get-AzureRmPolicyDefinition-Cmdlets eine Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="66fa4-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="66fa4-115">Der Befehl speichert Sie in der $PolicyDefinition-Variablen.</span><span class="sxs-lookup"><span data-stu-id="66fa4-115">The command stores it in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="66fa4-116">Mit dem zweiten Befehl wird die Richtliniendefinition entfernt, die durch die Eigenschaft " **Resourcen** " von $PolicyDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="66fa4-116">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="66fa4-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="66fa4-117">PARAMETERS</span></span>

### <span data-ttu-id="66fa4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66fa4-118">-ApiVersion</span></span>
<span data-ttu-id="66fa4-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="66fa4-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="66fa4-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="66fa4-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="66fa4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="66fa4-121">-Force</span></span>
<span data-ttu-id="66fa4-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="66fa4-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66fa4-123">-ID</span><span class="sxs-lookup"><span data-stu-id="66fa4-123">-Id</span></span>
<span data-ttu-id="66fa4-124">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="66fa4-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66fa4-125">-Information</span><span class="sxs-lookup"><span data-stu-id="66fa4-125">-InformationAction</span></span>
<span data-ttu-id="66fa4-126">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="66fa4-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="66fa4-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="66fa4-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66fa4-128">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="66fa4-128">Continue</span></span>
- <span data-ttu-id="66fa4-129">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="66fa4-129">Ignore</span></span>
- <span data-ttu-id="66fa4-130">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="66fa4-130">Inquire</span></span>
- <span data-ttu-id="66fa4-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="66fa4-131">SilentlyContinue</span></span>
- <span data-ttu-id="66fa4-132">Beenden</span><span class="sxs-lookup"><span data-stu-id="66fa4-132">Stop</span></span>
- <span data-ttu-id="66fa4-133">Anhalten</span><span class="sxs-lookup"><span data-stu-id="66fa4-133">Suspend</span></span>

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

### <span data-ttu-id="66fa4-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="66fa4-134">-InformationVariable</span></span>
<span data-ttu-id="66fa4-135">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="66fa4-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="66fa4-136">-Name</span><span class="sxs-lookup"><span data-stu-id="66fa4-136">-Name</span></span>
<span data-ttu-id="66fa4-137">Gibt den Namen der Richtliniendefinition an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="66fa4-137">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66fa4-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="66fa4-138">-Pre</span></span>
<span data-ttu-id="66fa4-139">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="66fa4-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="66fa4-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66fa4-140">-Confirm</span></span>
<span data-ttu-id="66fa4-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66fa4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66fa4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66fa4-142">-WhatIf</span></span>
<span data-ttu-id="66fa4-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66fa4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66fa4-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66fa4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66fa4-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fa4-145">-DefaultProfile</span></span>
<span data-ttu-id="66fa4-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66fa4-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66fa4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fa4-147">CommonParameters</span></span>
<span data-ttu-id="66fa4-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fa4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fa4-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66fa4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fa4-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66fa4-150">INPUTS</span></span>

## <span data-ttu-id="66fa4-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66fa4-151">OUTPUTS</span></span>

### <span data-ttu-id="66fa4-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66fa4-152">System.Boolean</span></span>

## <span data-ttu-id="66fa4-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="66fa4-153">NOTES</span></span>

## <span data-ttu-id="66fa4-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66fa4-154">RELATED LINKS</span></span>

[<span data-ttu-id="66fa4-155">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66fa4-155">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="66fa4-156">Neu – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66fa4-156">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="66fa4-157">Satz-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="66fa4-157">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


