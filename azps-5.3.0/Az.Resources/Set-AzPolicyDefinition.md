---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 3aed403965bc48a26044b930fdf5cc9e9a93bbbe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459192"
---
# <span data-ttu-id="0bf39-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0bf39-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="0bf39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf39-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf39-103">Ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="0bf39-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="0bf39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bf39-104">SYNTAX</span></span>

### <span data-ttu-id="0bf39-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0bf39-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf39-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf39-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf39-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf39-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf39-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf39-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bf39-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf39-109">InputObjectParameterSet</span></span>
```
Set-AzPolicyDefinition [-DisplayName <String>] [-Description <String>] [-Policy <String>] [-Metadata <String>]
 [-Parameter <String>] [-Mode <String>] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bf39-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bf39-110">DESCRIPTION</span></span>
<span data-ttu-id="0bf39-111">Das **Cmdlet "Set-AzPolicyDefinition"** ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="0bf39-111">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="0bf39-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0bf39-112">EXAMPLES</span></span>

### <span data-ttu-id="0bf39-113">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="0bf39-113">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="0bf39-114">Der erste Befehl ruft eine Richtliniendefinition namens VMPolicyDefinition mithilfe des Get-AzPolicyDefinition cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="0bf39-114">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="0bf39-115">Der Befehl speichert dieses Objekt in der $PolicyDefinition Variable.</span><span class="sxs-lookup"><span data-stu-id="0bf39-115">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="0bf39-116">Mit dem zweiten Befehl wird die Beschreibung der Richtliniendefinition aktualisiert, die durch die **Eigenschaft "ResourceId"** der $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="0bf39-116">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="0bf39-117">Beispiel 2: Aktualisieren des Modus einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="0bf39-117">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="0bf39-118">Mit diesem Befehl wird die Richtliniendefinition "VMPolicyDefinition" aktualisiert, indem das Set-AzPolicyDefinition-Cmdlet verwendet wird, um die Moduseigenschaft auf "All" zu setzen.</span><span class="sxs-lookup"><span data-stu-id="0bf39-118">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="0bf39-119">Beispiel 3: Aktualisieren der Metadaten einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="0bf39-119">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="0bf39-120">Dieser Befehl aktualisiert die Metadaten einer Richtliniendefinition namens VMPolicyDefinition, um anzugeben, dass die Kategorie "Virtual Machine" ist.</span><span class="sxs-lookup"><span data-stu-id="0bf39-120">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="0bf39-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bf39-121">PARAMETERS</span></span>

### <span data-ttu-id="0bf39-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0bf39-122">-ApiVersion</span></span>
<span data-ttu-id="0bf39-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="0bf39-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0bf39-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="0bf39-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0bf39-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf39-125">-DefaultProfile</span></span>
<span data-ttu-id="0bf39-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0bf39-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bf39-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bf39-127">-Description</span></span>
<span data-ttu-id="0bf39-128">Gibt eine neue Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="0bf39-128">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="0bf39-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0bf39-129">-DisplayName</span></span>
<span data-ttu-id="0bf39-130">Gibt einen neuen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="0bf39-130">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="0bf39-131">-ID</span><span class="sxs-lookup"><span data-stu-id="0bf39-131">-Id</span></span>
<span data-ttu-id="0bf39-132">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0bf39-132">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0bf39-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bf39-133">-InputObject</span></span>
<span data-ttu-id="0bf39-134">Das Zu aktualisierende Richtliniendefinitionsobjekt, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0bf39-134">The policy definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="0bf39-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0bf39-135">-ManagementGroupName</span></span>
<span data-ttu-id="0bf39-136">Der Name der Verwaltungsgruppe der zu aktualisierende Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="0bf39-136">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="0bf39-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0bf39-137">-Metadata</span></span>
<span data-ttu-id="0bf39-138">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="0bf39-138">The metadata for policy definition.</span></span> <span data-ttu-id="0bf39-139">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0bf39-139">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="0bf39-140">-Mode</span><span class="sxs-lookup"><span data-stu-id="0bf39-140">-Mode</span></span>
<span data-ttu-id="0bf39-141">Der Modus der neuen Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="0bf39-141">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="0bf39-142">-Name</span><span class="sxs-lookup"><span data-stu-id="0bf39-142">-Name</span></span>
<span data-ttu-id="0bf39-143">Gibt den Namen der Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0bf39-143">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0bf39-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="0bf39-144">-Parameter</span></span>
<span data-ttu-id="0bf39-145">Die Parameterdeklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="0bf39-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="0bf39-146">Dabei kann es sich entweder um einen Pfad zu einem Dateinamen oder URI mit der Parameterdeklaration oder um die Parameterdeklaration als Zeichenfolge geben.</span><span class="sxs-lookup"><span data-stu-id="0bf39-146">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="0bf39-147">-Policy</span><span class="sxs-lookup"><span data-stu-id="0bf39-147">-Policy</span></span>
<span data-ttu-id="0bf39-148">Gibt eine neue Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="0bf39-148">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="0bf39-149">Sie können den Pfad einer JSON-Datei oder eine Zeichenfolge angeben, die die Richtlinie im JavaScript Object Notation (JSON)-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="0bf39-149">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="0bf39-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="0bf39-150">-Pre</span></span>
<span data-ttu-id="0bf39-151">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bf39-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0bf39-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0bf39-152">-SubscriptionId</span></span>
<span data-ttu-id="0bf39-153">Die Abonnement-ID der zu aktualisierende Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="0bf39-153">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="0bf39-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf39-154">CommonParameters</span></span>
<span data-ttu-id="0bf39-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bf39-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf39-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bf39-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf39-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0bf39-157">INPUTS</span></span>

### <span data-ttu-id="0bf39-158">System.String</span><span class="sxs-lookup"><span data-stu-id="0bf39-158">System.String</span></span>

### <span data-ttu-id="0bf39-159">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0bf39-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0bf39-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0bf39-160">OUTPUTS</span></span>

### <span data-ttu-id="0bf39-161">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="0bf39-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0bf39-162">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0bf39-162">NOTES</span></span>

## <span data-ttu-id="0bf39-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0bf39-163">RELATED LINKS</span></span>

[<span data-ttu-id="0bf39-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0bf39-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="0bf39-165">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0bf39-165">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="0bf39-166">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0bf39-166">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


