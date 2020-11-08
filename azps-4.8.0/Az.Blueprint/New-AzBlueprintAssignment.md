---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 295e70d91af0c6c06ac913c10bfe5a9e265523c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008106"
---
# <span data-ttu-id="fd392-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="fd392-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="fd392-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd392-102">SYNOPSIS</span></span>
<span data-ttu-id="fd392-103">Weisen Sie einem Abonnement oder einer Verwaltungsgruppe eine Blueprint-Definition zu.</span><span class="sxs-lookup"><span data-stu-id="fd392-103">Assign a blueprint definition to a subscription or a management group.</span></span>

## <span data-ttu-id="fd392-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd392-104">SYNTAX</span></span>

### <span data-ttu-id="fd392-105">CreateBlueprintAssignment (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd392-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd392-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="fd392-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd392-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd392-107">DESCRIPTION</span></span>
<span data-ttu-id="fd392-108">Zuweisen einer Blueprint-Definition zu einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="fd392-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="fd392-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd392-109">EXAMPLES</span></span>

### <span data-ttu-id="fd392-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd392-110">Example 1</span></span>
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

<span data-ttu-id="fd392-111">Erstellen Sie eine neue Blueprint-Zuweisung der Blueprint-Definition `$blueprintObject` innerhalb des angegebenen Abonnements unter Verwendung des definierten Parameters und des Ressourcengruppen Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="fd392-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="fd392-112">Verwendet die vom System zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="fd392-112">Uses system-assigned identity.</span></span> <span data-ttu-id="fd392-113">Der Speicherort definiert den Bereich zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="fd392-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="fd392-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fd392-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="fd392-115">Erstellen Sie eine neue Blueprint-Zuweisung der Blueprint-Definition `$blueprintObject` innerhalb des angegebenen Abonnements mithilfe des definierten Parameters und des Ressourcengruppen Wörterbuchs, und konfigurieren Sie die Ressourcen Sperrung für **allresources**.</span><span class="sxs-lookup"><span data-stu-id="fd392-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="fd392-116">Standardmäßig wird die vom System zugewiesene Identität verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd392-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="fd392-117">Der Speicherort definiert den Bereich zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="fd392-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="fd392-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fd392-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="fd392-119">Erstellen Sie eine neue Blueprint-Zuweisung der Blueprint-Definition `$blueprintObject` innerhalb des angegebenen Abonnements unter Verwendung des definierten Parameters und des Ressourcengruppen Wörterbuchs unter Verwendung der angegebenen vom Benutzer zugewiesenen Identitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="fd392-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="fd392-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="fd392-120">Example 4</span></span>
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

<span data-ttu-id="fd392-121">Erstellen einer Blueprint-Zuordnung über eine Zuordnungsdatei</span><span class="sxs-lookup"><span data-stu-id="fd392-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="fd392-122">Das Format der Zuordnungsdatei finden Sie in den Beispielen für Anforderung/Antwort unter: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="fd392-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="fd392-123">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="fd392-123">Example 5</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "myManagementGroup" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="fd392-124">Erstellen Sie eine neue Blueprint-Zuordnung der Blueprint-Definition `$blueprintObject` , die auf das angegebene Abonnement in der angegebenen Verwaltungsgruppe mit dem definierten Parameter ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="fd392-124">Create a new blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="fd392-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd392-125">PARAMETERS</span></span>

### <span data-ttu-id="fd392-126">-Zuordnungsdatei</span><span class="sxs-lookup"><span data-stu-id="fd392-126">-AssignmentFile</span></span>
<span data-ttu-id="fd392-127">Der Speicherort der Zuordnungsdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="fd392-127">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="fd392-128">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="fd392-128">-Blueprint</span></span>
<span data-ttu-id="fd392-129">Blueprint-Definitionsobjekt</span><span class="sxs-lookup"><span data-stu-id="fd392-129">Blueprint definition object.</span></span>

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

