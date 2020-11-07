---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebApp.md
ms.openlocfilehash: ec5f9cf60025e6b35248b2e7f8058040b404ec42
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842755"
---
# <span data-ttu-id="515ff-101">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="515ff-101">New-AzWebApp</span></span>

## <span data-ttu-id="515ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="515ff-102">SYNOPSIS</span></span>
<span data-ttu-id="515ff-103">Erstellt eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="515ff-103">Creates an Azure Web App.</span></span>

## <span data-ttu-id="515ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="515ff-104">SYNTAX</span></span>

### <span data-ttu-id="515ff-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="515ff-105">SimpleParameterSet (Default)</span></span>
```
New-AzWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="515ff-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="515ff-106">WebAppParameterSet</span></span>
```
New-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="515ff-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="515ff-107">DESCRIPTION</span></span>
<span data-ttu-id="515ff-108">Mit dem Cmdlet **New-AzWebApp** wird eine Azure Web App in einer bestimmten Ressourcengruppe erstellt, die den angegebenen app-Service Plan und das Rechenzentrum verwendet.</span><span class="sxs-lookup"><span data-stu-id="515ff-108">The **New-AzWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="515ff-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="515ff-109">EXAMPLES</span></span>

### <span data-ttu-id="515ff-110">Beispiel 1: Erstellen einer Web-App</span><span class="sxs-lookup"><span data-stu-id="515ff-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="515ff-111">Mit diesem Befehl wird eine Azure Web App mit dem Namen ContosoSite in der vorhandenen Ressourcengruppe Default-Web-westus in Rechenzentrum West US erstellt.</span><span class="sxs-lookup"><span data-stu-id="515ff-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="515ff-112">Der Befehl verwendet einen vorhandenen APP-Service Plan mit dem Namen ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="515ff-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="515ff-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="515ff-113">PARAMETERS</span></span>

### <span data-ttu-id="515ff-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="515ff-114">-AppServicePlan</span></span>
<span data-ttu-id="515ff-115">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="515ff-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="515ff-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="515ff-117">App-Einstellungen setzen Hashtable außer Kraft</span><span class="sxs-lookup"><span data-stu-id="515ff-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="515ff-118">-AseName</span></span>
<span data-ttu-id="515ff-119">Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="515ff-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="515ff-120">-AseResourceGroupName</span></span>
<span data-ttu-id="515ff-121">Ressourcengruppen Name der APP-Dienstumgebung</span><span class="sxs-lookup"><span data-stu-id="515ff-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="515ff-122">-AsJob</span></span>
<span data-ttu-id="515ff-123">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="515ff-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515ff-124">-DefaultProfile</span></span>
<span data-ttu-id="515ff-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="515ff-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="515ff-126">-GitRepositoryPath</span></span>
<span data-ttu-id="515ff-127">Der Pfad zum GitHub-Repository ölhaltiges die bereitzustellende Webanwendung.</span><span class="sxs-lookup"><span data-stu-id="515ff-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="515ff-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="515ff-129">Option "benutzerdefinierte Hostnamen ignorieren"</span><span class="sxs-lookup"><span data-stu-id="515ff-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="515ff-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="515ff-131">Option "Quellcodeverwaltung ignorieren"</span><span class="sxs-lookup"><span data-stu-id="515ff-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="515ff-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="515ff-133">Option "Quell-Webspiel Steckplätze einbeziehen"</span><span class="sxs-lookup"><span data-stu-id="515ff-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="515ff-134">-Location</span></span>
<span data-ttu-id="515ff-135">Lage</span><span class="sxs-lookup"><span data-stu-id="515ff-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-136">-Name</span><span class="sxs-lookup"><span data-stu-id="515ff-136">-Name</span></span>
<span data-ttu-id="515ff-137">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="515ff-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="515ff-138">-ResourceGroupName</span></span>
<span data-ttu-id="515ff-139">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="515ff-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="515ff-140">-SourceWebApp</span></span>
<span data-ttu-id="515ff-141">Quell-Webobjekt</span><span class="sxs-lookup"><span data-stu-id="515ff-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="515ff-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="515ff-143">Ressourcen-ID des vorhandenen Traffic Manager-Profils</span><span class="sxs-lookup"><span data-stu-id="515ff-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="515ff-144">-Confirm</span></span>
<span data-ttu-id="515ff-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="515ff-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="515ff-146">-WhatIf</span></span>
<span data-ttu-id="515ff-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="515ff-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="515ff-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="515ff-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="515ff-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515ff-149">CommonParameters</span></span>
<span data-ttu-id="515ff-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="515ff-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515ff-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="515ff-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515ff-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="515ff-152">INPUTS</span></span>

### <span data-ttu-id="515ff-153">Website</span><span class="sxs-lookup"><span data-stu-id="515ff-153">Site</span></span>
<span data-ttu-id="515ff-154">Der Parameter "SourceWebApp" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="515ff-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="515ff-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="515ff-155">OUTPUTS</span></span>

### <span data-ttu-id="515ff-156">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="515ff-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="515ff-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="515ff-157">NOTES</span></span>

## <span data-ttu-id="515ff-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="515ff-158">RELATED LINKS</span></span>

[<span data-ttu-id="515ff-159">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="515ff-159">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="515ff-160">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="515ff-160">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="515ff-161">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="515ff-161">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="515ff-162">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="515ff-162">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="515ff-163">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="515ff-163">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


