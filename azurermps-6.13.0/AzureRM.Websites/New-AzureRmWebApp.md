---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 2dfa72867655b95ea752c23c8605f19e7544e8e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475857"
---
# <span data-ttu-id="78327-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="78327-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="78327-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78327-102">SYNOPSIS</span></span>
<span data-ttu-id="78327-103">Erstellt eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="78327-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78327-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78327-104">SYNTAX</span></span>

### <span data-ttu-id="78327-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="78327-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-ContainerImageName <String>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-GitRepositoryPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78327-106">PrivateRegistry</span><span class="sxs-lookup"><span data-stu-id="78327-106">PrivateRegistry</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] -ContainerImageName <String> -ContainerRegistryUrl <String>
 -ContainerRegistryUser <String> -ContainerRegistryPassword <SecureString>
 [-EnableContainerContinuousDeployment] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78327-107">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="78327-107">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [[-TrafficManagerProfile] <String>]
 [-EnableContainerContinuousDeployment] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-IncludeSourceWebAppSlots] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78327-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78327-108">DESCRIPTION</span></span>
<span data-ttu-id="78327-109">Mit dem Cmdlet **New-AzureRmWebApp** wird eine Azure Web App in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="78327-109">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="78327-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78327-110">EXAMPLES</span></span>

### <span data-ttu-id="78327-111">Beispiel 1: Erstellen einer Web-App</span><span class="sxs-lookup"><span data-stu-id="78327-111">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="78327-112">Mit diesem Befehl wird eine Azure Web App mit dem Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West US erstellt.</span><span class="sxs-lookup"><span data-stu-id="78327-112">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="78327-113">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="78327-113">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="78327-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="78327-114">PARAMETERS</span></span>

### <span data-ttu-id="78327-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="78327-115">-AppServicePlan</span></span>
<span data-ttu-id="78327-116">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="78327-116">App Service Plan Name</span></span>

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

### <span data-ttu-id="78327-117">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="78327-117">-AppSettingsOverrides</span></span>
<span data-ttu-id="78327-118">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="78327-118">App Settings Overrides HashTable</span></span>

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

### <span data-ttu-id="78327-119">-AseName</span><span class="sxs-lookup"><span data-stu-id="78327-119">-AseName</span></span>
<span data-ttu-id="78327-120">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="78327-120">App Service Environment Name</span></span>

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

### <span data-ttu-id="78327-121">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78327-121">-AseResourceGroupName</span></span>
<span data-ttu-id="78327-122">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="78327-122">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="78327-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78327-123">-AsJob</span></span>
<span data-ttu-id="78327-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="78327-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78327-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="78327-125">-ContainerImageName</span></span>
<span data-ttu-id="78327-126">Name des Container Bilds und optionales Tag, beispielsweise (Bild: Tag)</span><span class="sxs-lookup"><span data-stu-id="78327-126">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="78327-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="78327-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="78327-128">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="78327-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="78327-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="78327-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="78327-130">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="78327-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="78327-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="78327-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="78327-132">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="78327-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="78327-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78327-133">-DefaultProfile</span></span>
<span data-ttu-id="78327-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78327-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78327-135">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="78327-135">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="78327-136">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="78327-136">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="78327-137">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="78327-137">-GitRepositoryPath</span></span>
<span data-ttu-id="78327-138">Der Pfad zum GitHub-Repository ölhaltiges die bereitzustellende Webanwendung.</span><span class="sxs-lookup"><span data-stu-id="78327-138">Path to the GitHub repository containign the web application to deploy.</span></span>

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

### <span data-ttu-id="78327-139">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="78327-139">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="78327-140">Option "benutzerdefinierte Hostnamen ignorieren"</span><span class="sxs-lookup"><span data-stu-id="78327-140">Ignore Custom Host Names Option</span></span>

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

### <span data-ttu-id="78327-141">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="78327-141">-IgnoreSourceControl</span></span>
<span data-ttu-id="78327-142">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="78327-142">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="78327-143">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="78327-143">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="78327-144">Option "Quell-Webspiel Steckplätze einbeziehen"</span><span class="sxs-lookup"><span data-stu-id="78327-144">Include Source WebApp Slots Option</span></span>

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

### <span data-ttu-id="78327-145">-Standort</span><span class="sxs-lookup"><span data-stu-id="78327-145">-Location</span></span>
<span data-ttu-id="78327-146">Lage</span><span class="sxs-lookup"><span data-stu-id="78327-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, PrivateRegistry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WebAppParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78327-147">-Name</span><span class="sxs-lookup"><span data-stu-id="78327-147">-Name</span></span>
<span data-ttu-id="78327-148">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="78327-148">WebApp Name</span></span>

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

### <span data-ttu-id="78327-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78327-149">-ResourceGroupName</span></span>
<span data-ttu-id="78327-150">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="78327-150">Resource Group Name</span></span>

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

### <span data-ttu-id="78327-151">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="78327-151">-SourceWebApp</span></span>
<span data-ttu-id="78327-152">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="78327-152">Source WebApp Object</span></span>

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

### <span data-ttu-id="78327-153">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78327-153">-TrafficManagerProfile</span></span>
<span data-ttu-id="78327-154">Ressourcen-ID des vorhandenen Traffic Manager-Profils</span><span class="sxs-lookup"><span data-stu-id="78327-154">Resource Id of existing traffic manager profile</span></span>

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

### <span data-ttu-id="78327-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78327-155">-Confirm</span></span>
<span data-ttu-id="78327-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78327-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78327-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78327-157">-WhatIf</span></span>
<span data-ttu-id="78327-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78327-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78327-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78327-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78327-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78327-160">CommonParameters</span></span>
<span data-ttu-id="78327-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78327-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78327-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78327-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78327-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78327-163">INPUTS</span></span>

### <span data-ttu-id="78327-164">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="78327-164">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="78327-165">Parameter: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="78327-165">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="78327-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78327-166">OUTPUTS</span></span>

### <span data-ttu-id="78327-167">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="78327-167">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="78327-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="78327-168">NOTES</span></span>

## <span data-ttu-id="78327-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78327-169">RELATED LINKS</span></span>

[<span data-ttu-id="78327-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="78327-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="78327-171">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="78327-171">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="78327-172">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="78327-172">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="78327-173">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="78327-173">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="78327-174">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="78327-174">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


