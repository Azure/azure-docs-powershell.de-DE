---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: bd374f19a282ccafc3201a2965c33d4e8a3007ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996462"
---
# <span data-ttu-id="4fec5-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fec5-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="4fec5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4fec5-102">SYNOPSIS</span></span>
<span data-ttu-id="4fec5-103">Entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="4fec5-103">Removes a policy definition.</span></span>

## <span data-ttu-id="4fec5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fec5-104">SYNTAX</span></span>

### <span data-ttu-id="4fec5-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4fec5-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fec5-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fec5-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fec5-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fec5-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fec5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fec5-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fec5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fec5-109">DESCRIPTION</span></span>
<span data-ttu-id="4fec5-110">Das Cmdlet **Remove-AzPolicyDefinition** entfernt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="4fec5-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="4fec5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fec5-111">EXAMPLES</span></span>

### <span data-ttu-id="4fec5-112">Beispiel 1: Entfernen der Richtliniendefinition nach Name</span><span class="sxs-lookup"><span data-stu-id="4fec5-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="4fec5-113">Mit diesem Befehl wird die angegebene Richtliniendefinition entfernt.</span><span class="sxs-lookup"><span data-stu-id="4fec5-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="4fec5-114">Beispiel 2: Entfernen der Richtliniendefinition nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4fec5-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="4fec5-115">Der erste Befehl ruft mithilfe des Get-AzPolicyDefinition-Cmdlets eine Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="4fec5-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4fec5-116">Der Befehl speichert Sie in der $PolicyDefinition-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4fec5-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="4fec5-117">Mit dem zweiten Befehl wird die Richtliniendefinition entfernt, die durch die Eigenschaft " **Resourcen** " von $PolicyDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="4fec5-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="4fec5-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fec5-118">PARAMETERS</span></span>

### <span data-ttu-id="4fec5-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4fec5-119">-ApiVersion</span></span>
<span data-ttu-id="4fec5-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="4fec5-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4fec5-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="4fec5-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4fec5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fec5-122">-DefaultProfile</span></span>
<span data-ttu-id="4fec5-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4fec5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fec5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4fec5-124">-Force</span></span>
<span data-ttu-id="4fec5-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="4fec5-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4fec5-126">-ID</span><span class="sxs-lookup"><span data-stu-id="4fec5-126">-Id</span></span>
<span data-ttu-id="4fec5-127">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4fec5-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4fec5-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="4fec5-128">-ManagementGroupName</span></span>
<span data-ttu-id="4fec5-129">Der Name der Verwaltungsgruppe der zu löschenden Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="4fec5-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="4fec5-130">-Name</span><span class="sxs-lookup"><span data-stu-id="4fec5-130">-Name</span></span>
<span data-ttu-id="4fec5-131">Gibt den Namen der Richtliniendefinition an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4fec5-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4fec5-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="4fec5-132">-Pre</span></span>
<span data-ttu-id="4fec5-133">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4fec5-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4fec5-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4fec5-134">-SubscriptionId</span></span>
<span data-ttu-id="4fec5-135">Die Abonnement-ID der Richtliniendefinition, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4fec5-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="4fec5-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4fec5-136">-Confirm</span></span>
<span data-ttu-id="4fec5-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4fec5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fec5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fec5-138">-WhatIf</span></span>
<span data-ttu-id="4fec5-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fec5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fec5-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fec5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fec5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fec5-141">CommonParameters</span></span>
<span data-ttu-id="4fec5-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fec5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fec5-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fec5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fec5-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4fec5-144">INPUTS</span></span>

### <span data-ttu-id="4fec5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4fec5-145">System.String</span></span>

### <span data-ttu-id="4fec5-146">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4fec5-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4fec5-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4fec5-147">OUTPUTS</span></span>

### <span data-ttu-id="4fec5-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fec5-148">System.Boolean</span></span>

## <span data-ttu-id="4fec5-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="4fec5-149">NOTES</span></span>

## <span data-ttu-id="4fec5-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4fec5-150">RELATED LINKS</span></span>

[<span data-ttu-id="4fec5-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fec5-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="4fec5-152">Neu – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fec5-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="4fec5-153">Satz-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4fec5-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


