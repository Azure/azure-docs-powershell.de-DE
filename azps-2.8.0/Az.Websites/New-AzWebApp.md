---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: 9d544d48a430aa671c0c18721e6dece6f1351424
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826972"
---
# <span data-ttu-id="bb21e-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb21e-101">New-AzWebApp</span></span>

## <span data-ttu-id="bb21e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb21e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb21e-103">Erstellt eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bb21e-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="bb21e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb21e-104">SYNTAX</span></span>

### <span data-ttu-id="bb21e-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb21e-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb21e-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="bb21e-106">PrivateRegistry</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>] [[-AppServicePlan] <String>]
 -ContainerImageName <String> -ContainerRegistryUrl <String> -ContainerRegistryUser <String>
 -ContainerRegistryPassword <SecureString> [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb21e-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb21e-107">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>] [-EnableContainerContinuousDeployment]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb21e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb21e-108">DESCRIPTION</span></span>
<span data-ttu-id="bb21e-109">Mit dem Cmdlet **New-AzWebApp** wird eine Azure Web App in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb21e-109">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="bb21e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb21e-110">EXAMPLES</span></span>

### <span data-ttu-id="bb21e-111">Beispiel 1: Erstellen einer Web-App</span><span class="sxs-lookup"><span data-stu-id="bb21e-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="bb21e-112">Mit diesem Befehl wird eine Azure Web App mit dem Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West US erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb21e-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="bb21e-113">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="bb21e-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="bb21e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb21e-114">PARAMETERS</span></span>

### <span data-ttu-id="bb21e-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bb21e-115">-AppServicePlan</span></span>
<span data-ttu-id="bb21e-116">Name des App-Service Plans oder App-Service Plan-ID. Wenn sich ein Webanwendungs-und App-Service Plan in verschiedenen Ressourcengruppen befindet, verwenden Sie die ID anstelle des Namens.</span><span class="sxs-lookup"><span data-stu-id="bb21e-116">App Service Plan Name or App Service Plan Id. If a WebApp and App Service Plan are in different Resource Groups, use the ID instead of the name.</span></span> <span data-ttu-id="bb21e-117">Die APP-Service Plan-ID kann mit folgendem abgerufen werden: $ASP = Get-AzAppServicePlan-ResourceGroup myRG-Name Web$ASP. ID gibt die ID des App-Service Plans zurück.</span><span class="sxs-lookup"><span data-stu-id="bb21e-117">The App Service Plan Id can be retrieved using: $asp = Get-AzAppServicePlan -ResourceGroup  myRG -Name MyWebapp $asp.id returns the App Service Plan Id.</span></span>


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

### <span data-ttu-id="bb21e-118">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="bb21e-118">-AppSettingsOverrides</span></span>
<span data-ttu-id="bb21e-119">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="bb21e-119">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="bb21e-120">-AseName</span><span class="sxs-lookup"><span data-stu-id="bb21e-120">-AseName</span></span>
<span data-ttu-id="bb21e-121">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="bb21e-121">App Service Environment Name</span></span>

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

### <span data-ttu-id="bb21e-122">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb21e-122">-AseResourceGroupName</span></span>
<span data-ttu-id="bb21e-123">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="bb21e-123">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="bb21e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb21e-124">-AsJob</span></span>
<span data-ttu-id="bb21e-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bb21e-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb21e-126">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="bb21e-126">-ContainerImageName</span></span>
<span data-ttu-id="bb21e-127">Name des Container Bilds und optionales Tag, beispielsweise (Bild: Tag)</span><span class="sxs-lookup"><span data-stu-id="bb21e-127">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="bb21e-128">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="bb21e-128">-ContainerRegistryPassword</span></span>
<span data-ttu-id="bb21e-129">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="bb21e-129">Private Container Registry Password</span></span>

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

### <span data-ttu-id="bb21e-130">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="bb21e-130">-ContainerRegistryUrl</span></span>
<span data-ttu-id="bb21e-131">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="bb21e-131">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="bb21e-132">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="bb21e-132">-ContainerRegistryUser</span></span>
<span data-ttu-id="bb21e-133">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="bb21e-133">Private Container Registry Username</span></span>

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

### <span data-ttu-id="bb21e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb21e-134">-DefaultProfile</span></span>
<span data-ttu-id="bb21e-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bb21e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb21e-136">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="bb21e-136">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="bb21e-137">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="bb21e-137">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="bb21e-138">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="bb21e-138">-GitRepositoryPath</span></span>
<span data-ttu-id="bb21e-139">Der Pfad zum GitHub-Repository, das die bereitzustellende Webanwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="bb21e-139">Path to the GitHub repository containing the web application to deploy.</span></span>

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

### <span data-ttu-id="bb21e-140">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="bb21e-140">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="bb21e-141">Option "benutzerdefinierte Hostnamen ignorieren"</span><span class="sxs-lookup"><span data-stu-id="bb21e-141">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="bb21e-142">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="bb21e-142">-IgnoreSourceControl</span></span>
<span data-ttu-id="bb21e-143">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="bb21e-143">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="bb21e-144">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="bb21e-144">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="bb21e-145">Option "Quell-Webspiel Steckplätze einbeziehen"</span><span class="sxs-lookup"><span data-stu-id="bb21e-145">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="bb21e-146">-Standort</span><span class="sxs-lookup"><span data-stu-id="bb21e-146">-Location</span></span>
<span data-ttu-id="bb21e-147">Lage</span><span class="sxs-lookup"><span data-stu-id="bb21e-147">Location</span></span>

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

### <span data-ttu-id="bb21e-148">-Name</span><span class="sxs-lookup"><span data-stu-id="bb21e-148">-Name</span></span>
<span data-ttu-id="bb21e-149">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="bb21e-149">WebApp Name</span></span>

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

### <span data-ttu-id="bb21e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb21e-150">-ResourceGroupName</span></span>
<span data-ttu-id="bb21e-151">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="bb21e-151">Resource Group Name</span></span>

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

### <span data-ttu-id="bb21e-152">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="bb21e-152">-SourceWebApp</span></span>
<span data-ttu-id="bb21e-153">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="bb21e-153">Source WebApp Object</span></span>

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

### <span data-ttu-id="bb21e-154">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bb21e-154">-TrafficManagerProfile</span></span>
<span data-ttu-id="bb21e-155">Ressourcen-ID des vorhandenen Traffic Manager-Profils</span><span class="sxs-lookup"><span data-stu-id="bb21e-155">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="bb21e-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bb21e-156">-Confirm</span></span>
<span data-ttu-id="bb21e-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb21e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb21e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb21e-158">-WhatIf</span></span>
<span data-ttu-id="bb21e-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb21e-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb21e-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb21e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb21e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb21e-161">CommonParameters</span></span>
<span data-ttu-id="bb21e-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb21e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb21e-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb21e-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb21e-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb21e-164">INPUTS</span></span>

### <span data-ttu-id="bb21e-165">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="bb21e-165">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bb21e-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb21e-166">OUTPUTS</span></span>

### <span data-ttu-id="bb21e-167">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="bb21e-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="bb21e-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb21e-168">NOTES</span></span>

## <span data-ttu-id="bb21e-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb21e-169">RELATED LINKS</span></span>

[<span data-ttu-id="bb21e-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb21e-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="bb21e-171">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb21e-171">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="bb21e-172">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb21e-172">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="bb21e-173">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb21e-173">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="bb21e-174">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb21e-174">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


