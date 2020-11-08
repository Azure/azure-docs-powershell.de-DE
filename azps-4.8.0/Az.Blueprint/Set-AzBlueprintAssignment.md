---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165306"
---
# <span data-ttu-id="9d192-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="9d192-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="9d192-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d192-102">SYNOPSIS</span></span>
<span data-ttu-id="9d192-103">Aktualisieren einer vorhandenen Blueprint-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="9d192-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="9d192-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d192-104">SYNTAX</span></span>

### <span data-ttu-id="9d192-105">UpdateBlueprintAssignment (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d192-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d192-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="9d192-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d192-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d192-107">DESCRIPTION</span></span>
<span data-ttu-id="9d192-108">Aktualisieren einer vorhandenen Blueprint-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="9d192-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="9d192-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d192-109">EXAMPLES</span></span>

### <span data-ttu-id="9d192-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d192-110">Example 1</span></span>
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

<span data-ttu-id="9d192-111">Aktualisieren Sie eine vorhandene Blueprint-Zuordnung der Blueprint `$blueprintObject` -Definition innerhalb des angegebenen Abonnements, und aktualisieren Sie die Parameter.</span><span class="sxs-lookup"><span data-stu-id="9d192-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="9d192-112">Verwendet die vom System zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="9d192-112">Uses system-assigned identity.</span></span> <span data-ttu-id="9d192-113">Der Speicherort definiert den Bereich zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="9d192-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="9d192-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9d192-114">Example 2</span></span>
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

<span data-ttu-id="9d192-115">Aktualisieren einer vorhandenen Blueprint-Zuordnung über eine Zuordnungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d192-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="9d192-116">Das Format der Zuordnungsdatei finden Sie in den Beispielen für Anforderung/Antwort unter: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="9d192-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="9d192-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9d192-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="9d192-118">Aktualisieren einer vorhandenen Blueprint-Zuordnung der Blueprint-Definition `$blueprintObject` , die auf das angegebene Abonnement in der angegebenen Verwaltungsgruppe mit dem definierten Parameter ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="9d192-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="9d192-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d192-119">PARAMETERS</span></span>

### <span data-ttu-id="9d192-120">-Zuordnungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d192-120">-AssignmentFile</span></span>
<span data-ttu-id="9d192-121">Der Speicherort der Zuordnungsdatei im JSON-Format auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="9d192-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="9d192-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="9d192-122">-Blueprint</span></span>
<span data-ttu-id="9d192-123">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="9d192-123">Blueprint object.</span></span>

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

### <span data-ttu-id="9d192-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d192-124">-DefaultProfile</span></span>
<span data-ttu-id="9d192-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d192-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d192-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="9d192-126">-Location</span></span>
<span data-ttu-id="9d192-127">Der Bereich, in dem die verwaltete Identität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d192-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="9d192-128">Weitere Informationen finden Sie unter aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="9d192-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="9d192-129">-Sperre</span><span class="sxs-lookup"><span data-stu-id="9d192-129">-Lock</span></span>
<span data-ttu-id="9d192-130">Sperren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9d192-130">Lock resources.</span></span>
<span data-ttu-id="9d192-131">Weitere Informationen finden Sie unter aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="9d192-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="9d192-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="9d192-132">-ManagementGroupId</span></span>
<span data-ttu-id="9d192-133">Die ID der Verwaltungsgruppe, in der die Blueprint-Zuweisung (en) gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d192-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="9d192-134">-Name</span><span class="sxs-lookup"><span data-stu-id="9d192-134">-Name</span></span>
<span data-ttu-id="9d192-135">Blueprint-Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="9d192-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="9d192-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9d192-136">-Parameter</span></span>
<span data-ttu-id="9d192-137">Artefakt-Parameter</span><span class="sxs-lookup"><span data-stu-id="9d192-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="9d192-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="9d192-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="9d192-139">Hashtable mit Parametern, die an das Artefakt der Ressourcengruppe übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9d192-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="9d192-140">-SecureString</span><span class="sxs-lookup"><span data-stu-id="9d192-140">-SecureStringParameter</span></span>
<span data-ttu-id="9d192-141">Sicherer Zeichenfolgenparameter für keyvault-Ressourcen-ID, Name und Version.</span><span class="sxs-lookup"><span data-stu-id="9d192-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="9d192-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9d192-142">-SubscriptionId</span></span>
<span data-ttu-id="9d192-143">Abonnement-Nr, um den Blueprint zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9d192-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="9d192-144">Dies kann eine durch trennzeichengetrennte Liste von Abonnement-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="9d192-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="9d192-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9d192-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="9d192-146">System zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d192-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="9d192-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9d192-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="9d192-148">Benutzer zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d192-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="9d192-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9d192-149">-Confirm</span></span>
<span data-ttu-id="9d192-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d192-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d192-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d192-151">-WhatIf</span></span>
<span data-ttu-id="9d192-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d192-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d192-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d192-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d192-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d192-154">CommonParameters</span></span>
<span data-ttu-id="9d192-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d192-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d192-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d192-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d192-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d192-157">INPUTS</span></span>

### <span data-ttu-id="9d192-158">System. String</span><span class="sxs-lookup"><span data-stu-id="9d192-158">System.String</span></span>

### <span data-ttu-id="9d192-159">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="9d192-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="9d192-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="9d192-160">System.String[]</span></span>

### <span data-ttu-id="9d192-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9d192-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9d192-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d192-162">OUTPUTS</span></span>

### <span data-ttu-id="9d192-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="9d192-163">System.Object</span></span>
## <span data-ttu-id="9d192-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d192-164">NOTES</span></span>

## <span data-ttu-id="9d192-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d192-165">RELATED LINKS</span></span>
