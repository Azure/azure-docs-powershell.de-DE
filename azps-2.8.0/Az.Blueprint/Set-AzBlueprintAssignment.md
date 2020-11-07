---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: df1d25f2d5362a81bd33b74bad223bbfb952daa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652330"
---
# <span data-ttu-id="8daca-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="8daca-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="8daca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8daca-102">SYNOPSIS</span></span>
<span data-ttu-id="8daca-103">Aktualisieren einer vorhandenen Blueprint-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="8daca-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="8daca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8daca-104">SYNTAX</span></span>

### <span data-ttu-id="8daca-105">UpdateBlueprintAssignment (Standard)</span><span class="sxs-lookup"><span data-stu-id="8daca-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8daca-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="8daca-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8daca-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8daca-107">DESCRIPTION</span></span>
<span data-ttu-id="8daca-108">Aktualisieren einer vorhandenen Blueprint-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="8daca-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="8daca-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8daca-109">EXAMPLES</span></span>

### <span data-ttu-id="8daca-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8daca-110">Example 1</span></span>
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

<span data-ttu-id="8daca-111">Aktualisieren Sie eine vorhandene Blueprint-Zuordnung der Blueprint `$blueprintObject` -Definition innerhalb des angegebenen Abonnements, und aktualisieren Sie die Parameter.</span><span class="sxs-lookup"><span data-stu-id="8daca-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="8daca-112">Verwendet die vom System zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="8daca-112">Uses system-assigned identity.</span></span> <span data-ttu-id="8daca-113">Der Speicherort definiert den Bereich zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="8daca-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="8daca-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8daca-114">Example 2</span></span>
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

<span data-ttu-id="8daca-115">Aktualisieren einer vorhandenen Blueprint-Zuordnung über eine Zuordnungsdatei</span><span class="sxs-lookup"><span data-stu-id="8daca-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="8daca-116">Das Format der Zuordnungsdatei finden Sie in den Beispielen für Anforderung/Antwort unter: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="8daca-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="8daca-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8daca-117">PARAMETERS</span></span>

### <span data-ttu-id="8daca-118">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="8daca-118">-Blueprint</span></span>
<span data-ttu-id="8daca-119">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="8daca-119">Blueprint object.</span></span>

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

### <span data-ttu-id="8daca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8daca-120">-DefaultProfile</span></span>
<span data-ttu-id="8daca-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8daca-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8daca-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="8daca-122">-Location</span></span>
<span data-ttu-id="8daca-123">Der Bereich, in dem die verwaltete Identität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8daca-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="8daca-124">Weitere Informationen finden Sie unter aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="8daca-124">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="8daca-125">-Sperre</span><span class="sxs-lookup"><span data-stu-id="8daca-125">-Lock</span></span>
<span data-ttu-id="8daca-126">Sperren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8daca-126">Lock resources.</span></span>
<span data-ttu-id="8daca-127">Weitere Informationen finden Sie unter aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="8daca-127">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="8daca-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8daca-128">-Name</span></span>
<span data-ttu-id="8daca-129">Blueprint-Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="8daca-129">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="8daca-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8daca-130">-Parameter</span></span>
<span data-ttu-id="8daca-131">Artefakt-Parameter</span><span class="sxs-lookup"><span data-stu-id="8daca-131">Artifact parameter.</span></span>

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

### <span data-ttu-id="8daca-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="8daca-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="8daca-133">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="8daca-133">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="8daca-134">-SecureString</span><span class="sxs-lookup"><span data-stu-id="8daca-134">-SecureStringParameter</span></span>
<span data-ttu-id="8daca-135">Sicherer Zeichenfolgenparameter für keyvault-Ressourcen-ID, Name und Version.</span><span class="sxs-lookup"><span data-stu-id="8daca-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="8daca-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8daca-136">-SubscriptionId</span></span>
<span data-ttu-id="8daca-137">Abonnement-Nr, um den Blueprint zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8daca-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="8daca-138">Dies kann eine durch trennzeichengetrennte Liste von Abonnement-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="8daca-138">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="8daca-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8daca-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="8daca-140">System zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8daca-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="8daca-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8daca-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="8daca-142">Benutzer zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8daca-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="8daca-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8daca-143">-Confirm</span></span>
<span data-ttu-id="8daca-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8daca-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8daca-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8daca-145">-WhatIf</span></span>
<span data-ttu-id="8daca-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8daca-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8daca-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8daca-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8daca-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8daca-148">CommonParameters</span></span>
<span data-ttu-id="8daca-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8daca-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8daca-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8daca-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8daca-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8daca-151">INPUTS</span></span>

### <span data-ttu-id="8daca-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8daca-152">System.String</span></span>

### <span data-ttu-id="8daca-153">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="8daca-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="8daca-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="8daca-154">System.String[]</span></span>

### <span data-ttu-id="8daca-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8daca-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8daca-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8daca-156">OUTPUTS</span></span>

### <span data-ttu-id="8daca-157">System. Object</span><span class="sxs-lookup"><span data-stu-id="8daca-157">System.Object</span></span>
## <span data-ttu-id="8daca-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="8daca-158">NOTES</span></span>

## <span data-ttu-id="8daca-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8daca-159">RELATED LINKS</span></span>
