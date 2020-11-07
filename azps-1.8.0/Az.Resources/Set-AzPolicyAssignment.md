---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 2b699219281d64e50694f7e7dd70a965626f7132
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659522"
---
# <span data-ttu-id="a5987-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a5987-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="a5987-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5987-102">SYNOPSIS</span></span>
<span data-ttu-id="a5987-103">Ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="a5987-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="a5987-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5987-104">SYNTAX</span></span>

### <span data-ttu-id="a5987-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5987-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5987-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5987-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5987-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5987-107">DESCRIPTION</span></span>
<span data-ttu-id="a5987-108">Das Cmdlet " **festlegen-AzPolicyAssignment** " ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="a5987-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="a5987-109">Geben Sie eine Zuordnung nach ID oder nach Name und Bereich an.</span><span class="sxs-lookup"><span data-stu-id="a5987-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="a5987-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5987-110">EXAMPLES</span></span>

### <span data-ttu-id="a5987-111">Beispiel 1: Aktualisieren des Anzeigenamens</span><span class="sxs-lookup"><span data-stu-id="a5987-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="a5987-112">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="a5987-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a5987-113">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5987-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a5987-114">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen PolicyAssignment mithilfe des Get-AzPolicyAssignment-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="a5987-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="a5987-115">Der Befehl speichert das Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5987-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="a5987-116">Der endgültige Befehl aktualisiert den Anzeigenamen in der Richtlinienzuweisung in der Ressourcengruppe, die von der Eigenschaft " **Resourcen** -Wert" von $ResourceGroup angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a5987-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="a5987-117">Beispiel 2: Hinzufügen einer verwalteten Identität zur Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="a5987-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="a5987-118">Der erste Befehl ruft mithilfe des Get-AzPolicyAssignment-Cmdlets die Richtlinienzuweisung mit dem Namen PolicyAssignment aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="a5987-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="a5987-119">Der Befehl speichert das Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5987-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="a5987-120">Der endgültige Befehl weist der Richtlinienzuweisung eine verwaltete Identität zu.</span><span class="sxs-lookup"><span data-stu-id="a5987-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="a5987-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5987-121">PARAMETERS</span></span>

### <span data-ttu-id="a5987-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a5987-122">-ApiVersion</span></span>
<span data-ttu-id="a5987-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="a5987-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a5987-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="a5987-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a5987-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a5987-125">-AssignIdentity</span></span>
<span data-ttu-id="a5987-126">Generieren Sie eine Azure Active Directory-Identität für diese Richtlinienzuweisung, und weisen Sie diese zu.</span><span class="sxs-lookup"><span data-stu-id="a5987-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="a5987-127">Die Identität wird verwendet, wenn Bereitstellungen für "deployIfNotExists"-Richtlinien ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a5987-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="a5987-128">Beim Zuweisen einer Identität ist ein Speicherort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a5987-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="a5987-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5987-129">-DefaultProfile</span></span>
<span data-ttu-id="a5987-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a5987-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5987-131">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5987-131">-Description</span></span>
<span data-ttu-id="a5987-132">Die Beschreibung für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="a5987-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="a5987-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a5987-133">-DisplayName</span></span>
<span data-ttu-id="a5987-134">Gibt einen neuen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="a5987-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="a5987-135">-ID</span><span class="sxs-lookup"><span data-stu-id="a5987-135">-Id</span></span>
<span data-ttu-id="a5987-136">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a5987-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a5987-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="a5987-137">-Location</span></span>
<span data-ttu-id="a5987-138">Der Speicherort der Ressourcen Identität der Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="a5987-138">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="a5987-139">Dies ist erforderlich, wenn der-AssignIdentity-Schalter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5987-139">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="a5987-140">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="a5987-140">-Metadata</span></span>
<span data-ttu-id="a5987-141">Die aktualisierten Metadaten für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="a5987-141">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="a5987-142">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a5987-142">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="a5987-143">-Name</span><span class="sxs-lookup"><span data-stu-id="a5987-143">-Name</span></span>
<span data-ttu-id="a5987-144">Gibt den Namen der Richtlinien Aufgabe an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a5987-144">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a5987-145">-NotScope</span><span class="sxs-lookup"><span data-stu-id="a5987-145">-NotScope</span></span>
<span data-ttu-id="a5987-146">Die Richtlinienzuweisung nicht Bereiche.</span><span class="sxs-lookup"><span data-stu-id="a5987-146">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="a5987-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="a5987-147">-Pre</span></span>
<span data-ttu-id="a5987-148">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a5987-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a5987-149">-Scope</span><span class="sxs-lookup"><span data-stu-id="a5987-149">-Scope</span></span>
<span data-ttu-id="a5987-150">Gibt den Bereich an, auf dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5987-150">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="a5987-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5987-151">CommonParameters</span></span>
<span data-ttu-id="a5987-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5987-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5987-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5987-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5987-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5987-154">INPUTS</span></span>

### <span data-ttu-id="a5987-155">System. String</span><span class="sxs-lookup"><span data-stu-id="a5987-155">System.String</span></span>

### <span data-ttu-id="a5987-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="a5987-156">System.String[]</span></span>

## <span data-ttu-id="a5987-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5987-157">OUTPUTS</span></span>

### <span data-ttu-id="a5987-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a5987-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a5987-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5987-159">NOTES</span></span>

## <span data-ttu-id="a5987-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5987-160">RELATED LINKS</span></span>

[<span data-ttu-id="a5987-161">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a5987-161">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="a5987-162">Neu – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a5987-162">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="a5987-163">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a5987-163">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


