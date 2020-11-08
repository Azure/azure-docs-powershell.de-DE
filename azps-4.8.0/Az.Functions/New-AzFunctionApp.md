---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166928"
---
# <span data-ttu-id="ccc04-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="ccc04-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="ccc04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccc04-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc04-103">Erstellt eine Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="ccc04-103">Creates a function app.</span></span>

## <span data-ttu-id="ccc04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccc04-104">SYNTAX</span></span>

### <span data-ttu-id="ccc04-105">Verbrauch (Standard)</span><span class="sxs-lookup"><span data-stu-id="ccc04-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ccc04-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccc04-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ccc04-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="ccc04-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ccc04-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccc04-108">DESCRIPTION</span></span>
<span data-ttu-id="ccc04-109">Erstellt eine Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="ccc04-109">Creates a function app.</span></span>

## <span data-ttu-id="ccc04-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccc04-110">EXAMPLES</span></span>

### <span data-ttu-id="ccc04-111">Beispiel 1: Erstellen einer Energieverbrauchs-PowerShell-Funktions-APP in Central US.</span><span class="sxs-lookup"><span data-stu-id="ccc04-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="ccc04-112">Mit diesem Befehl wird eine APP für die Verbrauchs-PowerShell-Funktion in Central US erstellt.</span><span class="sxs-lookup"><span data-stu-id="ccc04-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="ccc04-113">Beispiel 2: Erstellen einer PowerShell-Funktions-APP, die in einem Service Plan gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="ccc04-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="ccc04-114">Mit diesem Befehl wird eine PowerShell-Funktions-APP erstellt, die in einem Service Plan gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="ccc04-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="ccc04-115">Beispiel 3: Erstellen einer Funktions-APP unter Verwendung eines privaten ACR-Bilds</span><span class="sxs-lookup"><span data-stu-id="ccc04-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="ccc04-116">Mit diesem Befehl wird eine Funktions-APP mit einem privaten ACR-Bild erstellt.</span><span class="sxs-lookup"><span data-stu-id="ccc04-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="ccc04-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccc04-117">PARAMETERS</span></span>

### <span data-ttu-id="ccc04-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="ccc04-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="ccc04-119">Instrumentations Schlüssel für App-Einblicke, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ccc04-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="ccc04-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="ccc04-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="ccc04-121">Der Name des vorhandenen APP Insights-Projekts, das der Funktions-APP hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ccc04-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="ccc04-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="ccc04-122">-AppSetting</span></span>
<span data-ttu-id="ccc04-123">Funktions-APP-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="ccc04-123">Function app settings.</span></span>

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

### <span data-ttu-id="ccc04-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccc04-124">-AsJob</span></span>
<span data-ttu-id="ccc04-125">Führt das Cmdlet als Hintergrund Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="ccc04-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="ccc04-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc04-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="ccc04-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ccc04-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="ccc04-128">Deaktivieren Sie das Erstellen von Anwendungs Einblicken während der Erstellung der Funktion app.</span><span class="sxs-lookup"><span data-stu-id="ccc04-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="ccc04-129">Es stehen keine Protokolle zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ccc04-129">No logs will be available.</span></span>

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

### <span data-ttu-id="ccc04-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="ccc04-130">-DockerImageName</span></span>
<span data-ttu-id="ccc04-131">Nur für Linux.</span><span class="sxs-lookup"><span data-stu-id="ccc04-131">Linux only.</span></span>
<span data-ttu-id="ccc04-132">Name des Container Bilds aus der Docker-Registrierung, z.b. Publisher/Image-Name: Tag.</span><span class="sxs-lookup"><span data-stu-id="ccc04-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

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

### <span data-ttu-id="ccc04-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ccc04-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="ccc04-134">Der Container Registrierungs Benutzername und das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="ccc04-134">The container registry user name and password.</span></span>
<span data-ttu-id="ccc04-135">Für private Registrierungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ccc04-135">Required for private registries.</span></span>

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

### <span data-ttu-id="ccc04-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="ccc04-136">-FunctionsVersion</span></span>
<span data-ttu-id="ccc04-137">Die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="ccc04-137">The Functions version.</span></span>

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

