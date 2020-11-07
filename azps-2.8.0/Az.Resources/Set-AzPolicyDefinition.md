---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 4016809ed2592c5d10bc284e4a692381d7965107
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824932"
---
# <span data-ttu-id="e435a-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e435a-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="e435a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e435a-102">SYNOPSIS</span></span>
<span data-ttu-id="e435a-103">Ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="e435a-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="e435a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e435a-104">SYNTAX</span></span>

### <span data-ttu-id="e435a-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e435a-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e435a-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e435a-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e435a-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e435a-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e435a-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e435a-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e435a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e435a-109">DESCRIPTION</span></span>
<span data-ttu-id="e435a-110">Das Cmdlet " **Satz-AzPolicyDefinition** " ändert eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="e435a-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="e435a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e435a-111">EXAMPLES</span></span>

### <span data-ttu-id="e435a-112">Beispiel 1: Aktualisieren der Beschreibung einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="e435a-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="e435a-113">Der erste Befehl ruft mithilfe des Get-AzPolicyDefinition-Cmdlets eine Richtliniendefinition mit dem Namen VMPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="e435a-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="e435a-114">Der Befehl speichert das Objekt in der $PolicyDefinition Variablen.</span><span class="sxs-lookup"><span data-stu-id="e435a-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="e435a-115">Der zweite Befehl aktualisiert die Beschreibung der Richtliniendefinition, die von der Eigenschaft " **Resourcen** -Eigenschaft" von $PolicyDefinition identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="e435a-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="e435a-116">Beispiel 2: Aktualisieren des Modus einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="e435a-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="e435a-117">Dieser Befehl aktualisiert die Richtliniendefinition mit dem Namen VMPolicyDefinition mithilfe des Set-AzPolicyDefinition-Cmdlets, um die Mode-Eigenschaft auf "alle" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e435a-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="e435a-118">Beispiel 3: Aktualisieren der Metadaten einer Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="e435a-118">Example 3: Update the metadata of a policy definition</span></span>
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

<span data-ttu-id="e435a-119">Dieser Befehl aktualisiert die Metadaten einer Richtliniendefinition mit dem Namen VMPolicyDefinition, um anzugeben, dass die Kategorie "virtueller Computer" lautet.</span><span class="sxs-lookup"><span data-stu-id="e435a-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="e435a-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="e435a-120">PARAMETERS</span></span>

### <span data-ttu-id="e435a-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e435a-121">-ApiVersion</span></span>
<span data-ttu-id="e435a-122">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="e435a-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e435a-123">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="e435a-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e435a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e435a-124">-DefaultProfile</span></span>
<span data-ttu-id="e435a-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e435a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e435a-126">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e435a-126">-Description</span></span>
<span data-ttu-id="e435a-127">Gibt eine neue Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="e435a-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="e435a-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e435a-128">-DisplayName</span></span>
<span data-ttu-id="e435a-129">Gibt einen neuen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="e435a-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="e435a-130">-ID</span><span class="sxs-lookup"><span data-stu-id="e435a-130">-Id</span></span>
<span data-ttu-id="e435a-131">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e435a-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e435a-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e435a-132">-ManagementGroupName</span></span>
<span data-ttu-id="e435a-133">Der Name der Verwaltungsgruppe der Richtliniendefinition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e435a-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="e435a-134">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="e435a-134">-Metadata</span></span>
<span data-ttu-id="e435a-135">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="e435a-135">The metadata for policy definition.</span></span> <span data-ttu-id="e435a-136">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e435a-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="e435a-137">-Modus</span><span class="sxs-lookup"><span data-stu-id="e435a-137">-Mode</span></span>
<span data-ttu-id="e435a-138">Der Modus der neuen Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="e435a-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="e435a-139">-Name</span><span class="sxs-lookup"><span data-stu-id="e435a-139">-Name</span></span>
<span data-ttu-id="e435a-140">Gibt den Namen der Richtliniendefinition an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e435a-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e435a-141">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e435a-141">-Parameter</span></span>
<span data-ttu-id="e435a-142">Die Parameters-Deklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="e435a-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="e435a-143">Dies kann entweder ein Pfad zu einem Dateinamen oder URI sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e435a-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="e435a-144">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e435a-144">-Policy</span></span>
<span data-ttu-id="e435a-145">Gibt neue Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="e435a-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="e435a-146">Sie können den Pfad einer JSON-Datei oder einer Zeichenfolge, die die Richtlinie enthält, im JSON-Format (JavaScript Object Notation) angeben.</span><span class="sxs-lookup"><span data-stu-id="e435a-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="e435a-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="e435a-147">-Pre</span></span>
<span data-ttu-id="e435a-148">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e435a-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e435a-149">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e435a-149">-SubscriptionId</span></span>
<span data-ttu-id="e435a-150">Die Abonnement-ID der Richtliniendefinition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e435a-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="e435a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e435a-151">CommonParameters</span></span>
<span data-ttu-id="e435a-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e435a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e435a-153">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e435a-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e435a-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e435a-154">INPUTS</span></span>

### <span data-ttu-id="e435a-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e435a-155">System.String</span></span>

### <span data-ttu-id="e435a-156">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e435a-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e435a-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e435a-157">OUTPUTS</span></span>

### <span data-ttu-id="e435a-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e435a-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e435a-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="e435a-159">NOTES</span></span>

## <span data-ttu-id="e435a-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e435a-160">RELATED LINKS</span></span>

[<span data-ttu-id="e435a-161">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e435a-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="e435a-162">Neu – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e435a-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="e435a-163">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e435a-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


