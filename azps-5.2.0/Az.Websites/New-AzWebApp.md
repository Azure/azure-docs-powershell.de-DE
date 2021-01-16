---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 760aacba880276059c4a468454cccec29d397183
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290158"
---
# <span data-ttu-id="ccb6f-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccb6f-101">New-AzWebApp</span></span>

## <span data-ttu-id="ccb6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccb6f-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb6f-103">Erstellt eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="ccb6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccb6f-104">SYNTAX</span></span>

### <span data-ttu-id="ccb6f-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ccb6f-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccb6f-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="ccb6f-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccb6f-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccb6f-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb6f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccb6f-108">DESCRIPTION</span></span>
<span data-ttu-id="ccb6f-109">Das **Cmdlet "New-AzWebApp"** erstellt eine Azure Web App in einer bestimmten Ressourcengruppe, die den angegebenen App Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="ccb6f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ccb6f-110">EXAMPLES</span></span>

### <span data-ttu-id="ccb6f-111">Beispiel 1: Erstellen einer Web App</span><span class="sxs-lookup"><span data-stu-id="ccb6f-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="ccb6f-112">Mit diesem Befehl wird eine Azure Web App mit dem Namen "ContosoSite" in der vorhandenen Ressourcengruppe "Default-Web-WestUS" im Rechenzentrum "USA, Westen" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="ccb6f-113">Der Befehl verwendet einen vorhandenen App-Dienstplan namens ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="ccb6f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccb6f-114">PARAMETERS</span></span>

### <span data-ttu-id="ccb6f-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccb6f-115">-AppServicePlan</span></span>
<span data-ttu-id="ccb6f-116">Name des App-Serviceplans oder Id des App-Serviceplans. Wenn sich ein WebApp- und ein App-Dienstplan in verschiedenen Ressourcengruppen befinden, verwenden Sie die ID anstelle des Namens.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="ccb6f-117">Die Plan-ID des App-Diensts kann mit: $asp = Get-AzAppServicePlan -ResourceGroup myRG -Name MyWebapp $asp.id wird die Id des App-Serviceplans zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="ccb6f-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="ccb6f-119">#A0 setzt HashTable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="ccb6f-119">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="ccb6f-120">-AseName</span></span>
<span data-ttu-id="ccb6f-121">Name der App-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="ccb6f-121">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccb6f-122">-AseResourceGroupName</span></span>
<span data-ttu-id="ccb6f-123">Ressourcengruppenname der App-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="ccb6f-123">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccb6f-124">-AsJob</span></span>
<span data-ttu-id="ccb6f-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ccb6f-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccb6f-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="ccb6f-126">-ContainerImageName</span></span>
<span data-ttu-id="ccb6f-127">Container Image Name and optional tag, for example (image:tag)</span><span class="sxs-lookup"><span data-stu-id="ccb6f-127">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="ccb6f-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="ccb6f-129">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="ccb6f-129">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="ccb6f-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="ccb6f-131">URL des Registrierungsservers für privaten Container</span><span class="sxs-lookup"><span data-stu-id="ccb6f-131">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="ccb6f-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="ccb6f-133">Private Container Registry Username</span><span class="sxs-lookup"><span data-stu-id="ccb6f-133">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb6f-134">-DefaultProfile</span></span>
<span data-ttu-id="ccb6f-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccb6f-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="ccb6f-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="ccb6f-137">Aktiviert/Deaktiviert den Container-Webhook für die fortlaufende Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ccb6f-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="ccb6f-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="ccb6f-138">-GitRepositoryPath</span></span>
<span data-ttu-id="ccb6f-139">Pfad zum GitHub-Repository, das die webanwendung enthält, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-139">Path to the GitHub repository containing the web application to deploy.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="ccb6f-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="ccb6f-141">Option "Benutzerdefinierte Hostnamen ignorieren"</span><span class="sxs-lookup"><span data-stu-id="ccb6f-141">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="ccb6f-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="ccb6f-143">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="ccb6f-143">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ccb6f-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="ccb6f-145">Include Source WebApp Slots Option</span><span class="sxs-lookup"><span data-stu-id="ccb6f-145">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-146">-Location</span><span class="sxs-lookup"><span data-stu-id="ccb6f-146">-Location</span></span>
<span data-ttu-id="ccb6f-147">Position</span><span class="sxs-lookup"><span data-stu-id="ccb6f-147">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-148">-Name</span><span class="sxs-lookup"><span data-stu-id="ccb6f-148">-Name</span></span>
<span data-ttu-id="ccb6f-149">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="ccb6f-149">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccb6f-150">-ResourceGroupName</span></span>
<span data-ttu-id="ccb6f-151">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ccb6f-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PrivateRegistry, WebAppParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="ccb6f-152">-SourceWebApp</span></span>
<span data-ttu-id="ccb6f-153">Quell-WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="ccb6f-153">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: WebAppParameterSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ccb6f-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="ccb6f-155">Ressourcen-ID des vorhandenen Datenverkehrs-Manager-Profils</span><span class="sxs-lookup"><span data-stu-id="ccb6f-155">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb6f-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccb6f-156">-Confirm</span></span>
<span data-ttu-id="ccb6f-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccb6f-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ccb6f-158">-WhatIf</span></span>
<span data-ttu-id="ccb6f-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccb6f-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccb6f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb6f-161">CommonParameters</span></span>
<span data-ttu-id="ccb6f-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccb6f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb6f-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccb6f-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb6f-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ccb6f-164">INPUTS</span></span>

### <span data-ttu-id="ccb6f-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ccb6f-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ccb6f-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ccb6f-166">OUTPUTS</span></span>

### <span data-ttu-id="ccb6f-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ccb6f-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ccb6f-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ccb6f-168">NOTES</span></span>

## <span data-ttu-id="ccb6f-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ccb6f-169">RELATED LINKS</span></span>

[<span data-ttu-id="ccb6f-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccb6f-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ccb6f-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccb6f-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ccb6f-172">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccb6f-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ccb6f-173">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccb6f-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ccb6f-174">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ccb6f-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