### <span data-ttu-id="fd392-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd392-130">-DefaultProfile</span></span>
<span data-ttu-id="fd392-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd392-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd392-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="fd392-132">-Location</span></span>
<span data-ttu-id="fd392-133">Der Bereich, in dem die verwaltete Identität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd392-133">Region for managed identity to be created in.</span></span>
<span data-ttu-id="fd392-134">Weitere Informationen finden Sie unter aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="fd392-134">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="fd392-135">-Sperre</span><span class="sxs-lookup"><span data-stu-id="fd392-135">-Lock</span></span>
<span data-ttu-id="fd392-136">Sperren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fd392-136">Lock resources.</span></span>
<span data-ttu-id="fd392-137">Weitere Informationen finden Sie unter aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="fd392-137">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="fd392-138">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="fd392-138">-ManagementGroupId</span></span>
<span data-ttu-id="fd392-139">Die ID der Verwaltungsgruppe, in der die Blueprint-Zuweisung (en) gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd392-139">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="fd392-140">-Name</span><span class="sxs-lookup"><span data-stu-id="fd392-140">-Name</span></span>
<span data-ttu-id="fd392-141">Blueprint-Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="fd392-141">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="fd392-142">-Parameter</span><span class="sxs-lookup"><span data-stu-id="fd392-142">-Parameter</span></span>
<span data-ttu-id="fd392-143">Artefaktparameter.</span><span class="sxs-lookup"><span data-stu-id="fd392-143">Artifact parameters.</span></span>

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

### <span data-ttu-id="fd392-144">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="fd392-144">-ResourceGroupParameter</span></span>
<span data-ttu-id="fd392-145">Hashtable mit Parametern, die an das Artefakt der Ressourcengruppe übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fd392-145">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="fd392-146">-SecureString</span><span class="sxs-lookup"><span data-stu-id="fd392-146">-SecureStringParameter</span></span>
<span data-ttu-id="fd392-147">Sicherer Zeichenfolgenparameter für keyvault-Ressourcen-ID, Name und Version.</span><span class="sxs-lookup"><span data-stu-id="fd392-147">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="fd392-148">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fd392-148">-SubscriptionId</span></span>
<span data-ttu-id="fd392-149">Abonnement-ID, um die Blueprint-Definition zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="fd392-149">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="fd392-150">Dies kann eine durch trennzeichengetrennte Liste von Abonnement-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="fd392-150">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="fd392-151">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fd392-151">-SystemAssignedIdentity</span></span>
<span data-ttu-id="fd392-152">System zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fd392-152">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="fd392-153">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fd392-153">-UserAssignedIdentity</span></span>
<span data-ttu-id="fd392-154">Benutzer zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fd392-154">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="fd392-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd392-155">-Confirm</span></span>
<span data-ttu-id="fd392-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd392-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd392-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd392-157">-WhatIf</span></span>
<span data-ttu-id="fd392-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd392-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd392-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd392-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd392-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd392-160">CommonParameters</span></span>
<span data-ttu-id="fd392-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd392-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd392-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd392-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd392-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd392-163">INPUTS</span></span>

### <span data-ttu-id="fd392-164">System. String</span><span class="sxs-lookup"><span data-stu-id="fd392-164">System.String</span></span>

### <span data-ttu-id="fd392-165">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="fd392-165">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="fd392-166">System. String []</span><span class="sxs-lookup"><span data-stu-id="fd392-166">System.String[]</span></span>

### <span data-ttu-id="fd392-167">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd392-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fd392-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd392-168">OUTPUTS</span></span>

### <span data-ttu-id="fd392-169">System. Object</span><span class="sxs-lookup"><span data-stu-id="fd392-169">System.Object</span></span>
## <span data-ttu-id="fd392-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd392-170">NOTES</span></span>

## <span data-ttu-id="fd392-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd392-171">RELATED LINKS</span></span>
