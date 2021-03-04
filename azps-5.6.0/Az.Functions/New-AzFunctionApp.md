---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 97a1fa7aa5488034fa1f0147ae5a06ff639ecc06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927144"
---
# <span data-ttu-id="cf93d-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="cf93d-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="cf93d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf93d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf93d-103">Erstellt eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf93d-103">Creates a function app.</span></span>

## <span data-ttu-id="cf93d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf93d-104">SYNTAX</span></span>

### <span data-ttu-id="cf93d-105">Verbrauch (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf93d-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf93d-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cf93d-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf93d-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="cf93d-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf93d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf93d-108">DESCRIPTION</span></span>
<span data-ttu-id="cf93d-109">Erstellt eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf93d-109">Creates a function app.</span></span>

## <span data-ttu-id="cf93d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf93d-110">EXAMPLES</span></span>

### <span data-ttu-id="cf93d-111">Beispiel 1: Erstellen einer PowerShell-Funktions-App für den Verbrauch in Zentral-USA.</span><span class="sxs-lookup"><span data-stu-id="cf93d-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="cf93d-112">Mit diesem Befehl wird eine PowerShell-Funktions-App in Zentral-USA erstellt.</span><span class="sxs-lookup"><span data-stu-id="cf93d-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="cf93d-113">Beispiel 2: Erstellen Sie eine PowerShell-Funktions-App, die in einem Dienstplan gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="cf93d-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="cf93d-114">Mit diesem Befehl wird eine PowerShell-Funktions-App erstellt, die in einem Dienstplan gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="cf93d-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="cf93d-115">Beispiel 3: Erstellen einer Funktions-App mit einem mit einem privaten ACR-Bild.</span><span class="sxs-lookup"><span data-stu-id="cf93d-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="cf93d-116">Mit diesem Befehl wird eine Funktions-App mithilfe eines privaten ACR-Bilds erstellt.</span><span class="sxs-lookup"><span data-stu-id="cf93d-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="cf93d-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cf93d-117">PARAMETERS</span></span>

### <span data-ttu-id="cf93d-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="cf93d-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="cf93d-119">Instrumentierungsschlüssel der App Insights, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cf93d-119">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="cf93d-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="cf93d-121">Name des vorhandenen App Insights-Projekts, das der Funktions-App hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf93d-121">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="cf93d-122">-AppSetting</span></span>
<span data-ttu-id="cf93d-123">Funktions-App-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="cf93d-123">Function app settings.</span></span>

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

### <span data-ttu-id="cf93d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf93d-124">-AsJob</span></span>
<span data-ttu-id="cf93d-125">Führt das Cmdlet als Hintergrundauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="cf93d-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="cf93d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf93d-126">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cf93d-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="cf93d-128">Deaktivieren Sie das Erstellen einer Ressource für Anwendungseinblicke während der Erstellung der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf93d-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="cf93d-129">Es sind keine Protokolle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf93d-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="cf93d-130">-DockerImageName</span></span>
<span data-ttu-id="cf93d-131">Nur Linux.</span><span class="sxs-lookup"><span data-stu-id="cf93d-131">Linux only.</span></span>
<span data-ttu-id="cf93d-132">Containerbildname aus Docker Registry, z. B. publisher/image-name:tag.</span><span class="sxs-lookup"><span data-stu-id="cf93d-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="cf93d-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="cf93d-134">Benutzername und Kennwort der Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="cf93d-134">The container registry user name and password.</span></span>
<span data-ttu-id="cf93d-135">Erforderlich für private Registrierungsstellen.</span><span class="sxs-lookup"><span data-stu-id="cf93d-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="cf93d-136">-FunctionsVersion</span></span>
<span data-ttu-id="cf93d-137">Die Version "Funktionen".</span><span class="sxs-lookup"><span data-stu-id="cf93d-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="cf93d-138">-IdentityID</span></span>
<span data-ttu-id="cf93d-139">Gibt die Liste der Benutzeridentitäten an, die der Funktions-App zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cf93d-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="cf93d-140">Die Benutzeridentitätsverweise werden ARM Ressourcen-ID im Formular "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf93d-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cf93d-141">-IdentityType</span></span>
<span data-ttu-id="cf93d-142">Gibt den Identitätstyp an, der für die Funktions-App verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf93d-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="cf93d-143">Die zulässigen Werte für diesen Parameter sind: - SystemAssigned - UserAssigned</span><span class="sxs-lookup"><span data-stu-id="cf93d-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-144">-Location</span><span class="sxs-lookup"><span data-stu-id="cf93d-144">-Location</span></span>
<span data-ttu-id="cf93d-145">Der Speicherort für den Verbrauchsplan.</span><span class="sxs-lookup"><span data-stu-id="cf93d-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-146">-Name</span><span class="sxs-lookup"><span data-stu-id="cf93d-146">-Name</span></span>
<span data-ttu-id="cf93d-147">Der Name der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf93d-147">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cf93d-148">-NoWait</span></span>
<span data-ttu-id="cf93d-149">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cf93d-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="cf93d-150">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cf93d-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cf93d-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="cf93d-151">-OSType</span></span>
<span data-ttu-id="cf93d-152">Das Betriebssystem zum Hosten der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf93d-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf93d-153">-PassThru</span></span>
<span data-ttu-id="cf93d-154">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf93d-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="cf93d-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="cf93d-155">-PlanName</span></span>
<span data-ttu-id="cf93d-156">Der Name des Dienstplans.</span><span class="sxs-lookup"><span data-stu-id="cf93d-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf93d-157">-ResourceGroupName</span></span>
<span data-ttu-id="cf93d-158">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf93d-158">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="cf93d-159">-Runtime</span></span>
<span data-ttu-id="cf93d-160">Die Funktionslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cf93d-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="cf93d-161">-RuntimeVersion</span></span>
<span data-ttu-id="cf93d-162">Die Funktionslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cf93d-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cf93d-163">-StorageAccountName</span></span>
<span data-ttu-id="cf93d-164">Der Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="cf93d-164">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf93d-165">-SubscriptionId</span></span>
<span data-ttu-id="cf93d-166">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="cf93d-166">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf93d-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="cf93d-167">-Tag</span></span>
<span data-ttu-id="cf93d-168">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="cf93d-168">Resource tags.</span></span>

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

### <span data-ttu-id="cf93d-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf93d-169">-Confirm</span></span>
<span data-ttu-id="cf93d-170">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf93d-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf93d-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf93d-171">-WhatIf</span></span>
<span data-ttu-id="cf93d-172">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf93d-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf93d-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf93d-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf93d-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf93d-174">CommonParameters</span></span>
<span data-ttu-id="cf93d-175">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf93d-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf93d-176">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf93d-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf93d-177">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf93d-177">INPUTS</span></span>

## <span data-ttu-id="cf93d-178">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf93d-178">OUTPUTS</span></span>

### <span data-ttu-id="cf93d-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="cf93d-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="cf93d-180">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cf93d-180">NOTES</span></span>

<span data-ttu-id="cf93d-181">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cf93d-181">ALIASES</span></span>

## <span data-ttu-id="cf93d-182">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cf93d-182">RELATED LINKS</span></span>

