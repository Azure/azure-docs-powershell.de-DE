---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 30e113ca85c24b46d4594658f1d91abb6b14bd3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495701"
---
# <span data-ttu-id="5b79d-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b79d-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="5b79d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b79d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b79d-103">Ruft Richtlinien Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="5b79d-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b79d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b79d-104">SYNTAX</span></span>

### <span data-ttu-id="5b79d-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b79d-105">NameParameterSet (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b79d-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b79d-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b79d-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b79d-107">SubscriptionIdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b79d-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b79d-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b79d-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b79d-109">BuiltinFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b79d-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b79d-110">CustomFilterParameterSet</span></span>
```
Get-AzureRmPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5b79d-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b79d-111">DESCRIPTION</span></span>
<span data-ttu-id="5b79d-112">Das Cmdlet " **Get-AzureRmPolicyDefinition** " Ruft eine Sammlung von Richtlinien Definitionen oder eine bestimmte Richtliniendefinition ab, die durch den Namen oder die ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5b79d-112">The **Get-AzureRmPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="5b79d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b79d-113">EXAMPLES</span></span>

### <span data-ttu-id="5b79d-114">Beispiel 1: Abrufen aller Richtlinien Definitionen</span><span class="sxs-lookup"><span data-stu-id="5b79d-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition
```

<span data-ttu-id="5b79d-115">Dieser Befehl ruft alle Richtlinien Definitionen ab.</span><span class="sxs-lookup"><span data-stu-id="5b79d-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="5b79d-116">Beispiel 2: Abrufen der Richtliniendefinition aus dem aktuellen Abonnement nach Name</span><span class="sxs-lookup"><span data-stu-id="5b79d-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="5b79d-117">Dieser Befehl ruft die Richtliniendefinition mit dem Namen VMPolicyDefinition aus dem aktuellen Standardabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5b79d-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="5b79d-118">Beispiel 3: Abrufen der Richtliniendefinition aus der Verwaltungsgruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="5b79d-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="5b79d-119">Dieser Befehl ruft die Richtliniendefinition mit dem Namen VMPolicyDefinition aus der Verwaltungsgruppe mit dem Namen Dept42 ab.</span><span class="sxs-lookup"><span data-stu-id="5b79d-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="5b79d-120">Beispiel 4: Abrufen aller integrierten Richtlinien Definitionen aus einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="5b79d-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzureRmPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="5b79d-121">Dieser Befehl ruft alle integrierten Richtlinien Definitionen aus dem Abonnement mit ID 3bf44b72-c631-427a-b8c8-53e2595398ca ab.</span><span class="sxs-lookup"><span data-stu-id="5b79d-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="5b79d-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b79d-122">PARAMETERS</span></span>

### <span data-ttu-id="5b79d-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5b79d-123">-ApiVersion</span></span>
<span data-ttu-id="5b79d-124">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="5b79d-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5b79d-125">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="5b79d-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5b79d-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="5b79d-126">-Builtin</span></span>
<span data-ttu-id="5b79d-127">Begrenzt die Liste der Ergebnisse auf nur integrierte Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="5b79d-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="5b79d-128">– Benutzerdefiniert</span><span class="sxs-lookup"><span data-stu-id="5b79d-128">-Custom</span></span>
<span data-ttu-id="5b79d-129">Begrenzt die Liste der Ergebnisse auf nur benutzerdefinierte Richtlinien Definitionen.</span><span class="sxs-lookup"><span data-stu-id="5b79d-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="5b79d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b79d-130">-DefaultProfile</span></span>
<span data-ttu-id="5b79d-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5b79d-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b79d-132">-ID</span><span class="sxs-lookup"><span data-stu-id="5b79d-132">-Id</span></span>
<span data-ttu-id="5b79d-133">Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5b79d-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5b79d-134">-Information</span><span class="sxs-lookup"><span data-stu-id="5b79d-134">-InformationAction</span></span>
<span data-ttu-id="5b79d-135">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="5b79d-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="5b79d-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5b79d-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b79d-137">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="5b79d-137">Continue</span></span>
- <span data-ttu-id="5b79d-138">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="5b79d-138">Ignore</span></span>
- <span data-ttu-id="5b79d-139">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="5b79d-139">Inquire</span></span>
- <span data-ttu-id="5b79d-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5b79d-140">SilentlyContinue</span></span>
- <span data-ttu-id="5b79d-141">Beenden</span><span class="sxs-lookup"><span data-stu-id="5b79d-141">Stop</span></span>
- <span data-ttu-id="5b79d-142">Anhalten</span><span class="sxs-lookup"><span data-stu-id="5b79d-142">Suspend</span></span>

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

### <span data-ttu-id="5b79d-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5b79d-143">-InformationVariable</span></span>
<span data-ttu-id="5b79d-144">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="5b79d-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5b79d-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="5b79d-145">-ManagementGroupName</span></span>
<span data-ttu-id="5b79d-146">Der Name der Verwaltungsgruppe der Richtliniendefinition (en), die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b79d-146">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="5b79d-147">-Name</span><span class="sxs-lookup"><span data-stu-id="5b79d-147">-Name</span></span>
<span data-ttu-id="5b79d-148">Gibt den Namen der Richtliniendefinition an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5b79d-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5b79d-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="5b79d-149">-Pre</span></span>
<span data-ttu-id="5b79d-150">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5b79d-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5b79d-151">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5b79d-151">-SubscriptionId</span></span>
<span data-ttu-id="5b79d-152">Die Abonnement-ID der Richtliniendefinition (en), die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b79d-152">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="5b79d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b79d-153">CommonParameters</span></span>
<span data-ttu-id="5b79d-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b79d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b79d-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b79d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b79d-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b79d-156">INPUTS</span></span>

## <span data-ttu-id="5b79d-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b79d-157">OUTPUTS</span></span>

## <span data-ttu-id="5b79d-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b79d-158">NOTES</span></span>

## <span data-ttu-id="5b79d-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b79d-159">RELATED LINKS</span></span>

[<span data-ttu-id="5b79d-160">Neu – AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b79d-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="5b79d-161">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b79d-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="5b79d-162">Satz-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b79d-162">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


