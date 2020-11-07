---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: 8cd1ee1d8f32bd203e9fb2d8ac5d75c2d6b2938d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843244"
---
# <span data-ttu-id="61eed-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61eed-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="61eed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61eed-102">SYNOPSIS</span></span>
<span data-ttu-id="61eed-103">Entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="61eed-103">Removes a policy definition.</span></span>

## <span data-ttu-id="61eed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61eed-104">SYNTAX</span></span>

### <span data-ttu-id="61eed-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="61eed-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61eed-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eed-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61eed-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eed-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61eed-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61eed-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61eed-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61eed-109">DESCRIPTION</span></span>
<span data-ttu-id="61eed-110">Das Cmdlet **Remove-AzPolicyDefinition** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="61eed-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="61eed-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61eed-111">EXAMPLES</span></span>

### <span data-ttu-id="61eed-112">Beispiel 1: Entfernen der Richtliniendefinition nach Name</span><span class="sxs-lookup"><span data-stu-id="61eed-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="61eed-113">Mit diesem Befehl wird die angegebene Richtliniendefinition entfernt.</span><span class="sxs-lookup"><span data-stu-id="61eed-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="61eed-114">Beispiel 2: Entfernen der Richtliniendefinition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="61eed-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="61eed-115">Der erste Befehl ruft mithilfe des Get-AzPolicyDefinition-Cmdlets eine Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="61eed-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="61eed-116">Der Befehl speichert Sie in der $PolicyDefinition-Variablen.</span><span class="sxs-lookup"><span data-stu-id="61eed-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="61eed-117">Mit dem zweiten Befehl wird die Richtliniendefinition entfernt, die durch die Eigenschaft " **Resourcen** " von $PolicyDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="61eed-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="61eed-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="61eed-118">PARAMETERS</span></span>

### <span data-ttu-id="61eed-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="61eed-119">-ApiVersion</span></span>
<span data-ttu-id="61eed-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="61eed-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="61eed-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="61eed-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="61eed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61eed-122">-DefaultProfile</span></span>
<span data-ttu-id="61eed-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="61eed-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61eed-124">-Force</span><span class="sxs-lookup"><span data-stu-id="61eed-124">-Force</span></span>
<span data-ttu-id="61eed-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="61eed-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61eed-126">-ID</span><span class="sxs-lookup"><span data-stu-id="61eed-126">-Id</span></span>
<span data-ttu-id="61eed-127">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="61eed-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="61eed-128">-Information</span><span class="sxs-lookup"><span data-stu-id="61eed-128">-InformationAction</span></span>
<span data-ttu-id="61eed-129">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="61eed-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="61eed-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="61eed-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="61eed-131">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="61eed-131">Continue</span></span>
- <span data-ttu-id="61eed-132">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="61eed-132">Ignore</span></span>
- <span data-ttu-id="61eed-133">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="61eed-133">Inquire</span></span>
- <span data-ttu-id="61eed-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="61eed-134">SilentlyContinue</span></span>
- <span data-ttu-id="61eed-135">Beenden</span><span class="sxs-lookup"><span data-stu-id="61eed-135">Stop</span></span>
- <span data-ttu-id="61eed-136">Anhalten</span><span class="sxs-lookup"><span data-stu-id="61eed-136">Suspend</span></span>

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

### <span data-ttu-id="61eed-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="61eed-137">-InformationVariable</span></span>
<span data-ttu-id="61eed-138">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="61eed-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="61eed-139">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="61eed-139">-ManagementGroupName</span></span>
<span data-ttu-id="61eed-140">Der Name der Verwaltungsgruppe der zu löschenden Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="61eed-140">The name of the management group of the policy definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61eed-141">-Name</span><span class="sxs-lookup"><span data-stu-id="61eed-141">-Name</span></span>
<span data-ttu-id="61eed-142">Gibt den Namen der Richtliniendefinition an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="61eed-142">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61eed-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="61eed-143">-Pre</span></span>
<span data-ttu-id="61eed-144">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="61eed-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="61eed-145">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="61eed-145">-SubscriptionId</span></span>
<span data-ttu-id="61eed-146">Die Abonnement-ID der Richtliniendefinition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="61eed-146">The subscription ID of the policy definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61eed-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61eed-147">-Confirm</span></span>
<span data-ttu-id="61eed-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61eed-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61eed-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61eed-149">-WhatIf</span></span>
<span data-ttu-id="61eed-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61eed-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61eed-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61eed-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61eed-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61eed-152">CommonParameters</span></span>
<span data-ttu-id="61eed-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61eed-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61eed-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61eed-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61eed-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61eed-155">INPUTS</span></span>

## <span data-ttu-id="61eed-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61eed-156">OUTPUTS</span></span>

## <span data-ttu-id="61eed-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="61eed-157">NOTES</span></span>

## <span data-ttu-id="61eed-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61eed-158">RELATED LINKS</span></span>

[<span data-ttu-id="61eed-159">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61eed-159">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="61eed-160">Neu – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61eed-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="61eed-161">Satz-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61eed-161">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


