---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145996"
---
# <span data-ttu-id="aeef0-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aeef0-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="aeef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeef0-102">SYNOPSIS</span></span>
<span data-ttu-id="aeef0-103">Entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="aeef0-103">Removes a policy definition.</span></span>

## <span data-ttu-id="aeef0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aeef0-104">SYNTAX</span></span>

### <span data-ttu-id="aeef0-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aeef0-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeef0-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeef0-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeef0-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeef0-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeef0-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeef0-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeef0-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeef0-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeef0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aeef0-110">DESCRIPTION</span></span>
<span data-ttu-id="aeef0-111">Das **Cmdlet "Remove-AzPolicyDefinition"** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="aeef0-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="aeef0-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aeef0-112">EXAMPLES</span></span>

### <span data-ttu-id="aeef0-113">Beispiel 1: Entfernen der Richtliniendefinition nach Name</span><span class="sxs-lookup"><span data-stu-id="aeef0-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="aeef0-114">Mit diesem Befehl wird die angegebene Richtliniendefinition entfernt.</span><span class="sxs-lookup"><span data-stu-id="aeef0-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="aeef0-115">Beispiel 2: Entfernen der Richtliniendefinition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="aeef0-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="aeef0-116">Der erste Befehl ruft eine Richtliniendefinition namens VMPolicyDefinition mithilfe des Get-AzPolicyDefinition cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="aeef0-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="aeef0-117">Der Befehl speichert sie in der $PolicyDefinition Variable.</span><span class="sxs-lookup"><span data-stu-id="aeef0-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="aeef0-118">Mit dem zweiten Befehl wird die Richtliniendefinition entfernt, die durch die **Eigenschaft "ResourceId"** der $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="aeef0-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="aeef0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aeef0-119">PARAMETERS</span></span>

### <span data-ttu-id="aeef0-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aeef0-120">-ApiVersion</span></span>
<span data-ttu-id="aeef0-121">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="aeef0-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="aeef0-122">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="aeef0-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="aeef0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeef0-123">-DefaultProfile</span></span>
<span data-ttu-id="aeef0-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aeef0-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeef0-125">-Force</span><span class="sxs-lookup"><span data-stu-id="aeef0-125">-Force</span></span>
<span data-ttu-id="aeef0-126">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="aeef0-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aeef0-127">-ID</span><span class="sxs-lookup"><span data-stu-id="aeef0-127">-Id</span></span>
<span data-ttu-id="aeef0-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="aeef0-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aeef0-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aeef0-129">-InputObject</span></span>
<span data-ttu-id="aeef0-130">Das Richtliniendefinitionsobjekt, das entfernt werden soll, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="aeef0-130">The policy definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aeef0-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="aeef0-131">-ManagementGroupName</span></span>
<span data-ttu-id="aeef0-132">Der Name der Verwaltungsgruppe der zu löschende Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="aeef0-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="aeef0-133">-Name</span><span class="sxs-lookup"><span data-stu-id="aeef0-133">-Name</span></span>
<span data-ttu-id="aeef0-134">Gibt den Namen der Richtliniendefinition an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="aeef0-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aeef0-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="aeef0-135">-Pre</span></span>
<span data-ttu-id="aeef0-136">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aeef0-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aeef0-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aeef0-137">-SubscriptionId</span></span>
<span data-ttu-id="aeef0-138">Die Abonnement-ID der zu löschende Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="aeef0-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="aeef0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aeef0-139">-Confirm</span></span>
<span data-ttu-id="aeef0-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aeef0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeef0-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aeef0-141">-WhatIf</span></span>
<span data-ttu-id="aeef0-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aeef0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeef0-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aeef0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeef0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeef0-144">CommonParameters</span></span>
<span data-ttu-id="aeef0-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeef0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeef0-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aeef0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeef0-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aeef0-147">INPUTS</span></span>

### <span data-ttu-id="aeef0-148">System.String</span><span class="sxs-lookup"><span data-stu-id="aeef0-148">System.String</span></span>

### <span data-ttu-id="aeef0-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aeef0-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aeef0-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aeef0-150">OUTPUTS</span></span>

### <span data-ttu-id="aeef0-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aeef0-151">System.Boolean</span></span>

## <span data-ttu-id="aeef0-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aeef0-152">NOTES</span></span>

## <span data-ttu-id="aeef0-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aeef0-153">RELATED LINKS</span></span>

[<span data-ttu-id="aeef0-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aeef0-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="aeef0-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aeef0-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="aeef0-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="aeef0-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


