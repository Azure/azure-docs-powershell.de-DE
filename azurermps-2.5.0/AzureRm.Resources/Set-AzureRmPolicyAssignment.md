---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: dc54d84886bc9c13fa6a4ecef4e41ef80fa6d4e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849040"
---
# <span data-ttu-id="459fd-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="459fd-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="459fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="459fd-102">SYNOPSIS</span></span>
<span data-ttu-id="459fd-103">Ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="459fd-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="459fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="459fd-104">SYNTAX</span></span>

### <span data-ttu-id="459fd-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="459fd-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="459fd-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="459fd-106">IdParameterSet</span></span>
```
Set-AzureRmPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="459fd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="459fd-107">DESCRIPTION</span></span>
<span data-ttu-id="459fd-108">Das Cmdlet " **festlegen-AzureRmPolicyAssignment** " ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="459fd-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="459fd-109">Geben Sie eine Zuordnung nach ID oder nach Name und Bereich an.</span><span class="sxs-lookup"><span data-stu-id="459fd-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="459fd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="459fd-110">EXAMPLES</span></span>

### <span data-ttu-id="459fd-111">Beispiel 1: Aktualisieren des Anzeigenamens</span><span class="sxs-lookup"><span data-stu-id="459fd-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="459fd-112">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="459fd-113">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="459fd-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="459fd-114">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen PolicyAssignment mithilfe des Get-AzureRmPolicyAssignment-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="459fd-115">Der Befehl speichert das Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="459fd-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="459fd-116">Der endgültige Befehl aktualisiert den Anzeigenamen in der Richtlinienzuweisung in der Ressourcengruppe, die von der Eigenschaft " **Resourcen** -Wert" von $ResourceGroup angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="459fd-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="459fd-117">Beispiel 2: Hinzufügen einer verwalteten Identität zur Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="459fd-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="459fd-118">Der erste Befehl ruft mithilfe des Get-AzureRmPolicyAssignment-Cmdlets die Richtlinienzuweisung mit dem Namen PolicyAssignment aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="459fd-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="459fd-119">Der Befehl speichert das Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="459fd-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="459fd-120">Der endgültige Befehl weist der Richtlinienzuweisung eine verwaltete Identität zu.</span><span class="sxs-lookup"><span data-stu-id="459fd-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="459fd-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="459fd-121">PARAMETERS</span></span>

### <span data-ttu-id="459fd-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="459fd-122">-ApiVersion</span></span>
<span data-ttu-id="459fd-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="459fd-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="459fd-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="459fd-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="459fd-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="459fd-125">-AssignIdentity</span></span>
<span data-ttu-id="459fd-126">Generieren Sie eine Azure Active Directory-Identität für diese Richtlinienzuweisung, und weisen Sie diese zu.</span><span class="sxs-lookup"><span data-stu-id="459fd-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="459fd-127">Die Identität wird verwendet, wenn Bereitstellungen für "deployIfNotExists"-Richtlinien ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="459fd-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="459fd-128">Beim Zuweisen einer Identität ist ein Speicherort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="459fd-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="459fd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459fd-129">-DefaultProfile</span></span>
<span data-ttu-id="459fd-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="459fd-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="459fd-131">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="459fd-131">-Description</span></span>
<span data-ttu-id="459fd-132">Die Beschreibung für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="459fd-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="459fd-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="459fd-133">-DisplayName</span></span>
<span data-ttu-id="459fd-134">Gibt einen neuen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="459fd-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="459fd-135">-ID</span><span class="sxs-lookup"><span data-stu-id="459fd-135">-Id</span></span>
<span data-ttu-id="459fd-136">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="459fd-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="459fd-137">-Information</span><span class="sxs-lookup"><span data-stu-id="459fd-137">-InformationAction</span></span>
<span data-ttu-id="459fd-138">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="459fd-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="459fd-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="459fd-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="459fd-140">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="459fd-140">Continue</span></span>
- <span data-ttu-id="459fd-141">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="459fd-141">Ignore</span></span>
- <span data-ttu-id="459fd-142">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="459fd-142">Inquire</span></span>
- <span data-ttu-id="459fd-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="459fd-143">SilentlyContinue</span></span>
- <span data-ttu-id="459fd-144">Beenden</span><span class="sxs-lookup"><span data-stu-id="459fd-144">Stop</span></span>
- <span data-ttu-id="459fd-145">Anhalten</span><span class="sxs-lookup"><span data-stu-id="459fd-145">Suspend</span></span>

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

### <span data-ttu-id="459fd-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="459fd-146">-InformationVariable</span></span>
<span data-ttu-id="459fd-147">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="459fd-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="459fd-148">-Standort</span><span class="sxs-lookup"><span data-stu-id="459fd-148">-Location</span></span>
<span data-ttu-id="459fd-149">Der Speicherort der Ressourcen Identität der Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="459fd-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="459fd-150">Dies ist erforderlich, wenn der-AssignIdentity-Schalter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="459fd-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="459fd-151">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="459fd-151">-Metadata</span></span>
<span data-ttu-id="459fd-152">Die aktualisierten Metadaten für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="459fd-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="459fd-153">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="459fd-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="459fd-154">-Name</span><span class="sxs-lookup"><span data-stu-id="459fd-154">-Name</span></span>
<span data-ttu-id="459fd-155">Gibt den Namen der Richtlinien Aufgabe an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="459fd-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="459fd-156">-NotScope</span></span>
<span data-ttu-id="459fd-157">Die Richtlinienzuweisung nicht Bereiche.</span><span class="sxs-lookup"><span data-stu-id="459fd-157">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-158">-Pre</span><span class="sxs-lookup"><span data-stu-id="459fd-158">-Pre</span></span>
<span data-ttu-id="459fd-159">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="459fd-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="459fd-160">-Scope</span><span class="sxs-lookup"><span data-stu-id="459fd-160">-Scope</span></span>
<span data-ttu-id="459fd-161">Gibt den Bereich an, auf dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="459fd-161">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-162">-SKU</span><span class="sxs-lookup"><span data-stu-id="459fd-162">-Sku</span></span>
<span data-ttu-id="459fd-163">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="459fd-163">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="459fd-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459fd-164">CommonParameters</span></span>
<span data-ttu-id="459fd-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="459fd-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459fd-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="459fd-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459fd-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="459fd-167">INPUTS</span></span>

## <span data-ttu-id="459fd-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="459fd-168">OUTPUTS</span></span>

## <span data-ttu-id="459fd-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="459fd-169">NOTES</span></span>

## <span data-ttu-id="459fd-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="459fd-170">RELATED LINKS</span></span>

[<span data-ttu-id="459fd-171">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="459fd-171">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="459fd-172">Neu – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="459fd-172">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="459fd-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="459fd-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


