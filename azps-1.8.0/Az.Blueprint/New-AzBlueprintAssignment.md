---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 43689de5ae2431db8bc523369700f32dba0206bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820896"
---
# <span data-ttu-id="e99f6-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e99f6-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e99f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e99f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e99f6-103">Zuweisen einer Blueprint-Definition zu einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e99f6-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="e99f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e99f6-104">SYNTAX</span></span>

```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e99f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e99f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e99f6-106">Zuweisen einer Blueprint-Definition zu einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e99f6-106">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="e99f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e99f6-107">EXAMPLES</span></span>

### <span data-ttu-id="e99f6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e99f6-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameters $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="e99f6-109">Erstellen Sie eine neue Blueprint-Zuweisung der Blueprint-Definition `$blueprintObject` innerhalb des angegebenen Abonnements unter Verwendung des definierten Parameters und des Ressourcengruppen Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="e99f6-109">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="e99f6-110">Verwendet die vom System zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="e99f6-110">Uses system-assigned identity.</span></span> <span data-ttu-id="e99f6-111">Der Speicherort definiert den Bereich zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="e99f6-111">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="e99f6-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e99f6-112">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="e99f6-113">Erstellen Sie eine neue Blueprint-Zuweisung der Blueprint-Definition `$blueprintObject` innerhalb des angegebenen Abonnements mithilfe des definierten Parameters und des Ressourcengruppen Wörterbuchs, und konfigurieren Sie die Ressourcen Sperrung für **allresources**.</span><span class="sxs-lookup"><span data-stu-id="e99f6-113">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="e99f6-114">Standardmäßig wird die vom System zugewiesene Identität verwendet.</span><span class="sxs-lookup"><span data-stu-id="e99f6-114">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="e99f6-115">Der Speicherort definiert den Bereich zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="e99f6-115">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="e99f6-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e99f6-116">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="e99f6-117">Erstellen Sie eine neue Blueprint-Zuweisung der Blueprint-Definition `$blueprintObject` innerhalb des angegebenen Abonnements unter Verwendung des definierten Parameters und des Ressourcengruppen Wörterbuchs unter Verwendung der angegebenen vom Benutzer zugewiesenen Identitäts-ID.</span><span class="sxs-lookup"><span data-stu-id="e99f6-117">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

## <span data-ttu-id="e99f6-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e99f6-118">PARAMETERS</span></span>

### <span data-ttu-id="e99f6-119">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="e99f6-119">-Blueprint</span></span>
<span data-ttu-id="e99f6-120">Blueprint-Definitionsobjekt</span><span class="sxs-lookup"><span data-stu-id="e99f6-120">Blueprint definition object.</span></span>

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

### <span data-ttu-id="e99f6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99f6-121">-DefaultProfile</span></span>
<span data-ttu-id="e99f6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e99f6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e99f6-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="e99f6-123">-Location</span></span>
<span data-ttu-id="e99f6-124">Der Bereich, in dem die verwaltete Identität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e99f6-124">Region for managed identity to be created in.</span></span>
<span data-ttu-id="e99f6-125">Weitere Informationen finden Sie unter aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="e99f6-125">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="e99f6-126">-Sperre</span><span class="sxs-lookup"><span data-stu-id="e99f6-126">-Lock</span></span>
<span data-ttu-id="e99f6-127">Sperren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e99f6-127">Lock resources.</span></span>
<span data-ttu-id="e99f6-128">Weitere Informationen finden Sie unter aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="e99f6-128">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="e99f6-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e99f6-129">-Name</span></span>
<span data-ttu-id="e99f6-130">Blueprint-Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="e99f6-130">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="e99f6-131">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e99f6-131">-Parameter</span></span>
<span data-ttu-id="e99f6-132">Artefaktparameter.</span><span class="sxs-lookup"><span data-stu-id="e99f6-132">Artifact parameters.</span></span>

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

### <span data-ttu-id="e99f6-133">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e99f6-133">-ResourceGroupParameter</span></span>
<span data-ttu-id="e99f6-134">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="e99f6-134">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="e99f6-135">-SecureString</span><span class="sxs-lookup"><span data-stu-id="e99f6-135">-SecureStringParameter</span></span>
<span data-ttu-id="e99f6-136">Sicherer Zeichenfolgenparameter für keyvault-Ressourcen-ID, Name und Version.</span><span class="sxs-lookup"><span data-stu-id="e99f6-136">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="e99f6-137">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e99f6-137">-SubscriptionId</span></span>
<span data-ttu-id="e99f6-138">Abonnement-ID, um die Blueprint-Definition zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="e99f6-138">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="e99f6-139">Dies kann eine durch trennzeichengetrennte Liste von Abonnement-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="e99f6-139">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="e99f6-140">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e99f6-140">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e99f6-141">System zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e99f6-141">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e99f6-142">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e99f6-142">-UserAssignedIdentity</span></span>
<span data-ttu-id="e99f6-143">Benutzer zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e99f6-143">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="e99f6-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e99f6-144">-Confirm</span></span>
<span data-ttu-id="e99f6-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e99f6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e99f6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e99f6-146">-WhatIf</span></span>
<span data-ttu-id="e99f6-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e99f6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e99f6-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e99f6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e99f6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99f6-149">CommonParameters</span></span>
<span data-ttu-id="e99f6-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99f6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99f6-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e99f6-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99f6-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e99f6-152">INPUTS</span></span>

### <span data-ttu-id="e99f6-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e99f6-153">System.String</span></span>

### <span data-ttu-id="e99f6-154">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="e99f6-154">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e99f6-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="e99f6-155">System.String[]</span></span>

### <span data-ttu-id="e99f6-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e99f6-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e99f6-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e99f6-157">OUTPUTS</span></span>

### <span data-ttu-id="e99f6-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="e99f6-158">System.Object</span></span>
## <span data-ttu-id="e99f6-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="e99f6-159">NOTES</span></span>

## <span data-ttu-id="e99f6-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e99f6-160">RELATED LINKS</span></span>
