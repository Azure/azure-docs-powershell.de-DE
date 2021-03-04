---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: a65892efce36490d256c99935f6cbe8a96f5ff98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937400"
---
# <span data-ttu-id="fac16-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fac16-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="fac16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fac16-102">SYNOPSIS</span></span>
<span data-ttu-id="fac16-103">Entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="fac16-103">Removes a policy definition.</span></span>

## <span data-ttu-id="fac16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fac16-104">SYNTAX</span></span>

### <span data-ttu-id="fac16-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fac16-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac16-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fac16-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac16-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fac16-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac16-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fac16-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac16-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fac16-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fac16-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fac16-110">DESCRIPTION</span></span>
<span data-ttu-id="fac16-111">Das **Cmdlet Remove-AzPolicyDefinition** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="fac16-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="fac16-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fac16-112">EXAMPLES</span></span>

### <span data-ttu-id="fac16-113">Beispiel 1: Entfernen der Richtliniendefinition nach Name</span><span class="sxs-lookup"><span data-stu-id="fac16-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="fac16-114">Mit diesem Befehl wird die angegebene Richtliniendefinition entfernt.</span><span class="sxs-lookup"><span data-stu-id="fac16-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="fac16-115">Beispiel 2: Entfernen der Richtliniendefinition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fac16-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="fac16-116">Der erste Befehl ruft eine Richtliniendefinition namens VMPolicyDefinition mithilfe des cmdlets Get-AzPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="fac16-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="fac16-117">Der Befehl speichert ihn in der $PolicyDefinition-Variable.</span><span class="sxs-lookup"><span data-stu-id="fac16-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="fac16-118">Mit dem zweiten Befehl wird die Richtliniendefinition entfernt, die durch die **ResourceId-Eigenschaft** von $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="fac16-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="fac16-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fac16-119">PARAMETERS</span></span>

### <span data-ttu-id="fac16-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fac16-120">-ApiVersion</span></span>
<span data-ttu-id="fac16-121">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="fac16-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fac16-122">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="fac16-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fac16-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac16-123">-DefaultProfile</span></span>
<span data-ttu-id="fac16-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fac16-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fac16-125">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="fac16-125">-Force</span></span>
<span data-ttu-id="fac16-126">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="fac16-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fac16-127">-ID</span><span class="sxs-lookup"><span data-stu-id="fac16-127">-Id</span></span>
<span data-ttu-id="fac16-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="fac16-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fac16-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fac16-129">-InputObject</span></span>
<span data-ttu-id="fac16-130">Das zu entfernende Richtliniendefinitionsobjekt, das aus einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fac16-130">The policy definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="fac16-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="fac16-131">-ManagementGroupName</span></span>
<span data-ttu-id="fac16-132">Der Name der Verwaltungsgruppe der zu löschende Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="fac16-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="fac16-133">-Name</span><span class="sxs-lookup"><span data-stu-id="fac16-133">-Name</span></span>
<span data-ttu-id="fac16-134">Gibt den Namen der Richtliniendefinition an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="fac16-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fac16-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="fac16-135">-Pre</span></span>
<span data-ttu-id="fac16-136">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fac16-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fac16-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fac16-137">-SubscriptionId</span></span>
<span data-ttu-id="fac16-138">Die Abonnement-ID der zu löschende Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="fac16-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="fac16-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fac16-139">-Confirm</span></span>
<span data-ttu-id="fac16-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fac16-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fac16-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fac16-141">-WhatIf</span></span>
<span data-ttu-id="fac16-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fac16-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fac16-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fac16-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fac16-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac16-144">CommonParameters</span></span>
<span data-ttu-id="fac16-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fac16-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac16-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fac16-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac16-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fac16-147">INPUTS</span></span>

### <span data-ttu-id="fac16-148">System.String</span><span class="sxs-lookup"><span data-stu-id="fac16-148">System.String</span></span>

### <span data-ttu-id="fac16-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fac16-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fac16-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fac16-150">OUTPUTS</span></span>

### <span data-ttu-id="fac16-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fac16-151">System.Boolean</span></span>

## <span data-ttu-id="fac16-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fac16-152">NOTES</span></span>

## <span data-ttu-id="fac16-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fac16-153">RELATED LINKS</span></span>

[<span data-ttu-id="fac16-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fac16-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="fac16-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fac16-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="fac16-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fac16-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