### <span data-ttu-id="ccc04-138">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="ccc04-138">-IdentityID</span></span>
<span data-ttu-id="ccc04-139">Gibt die Liste der Benutzeridentitäten an, die der Funktions-APP zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ccc04-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="ccc04-140">Die Benutzer Identitäts Bezüge sind arm-Ressourcen-IDs in der Form: '/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/Identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="ccc04-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ccc04-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ccc04-141">-IdentityType</span></span>
<span data-ttu-id="ccc04-142">Gibt den Typ der Identität an, die für die Funktions-APP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ccc04-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="ccc04-143">Die zulässigen Werte für diesen Parameter sind:-SystemAssigned-UserAssigned</span><span class="sxs-lookup"><span data-stu-id="ccc04-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="ccc04-144">-Standort</span><span class="sxs-lookup"><span data-stu-id="ccc04-144">-Location</span></span>
<span data-ttu-id="ccc04-145">Der Speicherort für den Verbrauchs Plan.</span><span class="sxs-lookup"><span data-stu-id="ccc04-145">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="ccc04-146">-Name</span><span class="sxs-lookup"><span data-stu-id="ccc04-146">-Name</span></span>
<span data-ttu-id="ccc04-147">Der Name der Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="ccc04-147">The name of the function app.</span></span>

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

### <span data-ttu-id="ccc04-148">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ccc04-148">-NoWait</span></span>
<span data-ttu-id="ccc04-149">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="ccc04-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="ccc04-150">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ccc04-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ccc04-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="ccc04-151">-OSType</span></span>
<span data-ttu-id="ccc04-152">Das Betriebssystem zum Hosten der Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="ccc04-152">The OS to host the function app.</span></span>

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

### <span data-ttu-id="ccc04-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccc04-153">-PassThru</span></span>
<span data-ttu-id="ccc04-154">Gibt "true" zurück, wenn der Befehl erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="ccc04-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="ccc04-155">-Planname</span><span class="sxs-lookup"><span data-stu-id="ccc04-155">-PlanName</span></span>
<span data-ttu-id="ccc04-156">Der Name des Service Plans.</span><span class="sxs-lookup"><span data-stu-id="ccc04-156">The name of the service plan.</span></span>

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

### <span data-ttu-id="ccc04-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccc04-157">-ResourceGroupName</span></span>
<span data-ttu-id="ccc04-158">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ccc04-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="ccc04-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="ccc04-159">-Runtime</span></span>
<span data-ttu-id="ccc04-160">Die Funktions Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="ccc04-160">The function runtime.</span></span>

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

### <span data-ttu-id="ccc04-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="ccc04-161">-RuntimeVersion</span></span>
<span data-ttu-id="ccc04-162">Die Funktions Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="ccc04-162">The function runtime.</span></span>

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

### <span data-ttu-id="ccc04-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ccc04-163">-StorageAccountName</span></span>
<span data-ttu-id="ccc04-164">Der Name des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="ccc04-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="ccc04-165">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ccc04-165">-SubscriptionId</span></span>
<span data-ttu-id="ccc04-166">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ccc04-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="ccc04-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="ccc04-167">-Tag</span></span>
<span data-ttu-id="ccc04-168">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="ccc04-168">Resource tags.</span></span>

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

### <span data-ttu-id="ccc04-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ccc04-169">-Confirm</span></span>
<span data-ttu-id="ccc04-170">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccc04-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccc04-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccc04-171">-WhatIf</span></span>
<span data-ttu-id="ccc04-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccc04-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccc04-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccc04-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccc04-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc04-174">CommonParameters</span></span>
<span data-ttu-id="ccc04-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccc04-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc04-176">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccc04-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc04-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccc04-177">INPUTS</span></span>

## <span data-ttu-id="ccc04-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccc04-178">OUTPUTS</span></span>

### <span data-ttu-id="ccc04-179">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="ccc04-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="ccc04-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccc04-180">NOTES</span></span>

<span data-ttu-id="ccc04-181">Aliase</span><span class="sxs-lookup"><span data-stu-id="ccc04-181">ALIASES</span></span>

## <span data-ttu-id="ccc04-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccc04-182">RELATED LINKS</span></span>

