---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291239"
---
# <span data-ttu-id="86053-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="86053-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="86053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86053-102">SYNOPSIS</span></span>
<span data-ttu-id="86053-103">Aktualisieren Sie eine vorhandene Blaupausenaufgabe.</span><span class="sxs-lookup"><span data-stu-id="86053-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="86053-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86053-104">SYNTAX</span></span>

### <span data-ttu-id="86053-105">UpdateBlueprintAssignment (Standard)</span><span class="sxs-lookup"><span data-stu-id="86053-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86053-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="86053-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86053-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86053-107">DESCRIPTION</span></span>
<span data-ttu-id="86053-108">Aktualisieren Sie eine vorhandene Blaupausenaufgabe.</span><span class="sxs-lookup"><span data-stu-id="86053-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="86053-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86053-109">EXAMPLES</span></span>

### <span data-ttu-id="86053-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86053-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="86053-111">Aktualisieren Sie eine vorhandene Blaupausenzuordnung der Blaupausendefinition innerhalb `$blueprintObject` des angegebenen Abonnements, und aktualisieren Sie die Parameter.</span><span class="sxs-lookup"><span data-stu-id="86053-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="86053-112">Verwendet die vom System zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="86053-112">Uses system-assigned identity.</span></span> <span data-ttu-id="86053-113">Der Speicherort definiert die Region zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="86053-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="86053-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="86053-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="86053-115">Aktualisieren Einer vorhandenen Blaupausenzuordnung mithilfe einer Aufgabendatei.</span><span class="sxs-lookup"><span data-stu-id="86053-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="86053-116">Das Format der Aufgabendatei finden Sie in den Beispielen für Anfragen/Antworten unter: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="86053-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="86053-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="86053-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="86053-118">Aktualisieren Sie eine vorhandene Blaupausenzuordnung der Blaupausendefinition, die auf das angegebene Abonnement in der angegebenen Verwaltungsgruppe abzielt, mithilfe `$blueprintObject` des definierten Parameters.</span><span class="sxs-lookup"><span data-stu-id="86053-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="86053-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86053-119">PARAMETERS</span></span>

### <span data-ttu-id="86053-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="86053-120">-AssignmentFile</span></span>
<span data-ttu-id="86053-121">Speicherort der Zuweisungsdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="86053-121">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86053-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="86053-122">-Blueprint</span></span>
<span data-ttu-id="86053-123">"Blueprint"-Objekt.</span><span class="sxs-lookup"><span data-stu-id="86053-123">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86053-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86053-124">-DefaultProfile</span></span>
<span data-ttu-id="86053-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86053-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86053-126">-Location</span><span class="sxs-lookup"><span data-stu-id="86053-126">-Location</span></span>
<span data-ttu-id="86053-127">Region für verwaltete Identität, in der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="86053-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="86053-128">Weitere Informationen zur aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="86053-128">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86053-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="86053-129">-Lock</span></span>
<span data-ttu-id="86053-130">Sperren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="86053-130">Lock resources.</span></span>
<span data-ttu-id="86053-131">Weitere Informationen zu aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="86053-131">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: UpdateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86053-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="86053-132">-ManagementGroupId</span></span>
<span data-ttu-id="86053-133">Die ID der Verwaltungsgruppe, in der die Blaupausenzuweisung(en) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="86053-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86053-134">-Name</span><span class="sxs-lookup"><span data-stu-id="86053-134">-Name</span></span>
<span data-ttu-id="86053-135">Name der Blaupause.</span><span class="sxs-lookup"><span data-stu-id="86053-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86053-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="86053-136">-Parameter</span></span>
<span data-ttu-id="86053-137">Parameter "Artefakt".</span><span class="sxs-lookup"><span data-stu-id="86053-137">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86053-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="86053-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="86053-139">Hashtable der Parameter, die an das Ressourcengruppenartefakt übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="86053-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86053-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="86053-140">-SecureStringParameter</span></span>
<span data-ttu-id="86053-141">Sicherer Zeichenfolgenparameter für die KeyVault-Ressourcen-ID, den Namen und die Version.</span><span class="sxs-lookup"><span data-stu-id="86053-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86053-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86053-142">-SubscriptionId</span></span>
<span data-ttu-id="86053-143">SubscriptionId zum Zuweisen der Blaupause.</span><span class="sxs-lookup"><span data-stu-id="86053-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="86053-144">Kann eine durch Trennzeichen getrennte Liste von "subscriptionId"-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="86053-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86053-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="86053-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="86053-146">Die vom System zugewiesene Identität (MSI) zum Bereitstellen der Artefakte.</span><span class="sxs-lookup"><span data-stu-id="86053-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86053-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="86053-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="86053-148">Die vom Benutzer zugewiesene Identität (User Assigned Identity, MSI) zum Bereitstellen der Artefakte.</span><span class="sxs-lookup"><span data-stu-id="86053-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86053-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86053-149">-Confirm</span></span>
<span data-ttu-id="86053-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86053-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86053-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="86053-151">-WhatIf</span></span>
<span data-ttu-id="86053-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86053-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86053-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86053-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86053-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86053-154">CommonParameters</span></span>
<span data-ttu-id="86053-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86053-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86053-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86053-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86053-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86053-157">INPUTS</span></span>

### <span data-ttu-id="86053-158">System.String</span><span class="sxs-lookup"><span data-stu-id="86053-158">System.String</span></span>

### <span data-ttu-id="86053-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="86053-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="86053-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="86053-160">System.String[]</span></span>

### <span data-ttu-id="86053-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="86053-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="86053-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86053-162">OUTPUTS</span></span>

### <span data-ttu-id="86053-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="86053-163">System.Object</span></span>
## <span data-ttu-id="86053-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="86053-164">NOTES</span></span>

## <span data-ttu-id="86053-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="86053-165">RELATED LINKS</span></span>
