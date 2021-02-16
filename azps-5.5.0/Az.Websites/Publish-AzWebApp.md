---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173388"
---
# <span data-ttu-id="03748-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="03748-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="03748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03748-102">SYNOPSIS</span></span>
<span data-ttu-id="03748-103">Stellt mithilfe der Zipploy eine Azure Web App aus einer ZIP-, JAR- oder WAR-Datei bereit.</span><span class="sxs-lookup"><span data-stu-id="03748-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="03748-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03748-104">SYNTAX</span></span>

### <span data-ttu-id="03748-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="03748-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03748-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="03748-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="03748-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03748-107">DESCRIPTION</span></span>
<span data-ttu-id="03748-108">Das **Cmdlet "Publish-AzWebApp"** lädt Inhalte in eine vorhandene Azure Web App hoch.</span><span class="sxs-lookup"><span data-stu-id="03748-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="03748-109">Der Inhalt sollte in einer ZIP-Datei gepackt werden, wenn Stapel wie .NET, Python oder Node oder eine WAR- oder JAR-Datei verwendet werden, wenn sie Java.</span><span class="sxs-lookup"><span data-stu-id="03748-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="03748-110">Der Inhalt sollte ohne zusätzliche Buildschritte während der Bereitstellung vor- und betriebsbereit sein.</span><span class="sxs-lookup"><span data-stu-id="03748-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="03748-111">Dieses Cmdlet verwendet die Features "Kudu Zipdeploy" und "Wardeploy" zum Bereitstellen von Inhalten.</span><span class="sxs-lookup"><span data-stu-id="03748-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="03748-112">Details zur Funktionsweise von Zipdeploy und Wardeploy und zum ordnungsgemäßen Packen einer Web App für die Bereitstellung finden Sie im Kudu-Wiki.</span><span class="sxs-lookup"><span data-stu-id="03748-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="03748-113"> https://aka.ms/kuduzipdeploy und enthalten hilfreiche Details zu https://aka.ms/kuduwardeploy Zipdeploy und Wardeploy.</span><span class="sxs-lookup"><span data-stu-id="03748-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="03748-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="03748-114">EXAMPLES</span></span>

### <span data-ttu-id="03748-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03748-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="03748-116">Lädt den Inhalt app.zip Web App namens "MyApp" hoch, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="03748-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="03748-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="03748-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="03748-118">Lädt den Inhalt von "javaproject.war" in den Stagingplatz der Web App namens "ContosoApp" hoch, die zur Ressourcengruppe "ContosoRG" gehört.</span><span class="sxs-lookup"><span data-stu-id="03748-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="03748-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="03748-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="03748-120">Lädt den Inhalt der app.zip in die Web App namens "ContosoApp" hoch, die zur Ressourcengruppe "ContosoRG" gehört.</span><span class="sxs-lookup"><span data-stu-id="03748-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="03748-121">Das Cmdlet wird in einem Hintergrundauftrag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03748-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="03748-122">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="03748-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="03748-123">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="03748-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="03748-124">Lädt den Inhalt von java_app.jar in die Web App namens "ContosoApp" hoch, die zur Ressourcengruppe "ContosoRG" gehört.</span><span class="sxs-lookup"><span data-stu-id="03748-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="03748-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03748-125">PARAMETERS</span></span>

### <span data-ttu-id="03748-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="03748-126">-ArchivePath</span></span>
<span data-ttu-id="03748-127">Der Pfad der Archivdatei.</span><span class="sxs-lookup"><span data-stu-id="03748-127">The path of the archive file.</span></span> <span data-ttu-id="03748-128">ZIP, WAR und JAR werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03748-128">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="03748-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03748-129">-AsJob</span></span>
<span data-ttu-id="03748-130">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="03748-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03748-131">-Force</span><span class="sxs-lookup"><span data-stu-id="03748-131">-Force</span></span>
<span data-ttu-id="03748-132">Option "Erzwingend entfernen"</span><span class="sxs-lookup"><span data-stu-id="03748-132">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="03748-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03748-133">-DefaultProfile</span></span>
<span data-ttu-id="03748-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="03748-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03748-135">-Name</span><span class="sxs-lookup"><span data-stu-id="03748-135">-Name</span></span>
<span data-ttu-id="03748-136">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="03748-136">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03748-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03748-137">-ResourceGroupName</span></span>
<span data-ttu-id="03748-138">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="03748-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03748-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="03748-139">-Slot</span></span>
<span data-ttu-id="03748-140">Der Name des Web-App-Slot.</span><span class="sxs-lookup"><span data-stu-id="03748-140">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03748-141">-WebApp</span><span class="sxs-lookup"><span data-stu-id="03748-141">-WebApp</span></span>
<span data-ttu-id="03748-142">Web -App-Objekt</span><span class="sxs-lookup"><span data-stu-id="03748-142">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03748-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03748-143">CommonParameters</span></span>
<span data-ttu-id="03748-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03748-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03748-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03748-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03748-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="03748-146">INPUTS</span></span>

### <span data-ttu-id="03748-147">System.String</span><span class="sxs-lookup"><span data-stu-id="03748-147">System.String</span></span>

### <span data-ttu-id="03748-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="03748-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="03748-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="03748-149">OUTPUTS</span></span>

### <span data-ttu-id="03748-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="03748-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="03748-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="03748-151">NOTES</span></span>

## <span data-ttu-id="03748-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="03748-152">RELATED LINKS</span></span>
