---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502458"
---
# <span data-ttu-id="6e526-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6e526-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="6e526-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e526-102">SYNOPSIS</span></span>
<span data-ttu-id="6e526-103">Ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="6e526-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e526-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e526-104">SYNTAX</span></span>

### <span data-ttu-id="6e526-105">SetByPolicyAssignmentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e526-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6e526-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="6e526-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6e526-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e526-107">DESCRIPTION</span></span>
<span data-ttu-id="6e526-108">Das Cmdlet " **festlegen-AzureRmPolicyAssignment** " ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="6e526-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="6e526-109">Geben Sie eine Zuordnung nach ID oder nach Name und Bereich an.</span><span class="sxs-lookup"><span data-stu-id="6e526-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="6e526-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e526-110">EXAMPLES</span></span>

### <span data-ttu-id="6e526-111">Beispiel 1: Aktualisieren des Anzeigenamens</span><span class="sxs-lookup"><span data-stu-id="6e526-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="6e526-112">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="6e526-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="6e526-113">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="6e526-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="6e526-114">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen PolicyAssignment mithilfe des Get-AzureRmPolicyAssignment-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="6e526-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="6e526-115">Der Befehl speichert das Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="6e526-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="6e526-116">Der endgültige Befehl aktualisiert den Anzeigenamen in der Richtlinienzuweisung, die von der Eigenschaft " **Resourcen** -Wert" von $PolicyAssignment angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6e526-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="6e526-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e526-117">PARAMETERS</span></span>

### <span data-ttu-id="6e526-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6e526-118">-ApiVersion</span></span>
<span data-ttu-id="6e526-119">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="6e526-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6e526-120">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="6e526-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6e526-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e526-121">-DefaultProfile</span></span>
<span data-ttu-id="6e526-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6e526-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e526-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e526-123">-Description</span></span>
<span data-ttu-id="6e526-124">Die Beschreibung für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="6e526-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e526-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6e526-125">-DisplayName</span></span>
<span data-ttu-id="6e526-126">Gibt einen neuen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="6e526-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e526-127">-ID</span><span class="sxs-lookup"><span data-stu-id="6e526-127">-Id</span></span>
<span data-ttu-id="6e526-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6e526-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e526-129">-Information</span><span class="sxs-lookup"><span data-stu-id="6e526-129">-InformationAction</span></span>
<span data-ttu-id="6e526-130">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="6e526-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6e526-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6e526-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e526-132">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="6e526-132">Continue</span></span>
- <span data-ttu-id="6e526-133">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="6e526-133">Ignore</span></span>
- <span data-ttu-id="6e526-134">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="6e526-134">Inquire</span></span>
- <span data-ttu-id="6e526-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6e526-135">SilentlyContinue</span></span>
- <span data-ttu-id="6e526-136">Beenden</span><span class="sxs-lookup"><span data-stu-id="6e526-136">Stop</span></span>
- <span data-ttu-id="6e526-137">Anhalten</span><span class="sxs-lookup"><span data-stu-id="6e526-137">Suspend</span></span>

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

### <span data-ttu-id="6e526-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6e526-138">-InformationVariable</span></span>
<span data-ttu-id="6e526-139">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="6e526-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6e526-140">-Name</span><span class="sxs-lookup"><span data-stu-id="6e526-140">-Name</span></span>
<span data-ttu-id="6e526-141">Gibt den Namen der Richtlinien Aufgabe an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6e526-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e526-142">-NotScope</span><span class="sxs-lookup"><span data-stu-id="6e526-142">-NotScope</span></span>
<span data-ttu-id="6e526-143">Die Richtlinienzuweisung nicht Bereiche.</span><span class="sxs-lookup"><span data-stu-id="6e526-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e526-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e526-144">-Pre</span></span>
<span data-ttu-id="6e526-145">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6e526-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6e526-146">-Scope</span><span class="sxs-lookup"><span data-stu-id="6e526-146">-Scope</span></span>
<span data-ttu-id="6e526-147">Gibt den Bereich an, auf dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e526-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e526-148">-SKU</span><span class="sxs-lookup"><span data-stu-id="6e526-148">-Sku</span></span>
<span data-ttu-id="6e526-149">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="6e526-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e526-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e526-150">CommonParameters</span></span>
<span data-ttu-id="6e526-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e526-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e526-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e526-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e526-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e526-153">INPUTS</span></span>

### <span data-ttu-id="6e526-154">Keine</span><span class="sxs-lookup"><span data-stu-id="6e526-154">None</span></span>
<span data-ttu-id="6e526-155">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6e526-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e526-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e526-156">OUTPUTS</span></span>

### <span data-ttu-id="6e526-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6e526-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6e526-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e526-158">NOTES</span></span>

## <span data-ttu-id="6e526-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e526-159">RELATED LINKS</span></span>

[<span data-ttu-id="6e526-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6e526-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6e526-161">Neu – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6e526-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="6e526-162">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6e526-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


