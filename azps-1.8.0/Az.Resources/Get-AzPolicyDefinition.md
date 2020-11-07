---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 78dc06f53a94f6fe1524189a0cea32f214439f66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659636"
---
# <span data-ttu-id="01faa-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="01faa-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="01faa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01faa-102">SYNOPSIS</span></span>
<span data-ttu-id="01faa-103">Ruft Richtlinien Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="01faa-103">Gets policy definitions.</span></span>

## <span data-ttu-id="01faa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01faa-104">SYNTAX</span></span>

### <span data-ttu-id="01faa-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="01faa-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01faa-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="01faa-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01faa-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01faa-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01faa-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01faa-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01faa-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="01faa-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01faa-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="01faa-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01faa-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01faa-111">DESCRIPTION</span></span>
<span data-ttu-id="01faa-112">Das Cmdlet " **Get-AzPolicyDefinition** " Ruft eine Sammlung von Richtlinien Definitionen oder eine bestimmte Richtliniendefinition ab, die durch den Namen oder die ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="01faa-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="01faa-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01faa-113">EXAMPLES</span></span>

### <span data-ttu-id="01faa-114">Beispiel 1: Abrufen aller Richtlinien Definitionen</span><span class="sxs-lookup"><span data-stu-id="01faa-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="01faa-115">Dieser Befehl ruft alle Richtlinien Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="01faa-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="01faa-116">Beispiel 2: Abrufen der Richtliniendefinition aus dem aktuellen Abonnement nach Name</span><span class="sxs-lookup"><span data-stu-id="01faa-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="01faa-117">Dieser Befehl ruft die Richtliniendefinition mit dem Namen VMPolicyDefinition aus dem aktuellen Standardabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="01faa-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="01faa-118">Beispiel 3: Abrufen der Richtliniendefinition aus der Verwaltungsgruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="01faa-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="01faa-119">Dieser Befehl ruft die Richtliniendefinition mit dem Namen VMPolicyDefinition aus der Verwaltungsgruppe mit dem Namen Dept42 ab.</span><span class="sxs-lookup"><span data-stu-id="01faa-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="01faa-120">Beispiel 4: Abrufen aller integrierten Richtlinien Definitionen aus einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="01faa-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="01faa-121">Dieser Befehl ruft alle integrierten Richtlinien Definitionen aus dem Abonnement mit ID 3bf44b72-c631-427a-b8c8-53e2595398ca ab.</span><span class="sxs-lookup"><span data-stu-id="01faa-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="01faa-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="01faa-122">PARAMETERS</span></span>

### <span data-ttu-id="01faa-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="01faa-123">-ApiVersion</span></span>
<span data-ttu-id="01faa-124">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="01faa-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="01faa-125">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="01faa-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="01faa-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="01faa-126">-Builtin</span></span>
<span data-ttu-id="01faa-127">Begrenzt die Liste der Ergebnisse auf nur integrierte Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="01faa-127">Limits list of results to only built-in policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01faa-128">– Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="01faa-128">-Custom</span></span>
<span data-ttu-id="01faa-129">Begrenzt die Liste der Ergebnisse auf nur benutzerdefinierte Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="01faa-129">Limits list of results to only custom policy definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01faa-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01faa-130">-DefaultProfile</span></span>
<span data-ttu-id="01faa-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="01faa-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01faa-132">-ID</span><span class="sxs-lookup"><span data-stu-id="01faa-132">-Id</span></span>
<span data-ttu-id="01faa-133">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="01faa-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="01faa-134">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="01faa-134">-ManagementGroupName</span></span>
<span data-ttu-id="01faa-135">Der Name der Verwaltungsgruppe der Richtliniendefinition (en), die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="01faa-135">The name of the management group of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01faa-136">-Name</span><span class="sxs-lookup"><span data-stu-id="01faa-136">-Name</span></span>
<span data-ttu-id="01faa-137">Gibt den Namen der Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="01faa-137">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01faa-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="01faa-138">-Pre</span></span>
<span data-ttu-id="01faa-139">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="01faa-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="01faa-140">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="01faa-140">-SubscriptionId</span></span>
<span data-ttu-id="01faa-141">Die Abonnement-ID der Richtliniendefinition (en), die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="01faa-141">The subscription ID of the policy definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01faa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01faa-142">CommonParameters</span></span>
<span data-ttu-id="01faa-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01faa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01faa-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01faa-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01faa-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01faa-145">INPUTS</span></span>

### <span data-ttu-id="01faa-146">System. String</span><span class="sxs-lookup"><span data-stu-id="01faa-146">System.String</span></span>

### <span data-ttu-id="01faa-147">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="01faa-147">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="01faa-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01faa-148">OUTPUTS</span></span>

### <span data-ttu-id="01faa-149">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="01faa-149">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="01faa-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="01faa-150">NOTES</span></span>

## <span data-ttu-id="01faa-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01faa-151">RELATED LINKS</span></span>

[<span data-ttu-id="01faa-152">Neu – AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="01faa-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="01faa-153">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="01faa-153">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="01faa-154">Satz-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="01faa-154">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


