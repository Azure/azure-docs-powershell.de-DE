---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: 5b6d514fc41c909fdd48b6a13ba85ab5836a5668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824920"
---
# <span data-ttu-id="fb903-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="fb903-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="fb903-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb903-102">SYNOPSIS</span></span>
<span data-ttu-id="fb903-103">Ändert eine Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="fb903-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="fb903-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb903-104">SYNTAX</span></span>

### <span data-ttu-id="fb903-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb903-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb903-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb903-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb903-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb903-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb903-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb903-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb903-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb903-109">DESCRIPTION</span></span>
<span data-ttu-id="fb903-110">Das Cmdlet " **Satz-AzPolicySetDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="fb903-110">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="fb903-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb903-111">EXAMPLES</span></span>

### <span data-ttu-id="fb903-112">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="fb903-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="fb903-113">Der erste Befehl ruft eine Richtliniensatz Definition mithilfe des Get-AzPolicySetDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="fb903-113">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="fb903-114">Der Befehl speichert das Objekt in der $PolicySetDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb903-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="fb903-115">Mit dem zweiten Befehl wird die Beschreibung der Richtliniensatz Definition aktualisiert, die durch die Eigenschaft " **Resourcen** " von $PolicySetDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="fb903-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="fb903-116">Beispiel 2: Aktualisieren der Metadaten einer Richtliniensatz Definition</span><span class="sxs-lookup"><span data-stu-id="fb903-116">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="fb903-117">Dieser Befehl aktualisiert die Metadaten einer Richtliniensatz Definition mit dem Namen VMPolicySetDefinition, um anzugeben, dass die Kategorie "virtueller Computer" lautet.</span><span class="sxs-lookup"><span data-stu-id="fb903-117">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="fb903-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb903-118">PARAMETERS</span></span>

### <span data-ttu-id="fb903-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fb903-119">-ApiVersion</span></span>
<span data-ttu-id="fb903-120">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb903-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fb903-121">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="fb903-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fb903-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb903-122">-DefaultProfile</span></span>
<span data-ttu-id="fb903-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fb903-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb903-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb903-124">-Description</span></span>
<span data-ttu-id="fb903-125">Die Beschreibung für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="fb903-125">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb903-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fb903-126">-DisplayName</span></span>
<span data-ttu-id="fb903-127">Der Anzeigename für die Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="fb903-127">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb903-128">-ID</span><span class="sxs-lookup"><span data-stu-id="fb903-128">-Id</span></span>
<span data-ttu-id="fb903-129">Die vollqualifizierte Richtlinien Definitions-ID, einschließlich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="fb903-129">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="fb903-130">z.b./Subscriptions/{SubscriptionId}/ResourceGroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="fb903-130">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="fb903-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="fb903-131">-ManagementGroupName</span></span>
<span data-ttu-id="fb903-132">Der Name der Verwaltungsgruppe der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb903-132">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="fb903-133">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="fb903-133">-Metadata</span></span>
<span data-ttu-id="fb903-134">Die Metadaten der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="fb903-134">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="fb903-135">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fb903-135">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb903-136">-Name</span><span class="sxs-lookup"><span data-stu-id="fb903-136">-Name</span></span>
<span data-ttu-id="fb903-137">Der Richtliniensatz-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="fb903-137">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb903-138">-Parameter</span><span class="sxs-lookup"><span data-stu-id="fb903-138">-Parameter</span></span>
<span data-ttu-id="fb903-139">Die Parameters-Deklaration der aktualisierten Richtliniensatz Definition.</span><span class="sxs-lookup"><span data-stu-id="fb903-139">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="fb903-140">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fb903-140">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb903-141">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fb903-141">-PolicyDefinition</span></span>
<span data-ttu-id="fb903-142">Die Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="fb903-142">The policy definitions.</span></span> <span data-ttu-id="fb903-143">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Richtlinien Definitionen enthält, oder die Richtlinien Definitionen als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fb903-143">This can either be a path to a file name containing the policy definitions, or the policy definitions as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb903-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="fb903-144">-Pre</span></span>
<span data-ttu-id="fb903-145">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="fb903-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fb903-146">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fb903-146">-SubscriptionId</span></span>
<span data-ttu-id="fb903-147">Die Abonnement-ID der Richtliniensatz Definition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb903-147">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="fb903-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb903-148">-Confirm</span></span>
<span data-ttu-id="fb903-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb903-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb903-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb903-150">-WhatIf</span></span>
<span data-ttu-id="fb903-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb903-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb903-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb903-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb903-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb903-153">CommonParameters</span></span>
<span data-ttu-id="fb903-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb903-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb903-155">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb903-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb903-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb903-156">INPUTS</span></span>

### <span data-ttu-id="fb903-157">System. String</span><span class="sxs-lookup"><span data-stu-id="fb903-157">System.String</span></span>

### <span data-ttu-id="fb903-158">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb903-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fb903-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb903-159">OUTPUTS</span></span>

### <span data-ttu-id="fb903-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fb903-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fb903-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb903-161">NOTES</span></span>

## <span data-ttu-id="fb903-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb903-162">RELATED LINKS</span></span>
