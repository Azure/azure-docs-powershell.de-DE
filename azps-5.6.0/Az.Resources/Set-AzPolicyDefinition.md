---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: ee3f1ffdb7e95e3c00b30238bf6d35833d99cea6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948488"
---
# <span data-ttu-id="8f271-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8f271-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="8f271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f271-102">SYNOPSIS</span></span>
<span data-ttu-id="8f271-103">Ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="8f271-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="8f271-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f271-104">SYNTAX</span></span>

### <span data-ttu-id="8f271-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f271-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f271-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f271-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f271-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f271-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f271-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f271-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f271-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f271-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f271-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f271-110">DESCRIPTION</span></span>
<span data-ttu-id="8f271-111">Das **Cmdlet Set-AzPolicyDefinition** ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="8f271-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="8f271-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f271-112">EXAMPLES</span></span>

### <span data-ttu-id="8f271-113">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="8f271-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="8f271-114">Der erste Befehl ruft eine Richtliniendefinition namens VMPolicyDefinition mithilfe des cmdlets Get-AzPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="8f271-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="8f271-115">Der Befehl speichert dieses Objekt in der $PolicyDefinition-Variable.</span><span class="sxs-lookup"><span data-stu-id="8f271-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="8f271-116">Der zweite Befehl aktualisiert die Beschreibung der Richtliniendefinition, die durch die **ResourceId-Eigenschaft** von $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="8f271-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="8f271-117">Beispiel 2: Aktualisieren des Modus einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="8f271-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="8f271-118">Mit diesem Befehl wird die Richtliniendefinition mit dem Namen VMPolicyDefinition aktualisiert, indem das cmdlet Set-AzPolicyDefinition verwendet wird, um seine Moduseigenschaft auf "Alle" zu setzen.</span><span class="sxs-lookup"><span data-stu-id="8f271-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="8f271-119">Beispiel 3: Aktualisieren der Metadaten einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="8f271-119">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="8f271-120">Mit diesem Befehl werden die Metadaten einer Richtliniendefinition namens VMPolicyDefinition aktualisiert, um anzugeben, dass die Kategorie "Virtueller Computer" ist.</span><span class="sxs-lookup"><span data-stu-id="8f271-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="8f271-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8f271-121">PARAMETERS</span></span>

### <span data-ttu-id="8f271-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f271-122">-ApiVersion</span></span>
<span data-ttu-id="8f271-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="8f271-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8f271-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="8f271-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8f271-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f271-125">-DefaultProfile</span></span>
<span data-ttu-id="8f271-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8f271-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f271-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f271-127">-Description</span></span>
<span data-ttu-id="8f271-128">Gibt eine neue Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="8f271-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="8f271-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8f271-129">-DisplayName</span></span>
<span data-ttu-id="8f271-130">Gibt einen neuen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="8f271-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="8f271-131">-ID</span><span class="sxs-lookup"><span data-stu-id="8f271-131">-Id</span></span>
<span data-ttu-id="8f271-132">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8f271-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8f271-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f271-133">-InputObject</span></span>
<span data-ttu-id="8f271-134">Das zu aktualisierende Richtliniendefinitionsobjekt, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8f271-134">The policy definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="8f271-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8f271-135">-ManagementGroupName</span></span>
<span data-ttu-id="8f271-136">Der Name der Verwaltungsgruppe der zu aktualisierende Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="8f271-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="8f271-137">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="8f271-137">-Metadata</span></span>
<span data-ttu-id="8f271-138">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="8f271-138">The metadata for policy definition.</span></span> <span data-ttu-id="8f271-139">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8f271-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="8f271-140">-Modus</span><span class="sxs-lookup"><span data-stu-id="8f271-140">-Mode</span></span>
<span data-ttu-id="8f271-141">Der Modus der neuen Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="8f271-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="8f271-142">-Name</span><span class="sxs-lookup"><span data-stu-id="8f271-142">-Name</span></span>
<span data-ttu-id="8f271-143">Gibt den Namen der Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8f271-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8f271-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8f271-144">-Parameter</span></span>
<span data-ttu-id="8f271-145">Die Parameterdeklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="8f271-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="8f271-146">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameterdeklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8f271-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="8f271-147">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="8f271-147">-Policy</span></span>
<span data-ttu-id="8f271-148">Gibt eine neue Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="8f271-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="8f271-149">Sie können den Pfad einer JSON-Datei oder eine Zeichenfolge angeben, die die Richtlinie im JSON-Format (JavaScript Object Notation) enthält.</span><span class="sxs-lookup"><span data-stu-id="8f271-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="8f271-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="8f271-150">-Pre</span></span>
<span data-ttu-id="8f271-151">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f271-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8f271-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f271-152">-SubscriptionId</span></span>
<span data-ttu-id="8f271-153">Die Abonnement-ID der zu aktualisierende Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="8f271-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="8f271-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f271-154">CommonParameters</span></span>
<span data-ttu-id="8f271-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f271-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f271-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f271-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f271-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f271-157">INPUTS</span></span>

### <span data-ttu-id="8f271-158">System.String</span><span class="sxs-lookup"><span data-stu-id="8f271-158">System.String</span></span>

### <span data-ttu-id="8f271-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8f271-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8f271-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f271-160">OUTPUTS</span></span>

### <span data-ttu-id="8f271-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8f271-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8f271-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8f271-162">NOTES</span></span>

## <span data-ttu-id="8f271-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8f271-163">RELATED LINKS</span></span>

[<span data-ttu-id="8f271-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8f271-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="8f271-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8f271-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="8f271-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8f271-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


