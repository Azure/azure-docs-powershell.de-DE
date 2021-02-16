---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149180"
---
# <span data-ttu-id="ad623-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="ad623-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="ad623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad623-102">SYNOPSIS</span></span>
<span data-ttu-id="ad623-103">Weisen Sie einem Abonnement oder einer Managementgruppe eine Blaupausendefinition zu.</span><span class="sxs-lookup"><span data-stu-id="ad623-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="ad623-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad623-104">SYNTAX</span></span>

### <span data-ttu-id="ad623-105">CreateBlueprintAssignment (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad623-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad623-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="ad623-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad623-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad623-107">DESCRIPTION</span></span>
<span data-ttu-id="ad623-108">Weisen Sie einem Abonnement eine Blaupausendefinition zu.</span><span class="sxs-lookup"><span data-stu-id="ad623-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="ad623-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ad623-109">EXAMPLES</span></span>

### <span data-ttu-id="ad623-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad623-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="ad623-111">Erstellen Sie eine neue Blaupausenzuordnung der Blaupausendefinition innerhalb des angegebenen Abonnements mithilfe des definierten Parameters und `$blueprintObject` Ressourcengruppenwörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="ad623-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="ad623-112">Verwendet die vom System zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="ad623-112">Uses system-assigned identity.</span></span> <span data-ttu-id="ad623-113">Der Speicherort definiert die Region zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="ad623-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="ad623-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ad623-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="ad623-115">Erstellen Sie eine neue Blaupausenzuordnung der Blaupausendefinition innerhalb des angegebenen Abonnements mit dem definierten Parameter- und Ressourcengruppenwörterbuch, und konfigurieren Sie die Ressourcensperre für `$blueprintObject` **AllResources.**</span><span class="sxs-lookup"><span data-stu-id="ad623-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="ad623-116">Standardmäßig wird die vom System zugewiesene Identität verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad623-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="ad623-117">Der Speicherort definiert die Region zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="ad623-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="ad623-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ad623-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="ad623-119">Erstellen Sie eine neue Blaupausenzuordnung der Blaupausendefinition innerhalb des angegebenen Abonnements, indem Sie den definierten Parameter und das Ressourcengruppenwörterbuch mit der angegebenen vom Benutzer `$blueprintObject` zugewiesenen Identitäts-ID verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad623-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="ad623-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ad623-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="ad623-121">Erstellen Sie eine Blaupausenaufgabe mithilfe einer Aufgabendatei.</span><span class="sxs-lookup"><span data-stu-id="ad623-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="ad623-122">Das Format der Aufgabendatei finden Sie in den Beispielen für Anfragen/Antworten unter: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="ad623-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="ad623-123">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="ad623-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="ad623-124">Erstellen Sie mithilfe des definierten Parameters eine neue Blaupausenzuordnung der Blaupausendefinition für das angegebene Abonnement in der `$blueprintObject` angegebenen Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ad623-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="ad623-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad623-125">PARAMETERS</span></span>

### <span data-ttu-id="ad623-126">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="ad623-126">-AssignmentFile</span></span>
<span data-ttu-id="ad623-127">Speicherort der Zuweisungsdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="ad623-127">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-128">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="ad623-128">-Blueprint</span></span>
<span data-ttu-id="ad623-129">Entwurfsdefinitionsobjekt</span><span class="sxs-lookup"><span data-stu-id="ad623-129">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad623-130">-DefaultProfile</span></span>
<span data-ttu-id="ad623-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad623-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad623-132">-Location</span><span class="sxs-lookup"><span data-stu-id="ad623-132">-Location</span></span>
<span data-ttu-id="ad623-133">Region für verwaltete Identität, in der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad623-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="ad623-134">Weitere Informationen zur aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="ad623-134">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-135">-Lock</span><span class="sxs-lookup"><span data-stu-id="ad623-135">-Lock</span></span>
<span data-ttu-id="ad623-136">Sperren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ad623-136">Lock resources.</span></span>
<span data-ttu-id="ad623-137">Weitere Informationen zu aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="ad623-137">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: CreateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ad623-138">-ManagementGroupId</span></span>
<span data-ttu-id="ad623-139">Die ID der Verwaltungsgruppe, in der die Blaupausenzuweisung(en) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ad623-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-140">-Name</span><span class="sxs-lookup"><span data-stu-id="ad623-140">-Name</span></span>
<span data-ttu-id="ad623-141">Name der Blaupause.</span><span class="sxs-lookup"><span data-stu-id="ad623-141">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ad623-142">-Parameter</span></span>
<span data-ttu-id="ad623-143">Artefaktparameter.</span><span class="sxs-lookup"><span data-stu-id="ad623-143">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="ad623-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="ad623-145">Hashtable der Parameter, die an das Ressourcengruppenartefakt übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad623-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-146">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="ad623-146">-SecureStringParameter</span></span>
<span data-ttu-id="ad623-147">Sicherer Zeichenfolgenparameter für die KeyVault-Ressourcen-ID, den Namen und die Version.</span><span class="sxs-lookup"><span data-stu-id="ad623-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad623-148">-SubscriptionId</span></span>
<span data-ttu-id="ad623-149">Abonnement-ID zum Zuweisen der Entwurfsdefinition.</span><span class="sxs-lookup"><span data-stu-id="ad623-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="ad623-150">Kann eine durch Trennzeichen getrennte Liste von "subscriptionId"-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="ad623-150">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: CreateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ad623-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="ad623-152">Vom System zugewiesene Identität (MSI), um die Artefakte zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ad623-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ad623-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="ad623-154">Vom Benutzer zugewiesene Identität (User Assigned Identity, MSI), um die Artefakte zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ad623-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad623-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad623-155">-Confirm</span></span>
<span data-ttu-id="ad623-156">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad623-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad623-157">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ad623-157">-WhatIf</span></span>
<span data-ttu-id="ad623-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad623-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad623-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad623-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad623-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad623-160">CommonParameters</span></span>
<span data-ttu-id="ad623-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad623-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad623-162">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad623-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad623-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ad623-163">INPUTS</span></span>

### <span data-ttu-id="ad623-164">System.String</span><span class="sxs-lookup"><span data-stu-id="ad623-164">System.String</span></span>

### <span data-ttu-id="ad623-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="ad623-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="ad623-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ad623-166">System.String[]</span></span>

### <span data-ttu-id="ad623-167">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad623-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad623-168">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ad623-168">OUTPUTS</span></span>

### <span data-ttu-id="ad623-169">System.Object</span><span class="sxs-lookup"><span data-stu-id="ad623-169">System.Object</span></span>
## <span data-ttu-id="ad623-170">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ad623-170">NOTES</span></span>

## <span data-ttu-id="ad623-171">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ad623-171">RELATED LINKS</span></span>
