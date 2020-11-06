---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: fcb1283531b35365cc8c07016c839a1152011160
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481606"
---
# <span data-ttu-id="f18f2-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f18f2-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="f18f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f18f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f18f2-103">Ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="f18f2-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f18f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f18f2-104">SYNTAX</span></span>

### <span data-ttu-id="f18f2-105">Der Parametersatz für den Richtlinien Zuordnungsnamen.</span><span class="sxs-lookup"><span data-stu-id="f18f2-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="f18f2-106">Standard</span><span class="sxs-lookup"><span data-stu-id="f18f2-106">(Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f18f2-107">Der Parametersatz für die Richtlinien Zuweisungs-ID.</span><span class="sxs-lookup"><span data-stu-id="f18f2-107">The policy assignment Id parameter set.</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f18f2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f18f2-108">DESCRIPTION</span></span>
<span data-ttu-id="f18f2-109">Das Cmdlet " **festlegen-AzureRmPolicyAssignment** " ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="f18f2-109">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="f18f2-110">Geben Sie eine Zuordnung nach ID oder nach Name und Bereich an.</span><span class="sxs-lookup"><span data-stu-id="f18f2-110">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="f18f2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f18f2-111">EXAMPLES</span></span>

### <span data-ttu-id="f18f2-112">Beispiel 1: Aktualisieren des Anzeigenamens</span><span class="sxs-lookup"><span data-stu-id="f18f2-112">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="f18f2-113">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f18f2-113">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="f18f2-114">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="f18f2-114">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f18f2-115">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen PolicyAssignment mithilfe des Get-AzureRmPolicyAssignment-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f18f2-115">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="f18f2-116">Der Befehl speichert das Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="f18f2-116">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="f18f2-117">Der endgültige Befehl aktualisiert den Anzeigenamen in der Richtlinienzuweisung, die von der Eigenschaft " **Resourcen** -Wert" von $PolicyAssignment angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f18f2-117">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="f18f2-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f18f2-118">PARAMETERS</span></span>

### <span data-ttu-id="f18f2-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f18f2-119">-ApiVersion</span></span>
<span data-ttu-id="f18f2-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="f18f2-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f18f2-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="f18f2-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f18f2-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f18f2-122">-DisplayName</span></span>
<span data-ttu-id="f18f2-123">Gibt einen neuen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="f18f2-123">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="f18f2-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f18f2-124">-Id</span></span>
<span data-ttu-id="f18f2-125">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f18f2-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f18f2-126">-Information</span><span class="sxs-lookup"><span data-stu-id="f18f2-126">-InformationAction</span></span>
<span data-ttu-id="f18f2-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="f18f2-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f18f2-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f18f2-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f18f2-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="f18f2-129">Continue</span></span>
- <span data-ttu-id="f18f2-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="f18f2-130">Ignore</span></span>
- <span data-ttu-id="f18f2-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="f18f2-131">Inquire</span></span>
- <span data-ttu-id="f18f2-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f18f2-132">SilentlyContinue</span></span>
- <span data-ttu-id="f18f2-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="f18f2-133">Stop</span></span>
- <span data-ttu-id="f18f2-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="f18f2-134">Suspend</span></span>

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

### <span data-ttu-id="f18f2-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f18f2-135">-InformationVariable</span></span>
<span data-ttu-id="f18f2-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="f18f2-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f18f2-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f18f2-137">-Name</span></span>
<span data-ttu-id="f18f2-138">Gibt den Namen der Richtlinien Aufgabe an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f18f2-138">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f18f2-139">-NotScope</span><span class="sxs-lookup"><span data-stu-id="f18f2-139">-NotScope</span></span>
<span data-ttu-id="f18f2-140">Die Richtlinienzuweisung nicht Bereiche.</span><span class="sxs-lookup"><span data-stu-id="f18f2-140">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f18f2-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="f18f2-141">-Pre</span></span>
<span data-ttu-id="f18f2-142">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f18f2-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f18f2-143">-Scope</span><span class="sxs-lookup"><span data-stu-id="f18f2-143">-Scope</span></span>
<span data-ttu-id="f18f2-144">Gibt den Bereich an, auf dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f18f2-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f18f2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f18f2-145">-DefaultProfile</span></span>
<span data-ttu-id="f18f2-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f18f2-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f18f2-147">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f18f2-147">-Description</span></span>
<span data-ttu-id="f18f2-148">Die Beschreibung für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="f18f2-148">The description for policy assignment.</span></span>

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

### <span data-ttu-id="f18f2-149">-SKU</span><span class="sxs-lookup"><span data-stu-id="f18f2-149">-Sku</span></span>
<span data-ttu-id="f18f2-150">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="f18f2-150">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f18f2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f18f2-151">CommonParameters</span></span>
<span data-ttu-id="f18f2-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f18f2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f18f2-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f18f2-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f18f2-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f18f2-154">INPUTS</span></span>

## <span data-ttu-id="f18f2-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f18f2-155">OUTPUTS</span></span>

### <span data-ttu-id="f18f2-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f18f2-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f18f2-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="f18f2-157">NOTES</span></span>

## <span data-ttu-id="f18f2-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f18f2-158">RELATED LINKS</span></span>

[<span data-ttu-id="f18f2-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f18f2-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f18f2-160">Neu – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f18f2-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f18f2-161">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f18f2-161">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


