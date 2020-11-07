---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 795f1a7c4a002b7a8a141460b3b5e403ef8dc168
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820900"
---
# <span data-ttu-id="9b84d-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="9b84d-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="9b84d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b84d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b84d-103">Aktualisieren einer vorhandenen Blueprint-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="9b84d-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="9b84d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b84d-104">SYNTAX</span></span>

```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-SubscriptionId <String[]>]
 -Location <String> [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>] [-SystemAssignedIdentity]
 [-UserAssignedIdentity <String>] [-Lock <PSLockMode>] [-SecureStringParameter <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b84d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b84d-105">DESCRIPTION</span></span>
<span data-ttu-id="9b84d-106">Aktualisieren einer vorhandenen Blueprint-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="9b84d-106">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="9b84d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b84d-107">EXAMPLES</span></span>

### <span data-ttu-id="9b84d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9b84d-108">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="9b84d-109">Aktualisieren Sie eine vorhandene Blueprint-Zuordnung der Blueprint `$blueprintObject` -Definition innerhalb des angegebenen Abonnements, und aktualisieren Sie die Parameter.</span><span class="sxs-lookup"><span data-stu-id="9b84d-109">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="9b84d-110">Verwendet die vom System zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="9b84d-110">Uses system-assigned identity.</span></span> <span data-ttu-id="9b84d-111">Der Speicherort definiert den Bereich zum Erstellen der verwalteten Identität.</span><span class="sxs-lookup"><span data-stu-id="9b84d-111">The location defines the region for creating the managed identity.</span></span>

## <span data-ttu-id="9b84d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b84d-112">PARAMETERS</span></span>

### <span data-ttu-id="9b84d-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="9b84d-113">-Blueprint</span></span>
<span data-ttu-id="9b84d-114">Blueprint-Objekt</span><span class="sxs-lookup"><span data-stu-id="9b84d-114">Blueprint object.</span></span>

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

### <span data-ttu-id="9b84d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b84d-115">-DefaultProfile</span></span>
<span data-ttu-id="9b84d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b84d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b84d-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="9b84d-117">-Location</span></span>
<span data-ttu-id="9b84d-118">Der Bereich, in dem die verwaltete Identität erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b84d-118">Region for managed identity to be created in.</span></span>
<span data-ttu-id="9b84d-119">Weitere Informationen finden Sie unter aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="9b84d-119">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="9b84d-120">-Sperre</span><span class="sxs-lookup"><span data-stu-id="9b84d-120">-Lock</span></span>
<span data-ttu-id="9b84d-121">Sperren von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9b84d-121">Lock resources.</span></span>
<span data-ttu-id="9b84d-122">Weitere Informationen finden Sie unter aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="9b84d-122">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="9b84d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9b84d-123">-Name</span></span>
<span data-ttu-id="9b84d-124">Blueprint-Zuordnungsname</span><span class="sxs-lookup"><span data-stu-id="9b84d-124">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="9b84d-125">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9b84d-125">-Parameter</span></span>
<span data-ttu-id="9b84d-126">Artefakt-Parameter</span><span class="sxs-lookup"><span data-stu-id="9b84d-126">Artifact parameter.</span></span>

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

### <span data-ttu-id="9b84d-127">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="9b84d-127">-ResourceGroupParameter</span></span>
<span data-ttu-id="9b84d-128">{{Fill ResourceGroupParameter Description}}</span><span class="sxs-lookup"><span data-stu-id="9b84d-128">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="9b84d-129">-SecureString</span><span class="sxs-lookup"><span data-stu-id="9b84d-129">-SecureStringParameter</span></span>
<span data-ttu-id="9b84d-130">Sicherer Zeichenfolgenparameter für keyvault-Ressourcen-ID, Name und Version.</span><span class="sxs-lookup"><span data-stu-id="9b84d-130">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="9b84d-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9b84d-131">-SubscriptionId</span></span>
<span data-ttu-id="9b84d-132">Abonnement-Nr, um den Blueprint zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="9b84d-132">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="9b84d-133">Dies kann eine durch trennzeichengetrennte Liste von Abonnement-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="9b84d-133">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="9b84d-134">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9b84d-134">-SystemAssignedIdentity</span></span>
<span data-ttu-id="9b84d-135">System zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9b84d-135">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="9b84d-136">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9b84d-136">-UserAssignedIdentity</span></span>
<span data-ttu-id="9b84d-137">Benutzer zugewiesene Identität (MSI), um die Artefakte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9b84d-137">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="9b84d-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b84d-138">-Confirm</span></span>
<span data-ttu-id="9b84d-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b84d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b84d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b84d-140">-WhatIf</span></span>
<span data-ttu-id="9b84d-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b84d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b84d-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b84d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b84d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b84d-143">CommonParameters</span></span>
<span data-ttu-id="9b84d-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b84d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b84d-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b84d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b84d-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b84d-146">INPUTS</span></span>

### <span data-ttu-id="9b84d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9b84d-147">System.String</span></span>

### <span data-ttu-id="9b84d-148">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="9b84d-148">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="9b84d-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="9b84d-149">System.String[]</span></span>

### <span data-ttu-id="9b84d-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b84d-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b84d-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b84d-151">OUTPUTS</span></span>

### <span data-ttu-id="9b84d-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="9b84d-152">System.Object</span></span>
## <span data-ttu-id="9b84d-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b84d-153">NOTES</span></span>

## <span data-ttu-id="9b84d-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b84d-154">RELATED LINKS</span></span>
