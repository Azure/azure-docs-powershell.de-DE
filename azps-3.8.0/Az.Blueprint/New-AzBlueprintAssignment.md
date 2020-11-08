---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 72c57f8310aaffdbe3c4afa38564c10132539749
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995338"
---
# <span data-ttu-id="08dac-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="08dac-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="08dac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08dac-102">SYNOPSIS</span></span>
<span data-ttu-id="08dac-103">Zuweisen einer Blueprint-Definition zu einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="08dac-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="08dac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08dac-104">SYNTAX</span></span>

### <span data-ttu-id="08dac-105">CreateBlueprintAssignment (Standard)</span><span class="sxs-lookup"><span data-stu-id="08dac-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08dac-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="08dac-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08dac-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08dac-107">DESCRIPTION</span></span>
<span data-ttu-id="08dac-108">Zuweisen einer Blueprint-Definition zu einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="08dac-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="08dac-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08dac-109">EXAMPLES</span></span>

### <span data-ttu-id="08dac-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08dac-110">Example 1</span></span>
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

<span data-ttu-id="08dac-111">Erstellen Sie eine neue Blueprint-Zuweisung der Blueprint-Definition `$blueprintObject` innerhalb des angegebenen Abonnements unter Verwendung des definierten Parameters und des Ressourcengruppen Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="08dac-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="08dac-112">Verwendet die vom System zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="08dac-112">Uses system-assigned identity.</span></span> <span data-ttu-id="08dac-113">Der Speicherort definiert den Bereich zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="08dac-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="08dac-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="08dac-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="08dac-115">Erstellen Sie eine neue Blueprint-Zuweisung der Blueprint-Definition `$blueprintObject` innerhalb des angegebenen Abonnements mithilfe des definierten Parameters und des Ressourcengruppen Wörterbuchs, und konfigurieren Sie die Ressourcen Sperrung für **allresources**.</span><span class="sxs-lookup"><span data-stu-id="08dac-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="08dac-116">Standardmäßig wird die vom System zugewiesene Identität verwendet.</span><span class="sxs-lookup"><span data-stu-id="08dac-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="08dac-117">Der Speicherort definiert den Bereich zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="08dac-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="08dac-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="08dac-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="08dac-119">Erstellen Sie eine neue Blueprint-Zuweisung der Blueprint-Definition `$blueprintObject` innerhalb des angegebenen Abonnements unter Verwendung des definierten Parameters und des Ressourcengruppen Wörterbuchs unter Verwendung der angegebenen vom Benutzer zugewiesenen Identitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="08dac-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="08dac-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="08dac-120">Example 4</span></span>
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

<span data-ttu-id="08dac-121">Erstellen einer Blueprint-Zuordnung über eine Zuordnungsdatei</span><span class="sxs-lookup"><span data-stu-id="08dac-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="08dac-122">Das Format der Zuordnungsdatei finden Sie in den Beispielen für Anforderung/Antwort unter: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="08dac-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="08dac-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="08dac-123">PARAMETERS</span></span>

### <span data-ttu-id="08dac-124">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="08dac-124">-Blueprint</span></span>
<span data-ttu-id="08dac-125">Blueprint-Definitionsobjekt</span><span class="sxs-lookup"><span data-stu-id="08dac-125">Blueprint definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08dac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08dac-126">-DefaultProfile</span></span>
<span data-ttu-id="08dac-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08dac-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08dac-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="08dac-128">-Location</span></span>
<span data-ttu-id="08dac-129">Der Bereich, in dem die verwaltete Identität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08dac-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="08dac-130">Weitere Informationen finden Sie unter aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="08dac-130">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08dac-131">-Sperre</span><span class="sxs-lookup"><span data-stu-id="08dac-131">-Lock</span></span>
<span data-ttu-id="08dac-132">Sperren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="08dac-132">Lock resources.</span></span>
<span data-ttu-id="08dac-133">Weitere Informationen finden Sie unter aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="08dac-133">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08dac-134">-Name</span><span class="sxs-lookup"><span data-stu-id="08dac-134">-Name</span></span>
<span data-ttu-id="08dac-135">Blueprint-Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="08dac-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08dac-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="08dac-136">-Parameter</span></span>
<span data-ttu-id="08dac-137">Artefaktparameter.</span><span class="sxs-lookup"><span data-stu-id="08dac-137">Artifact parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08dac-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="08dac-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="08dac-139">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="08dac-139">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08dac-140">-SecureString</span><span class="sxs-lookup"><span data-stu-id="08dac-140">-SecureStringParameter</span></span>
<span data-ttu-id="08dac-141">Sicherer Zeichenfolgenparameter für keyvault-Ressourcen-ID, Name und Version.</span><span class="sxs-lookup"><span data-stu-id="08dac-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08dac-142">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="08dac-142">-SubscriptionId</span></span>
<span data-ttu-id="08dac-143">Abonnement-ID, um die Blueprint-Definition zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="08dac-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="08dac-144">Dies kann eine durch trennzeichengetrennte Liste von Abonnement-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="08dac-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="08dac-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="08dac-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="08dac-146">System zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="08dac-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="08dac-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="08dac-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="08dac-148">Benutzer zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="08dac-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="08dac-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08dac-149">-Confirm</span></span>
<span data-ttu-id="08dac-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08dac-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08dac-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08dac-151">-WhatIf</span></span>
<span data-ttu-id="08dac-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08dac-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08dac-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08dac-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08dac-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08dac-154">CommonParameters</span></span>
<span data-ttu-id="08dac-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08dac-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08dac-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08dac-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08dac-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08dac-157">INPUTS</span></span>

### <span data-ttu-id="08dac-158">System. String</span><span class="sxs-lookup"><span data-stu-id="08dac-158">System.String</span></span>

### <span data-ttu-id="08dac-159">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="08dac-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="08dac-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="08dac-160">System.String[]</span></span>

### <span data-ttu-id="08dac-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="08dac-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="08dac-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08dac-162">OUTPUTS</span></span>

### <span data-ttu-id="08dac-163">System. Object</span><span class="sxs-lookup"><span data-stu-id="08dac-163">System.Object</span></span>
## <span data-ttu-id="08dac-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="08dac-164">NOTES</span></span>

## <span data-ttu-id="08dac-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08dac-165">RELATED LINKS</span></span>
