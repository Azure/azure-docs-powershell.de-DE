---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174429"
---
# <span data-ttu-id="d65be-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d65be-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="d65be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d65be-102">SYNOPSIS</span></span>
<span data-ttu-id="d65be-103">Ruft Richtlinienzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="d65be-103">Gets policy assignments.</span></span>

## <span data-ttu-id="d65be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d65be-104">SYNTAX</span></span>

### <span data-ttu-id="d65be-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d65be-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d65be-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d65be-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d65be-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="d65be-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d65be-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d65be-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d65be-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d65be-109">DESCRIPTION</span></span>
<span data-ttu-id="d65be-110">Das Cmdlet " **Get-AzPolicyAssignment** " ruft alle Richtlinienzuweisungen oder bestimmte Aufgaben ab.</span><span class="sxs-lookup"><span data-stu-id="d65be-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="d65be-111">Identifizieren Sie eine Richtlinien Aufgabe, die nach Name und Bereich oder nach ID abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d65be-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="d65be-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d65be-112">EXAMPLES</span></span>

### <span data-ttu-id="d65be-113">Beispiel 1: Abrufen aller Richtlinienzuweisungen</span><span class="sxs-lookup"><span data-stu-id="d65be-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="d65be-114">Mit diesem Befehl werden alle Richtlinienzuweisungen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d65be-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="d65be-115">Beispiel 2: Abrufen einer bestimmten Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="d65be-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="d65be-116">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d65be-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d65be-117">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen "PolicyAssignment07" für den Bereich ab **, den die Eigenschaft "** Eigenschaften" von $ResourceGroup identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d65be-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="d65be-118">Beispiel 3: Abrufen aller einer Verwaltungsgruppe zugewiesenen Richtlinienzuweisungen</span><span class="sxs-lookup"><span data-stu-id="d65be-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="d65be-119">Der erste Befehl gibt die ID der zu abfragenden Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d65be-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="d65be-120">Der zweite Befehl ruft alle Richtlinienzuweisungen ab, die der Verwaltungsgruppe mit der ID "mymanagegroup" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="d65be-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="d65be-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="d65be-121">PARAMETERS</span></span>

### <span data-ttu-id="d65be-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d65be-122">-ApiVersion</span></span>
<span data-ttu-id="d65be-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="d65be-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d65be-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="d65be-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d65be-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65be-125">-DefaultProfile</span></span>
<span data-ttu-id="d65be-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d65be-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d65be-127">-ID</span><span class="sxs-lookup"><span data-stu-id="d65be-127">-Id</span></span>
<span data-ttu-id="d65be-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d65be-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d65be-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="d65be-129">-IncludeDescendent</span></span>
<span data-ttu-id="d65be-130">Bewirkt, dass in der Liste der zurückgegebenen Richtlinienzuweisungen alle Aufgaben im Zusammenhang mit dem angegebenen Bereich eingeschlossen werden, einschließlich derer aus übergeordneten Bereichen und aus untergeordneten Bereichen.</span><span class="sxs-lookup"><span data-stu-id="d65be-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d65be-131">-Name</span><span class="sxs-lookup"><span data-stu-id="d65be-131">-Name</span></span>
<span data-ttu-id="d65be-132">Gibt den Namen der Richtlinien Aufgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d65be-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d65be-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d65be-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="d65be-134">Gibt die ID der Richtliniendefinition für die Richtlinienzuweisungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d65be-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d65be-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="d65be-135">-Pre</span></span>
<span data-ttu-id="d65be-136">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d65be-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d65be-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="d65be-137">-Scope</span></span>
<span data-ttu-id="d65be-138">Gibt den Bereich an, auf dem die Richtlinie für die Aufgabe angewendet wird, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d65be-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d65be-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65be-139">CommonParameters</span></span>
<span data-ttu-id="d65be-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d65be-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65be-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d65be-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65be-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d65be-142">INPUTS</span></span>

### <span data-ttu-id="d65be-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d65be-143">System.String</span></span>

### <span data-ttu-id="d65be-144">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d65be-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d65be-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d65be-145">OUTPUTS</span></span>

### <span data-ttu-id="d65be-146">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d65be-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d65be-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="d65be-147">NOTES</span></span>

## <span data-ttu-id="d65be-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d65be-148">RELATED LINKS</span></span>

[<span data-ttu-id="d65be-149">Neu – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d65be-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="d65be-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d65be-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="d65be-151">Satz-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d65be-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


