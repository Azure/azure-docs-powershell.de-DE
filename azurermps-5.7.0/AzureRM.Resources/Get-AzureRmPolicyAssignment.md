---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663758"
---
# <span data-ttu-id="f6dfd-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f6dfd-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="f6dfd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="f6dfd-103">Ruft Richtlinienzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6dfd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6dfd-104">SYNTAX</span></span>

### <span data-ttu-id="f6dfd-105">GetAllPolicyAssignments (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6dfd-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f6dfd-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f6dfd-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f6dfd-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="f6dfd-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f6dfd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6dfd-108">DESCRIPTION</span></span>
<span data-ttu-id="f6dfd-109">Das Cmdlet " **Get-AzureRmPolicyAssignment** " ruft alle Richtlinienzuweisungen oder bestimmte Aufgaben ab.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="f6dfd-110">Identifizieren Sie eine Richtlinien Aufgabe, die nach Name und Bereich oder nach ID abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="f6dfd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6dfd-111">EXAMPLES</span></span>

### <span data-ttu-id="f6dfd-112">Beispiel 1: Abrufen aller Richtlinienzuweisungen</span><span class="sxs-lookup"><span data-stu-id="f6dfd-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="f6dfd-113">Mit diesem Befehl werden alle Richtlinienzuweisungen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="f6dfd-114">Beispiel 2: Abrufen einer bestimmten Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="f6dfd-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="f6dfd-115">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="f6dfd-116">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f6dfd-117">Der zweite Befehl erhält die Richtlinienzuweisung mit dem Namen "PolicyAssignment07" für den Bereich, der von der Eigenschaft " **imsourcen** " von $ResourceGroup identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="f6dfd-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6dfd-118">PARAMETERS</span></span>

### <span data-ttu-id="f6dfd-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f6dfd-119">-ApiVersion</span></span>
<span data-ttu-id="f6dfd-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f6dfd-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dfd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6dfd-122">-DefaultProfile</span></span>
<span data-ttu-id="f6dfd-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f6dfd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dfd-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f6dfd-124">-Id</span></span>
<span data-ttu-id="f6dfd-125">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6dfd-126">-Information</span><span class="sxs-lookup"><span data-stu-id="f6dfd-126">-InformationAction</span></span>
<span data-ttu-id="f6dfd-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f6dfd-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f6dfd-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6dfd-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="f6dfd-129">Continue</span></span>
- <span data-ttu-id="f6dfd-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="f6dfd-130">Ignore</span></span>
- <span data-ttu-id="f6dfd-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="f6dfd-131">Inquire</span></span>
- <span data-ttu-id="f6dfd-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f6dfd-132">SilentlyContinue</span></span>
- <span data-ttu-id="f6dfd-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="f6dfd-133">Stop</span></span>
- <span data-ttu-id="f6dfd-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="f6dfd-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dfd-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f6dfd-135">-InformationVariable</span></span>
<span data-ttu-id="f6dfd-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dfd-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f6dfd-137">-Name</span></span>
<span data-ttu-id="f6dfd-138">Gibt den Namen der Richtlinien Aufgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6dfd-139">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f6dfd-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="f6dfd-140">Gibt die ID der Richtliniendefinition für die Richtlinienzuweisungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6dfd-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="f6dfd-141">-Pre</span></span>
<span data-ttu-id="f6dfd-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dfd-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="f6dfd-143">-Scope</span></span>
<span data-ttu-id="f6dfd-144">Gibt den Bereich an, auf dem die Richtlinie für die Aufgabe angewendet wird, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6dfd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6dfd-145">CommonParameters</span></span>
<span data-ttu-id="f6dfd-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6dfd-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6dfd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6dfd-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6dfd-148">INPUTS</span></span>

### <span data-ttu-id="f6dfd-149">Keine</span><span class="sxs-lookup"><span data-stu-id="f6dfd-149">None</span></span>
<span data-ttu-id="f6dfd-150">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f6dfd-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6dfd-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6dfd-151">OUTPUTS</span></span>

### <span data-ttu-id="f6dfd-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f6dfd-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f6dfd-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6dfd-153">NOTES</span></span>

## <span data-ttu-id="f6dfd-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6dfd-154">RELATED LINKS</span></span>

[<span data-ttu-id="f6dfd-155">Neu – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f6dfd-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f6dfd-156">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f6dfd-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f6dfd-157">Satz-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f6dfd-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


