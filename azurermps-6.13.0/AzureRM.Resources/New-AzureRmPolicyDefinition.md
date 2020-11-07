---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 22c8ea5c93a301796b2b42184a54744e9841163d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662161"
---
# <span data-ttu-id="bc41a-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bc41a-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="bc41a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc41a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc41a-103">Erstellt eine Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="bc41a-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc41a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc41a-104">SYNTAX</span></span>

### <span data-ttu-id="bc41a-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc41a-105">NameParameterSet (Default)</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bc41a-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc41a-106">ManagementGroupNameParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bc41a-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc41a-107">SubscriptionIdParameterSet</span></span>
```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bc41a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc41a-108">DESCRIPTION</span></span>
<span data-ttu-id="bc41a-109">Das Cmdlet **New-AzureRmPolicyDefinition** erstellt eine Richtliniendefinition, die eine Richtlinienregel im JSON-Format (JavaScript Object Notation) enthält.</span><span class="sxs-lookup"><span data-stu-id="bc41a-109">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="bc41a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc41a-110">EXAMPLES</span></span>

### <span data-ttu-id="bc41a-111">Beispiel 1: Erstellen einer Richtliniendefinition mithilfe einer Richtliniendatei</span><span class="sxs-lookup"><span data-stu-id="bc41a-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="bc41a-112">Mit diesem Befehl wird eine Richtliniendefinition mit dem Namen LocationDefinition erstellt, die die in C:\LocationPolicy.json angegebene Richtlinienregel enthält.</span><span class="sxs-lookup"><span data-stu-id="bc41a-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="bc41a-113">Oben finden Sie Beispielinhalte für die Datei "LocationPolicy.js".</span><span class="sxs-lookup"><span data-stu-id="bc41a-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="bc41a-114">Beispiel 2: Erstellen einer parametrisierten Richtliniendefinition mithilfe von Inline Parametern</span><span class="sxs-lookup"><span data-stu-id="bc41a-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzureRmPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="bc41a-115">Mit diesem Befehl wird eine Richtliniendefinition mit dem Namen LocationDefinition erstellt, die die in C:\LocationPolicy.json angegebene Richtlinienregel enthält.</span><span class="sxs-lookup"><span data-stu-id="bc41a-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="bc41a-116">Die Parameterdefinition für die Richtlinienregel wird Inline bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="bc41a-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="bc41a-117">Beispiel 3: Erstellen einer Richtliniendefinition Inline in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="bc41a-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="bc41a-118">Dieser Befehl erstellt eine Richtliniendefinition mit dem Namen VMPolicyDefinition in der Verwaltungsgruppe Dept42.</span><span class="sxs-lookup"><span data-stu-id="bc41a-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="bc41a-119">Der Befehl gibt die Richtlinie als Zeichenfolge im gültigen JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="bc41a-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="bc41a-120">Beispiel 4: Erstellen einer Richtliniendefinition Inline mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="bc41a-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzureRmPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="bc41a-121">Dieser Befehl erstellt eine Richtliniendefinition mit dem Namen VMPolicyDefinition mit Metadaten, die angibt, dass die Kategorie "virtueller Computer" lautet.</span><span class="sxs-lookup"><span data-stu-id="bc41a-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="bc41a-122">Der Befehl gibt die Richtlinie als Zeichenfolge im gültigen JSON-Format an.</span><span class="sxs-lookup"><span data-stu-id="bc41a-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="bc41a-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc41a-123">PARAMETERS</span></span>

### <span data-ttu-id="bc41a-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bc41a-124">-ApiVersion</span></span>
<span data-ttu-id="bc41a-125">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="bc41a-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bc41a-126">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="bc41a-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bc41a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc41a-127">-DefaultProfile</span></span>
<span data-ttu-id="bc41a-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bc41a-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc41a-129">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc41a-129">-Description</span></span>
<span data-ttu-id="bc41a-130">Gibt eine Beschreibung für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="bc41a-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="bc41a-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc41a-131">-DisplayName</span></span>
<span data-ttu-id="bc41a-132">Gibt einen Anzeigenamen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="bc41a-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="bc41a-133">-Information</span><span class="sxs-lookup"><span data-stu-id="bc41a-133">-InformationAction</span></span>
<span data-ttu-id="bc41a-134">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="bc41a-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="bc41a-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bc41a-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc41a-136">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="bc41a-136">Continue</span></span>
- <span data-ttu-id="bc41a-137">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="bc41a-137">Ignore</span></span>
- <span data-ttu-id="bc41a-138">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="bc41a-138">Inquire</span></span>
- <span data-ttu-id="bc41a-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bc41a-139">SilentlyContinue</span></span>
- <span data-ttu-id="bc41a-140">Beenden</span><span class="sxs-lookup"><span data-stu-id="bc41a-140">Stop</span></span>
- <span data-ttu-id="bc41a-141">Anhalten</span><span class="sxs-lookup"><span data-stu-id="bc41a-141">Suspend</span></span>

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

### <span data-ttu-id="bc41a-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bc41a-142">-InformationVariable</span></span>
<span data-ttu-id="bc41a-143">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="bc41a-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bc41a-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="bc41a-144">-ManagementGroupName</span></span>
<span data-ttu-id="bc41a-145">Der Name der Verwaltungsgruppe der neuen Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="bc41a-145">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="bc41a-146">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="bc41a-146">-Metadata</span></span>
<span data-ttu-id="bc41a-147">Die Metadaten für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="bc41a-147">The metadata for policy definition.</span></span> <span data-ttu-id="bc41a-148">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="bc41a-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="bc41a-149">-Modus</span><span class="sxs-lookup"><span data-stu-id="bc41a-149">-Mode</span></span>
<span data-ttu-id="bc41a-150">Der Modus der Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="bc41a-150">The mode of the policy definition</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc41a-151">-Name</span><span class="sxs-lookup"><span data-stu-id="bc41a-151">-Name</span></span>
<span data-ttu-id="bc41a-152">Gibt einen Namen für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="bc41a-152">Specifies a name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc41a-153">-Parameter</span><span class="sxs-lookup"><span data-stu-id="bc41a-153">-Parameter</span></span>
<span data-ttu-id="bc41a-154">Die Parameters-Deklaration für die Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="bc41a-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="bc41a-155">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Parameterdeklaration enthält, oder die Parameters-Deklaration als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="bc41a-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="bc41a-156">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bc41a-156">-Policy</span></span>
<span data-ttu-id="bc41a-157">Gibt eine Richtlinienregel für die Richtliniendefinition an.</span><span class="sxs-lookup"><span data-stu-id="bc41a-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="bc41a-158">Sie können den Pfad einer JSON-Datei oder einer Zeichenfolge, die die Richtlinie enthält, im JSON-Format angeben.</span><span class="sxs-lookup"><span data-stu-id="bc41a-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc41a-159">-Pre</span><span class="sxs-lookup"><span data-stu-id="bc41a-159">-Pre</span></span>
<span data-ttu-id="bc41a-160">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="bc41a-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bc41a-161">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="bc41a-161">-SubscriptionId</span></span>
<span data-ttu-id="bc41a-162">Die Abonnement-ID der neuen Richtliniendefinition.</span><span class="sxs-lookup"><span data-stu-id="bc41a-162">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="bc41a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc41a-163">CommonParameters</span></span>
<span data-ttu-id="bc41a-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc41a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc41a-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc41a-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc41a-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc41a-166">INPUTS</span></span>

## <span data-ttu-id="bc41a-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc41a-167">OUTPUTS</span></span>

## <span data-ttu-id="bc41a-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc41a-168">NOTES</span></span>

## <span data-ttu-id="bc41a-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc41a-169">RELATED LINKS</span></span>

[<span data-ttu-id="bc41a-170">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bc41a-170">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="bc41a-171">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bc41a-171">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="bc41a-172">Satz-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bc41a-172">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


