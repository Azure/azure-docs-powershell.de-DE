---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 726f991f5e51b6196b61a6e977ba1c5d4a1debf0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949843"
---
# <span data-ttu-id="8a482-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8a482-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="8a482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a482-102">SYNOPSIS</span></span>
<span data-ttu-id="8a482-103">Stellt mithilfe von zipdeploy eine Azure Web App aus einer ZIP-, JAR- oder WAR-Datei bereit.</span><span class="sxs-lookup"><span data-stu-id="8a482-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="8a482-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a482-104">SYNTAX</span></span>

### <span data-ttu-id="8a482-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8a482-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a482-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8a482-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="8a482-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a482-107">DESCRIPTION</span></span>
<span data-ttu-id="8a482-108">Das **Cmdlet Publish-AzWebApp** lädt Inhalte in eine vorhandene Azure Web App hoch.</span><span class="sxs-lookup"><span data-stu-id="8a482-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="8a482-109">Der Inhalt sollte in einer ZIP-Datei verpackt werden, wenn Stapel wie .NET, Python oder Node oder eine WAR- oder JAR-Datei verwendet werden, wenn sie Java.</span><span class="sxs-lookup"><span data-stu-id="8a482-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="8a482-110">Der Inhalt sollte ohne zusätzliche Buildschritte während der Bereitstellung vorab erstellt und einsatzbereit sein.</span><span class="sxs-lookup"><span data-stu-id="8a482-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="8a482-111">Dieses Cmdlet verwendet die Features "Kudu zipdeploy" und "wardeploy" zum Bereitstellen von Inhalten.</span><span class="sxs-lookup"><span data-stu-id="8a482-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="8a482-112">Details zur Funktionsweise von Zipdeploy und Wardeploy und zum ordnungsgemäßen Packen einer Web App für die Bereitstellung finden Sie im Kudu-Wiki.</span><span class="sxs-lookup"><span data-stu-id="8a482-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="8a482-113"> https://aka.ms/kuduzipdeploy und https://aka.ms/kuduwardeploy enthalten hilfreiche Details zu zipdeploy und wardeploy.</span><span class="sxs-lookup"><span data-stu-id="8a482-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="8a482-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a482-114">EXAMPLES</span></span>

### <span data-ttu-id="8a482-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a482-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="8a482-116">Lädt den Inhalt der app.zip in die Web-App mit dem Namen MyApp hoch, die zur Ressourcengruppe Default-Web-WestUS gehört.</span><span class="sxs-lookup"><span data-stu-id="8a482-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="8a482-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8a482-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="8a482-118">Lädt den Inhalt von javaproject.war in den Stagingplatz der Web-App namens ContosoApp hoch, die zur Ressourcengruppe ContosoRG gehört.</span><span class="sxs-lookup"><span data-stu-id="8a482-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="8a482-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8a482-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="8a482-120">Lädt den Inhalt der app.zip in die Web-App namens ContosoApp hoch, die zur Ressourcengruppe ContosoRG gehört.</span><span class="sxs-lookup"><span data-stu-id="8a482-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="8a482-121">Das Cmdlet wird in einem Hintergrundauftrag ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a482-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="8a482-122">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="8a482-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="8a482-123">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="8a482-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="8a482-124">Lädt den Inhalt von java_app.jar in die Web-App namens ContosoApp hoch, die zur Ressourcengruppe ContosoRG gehört.</span><span class="sxs-lookup"><span data-stu-id="8a482-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="8a482-125">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="8a482-125">Example 6</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Timeout 300000 -Force
```

<span data-ttu-id="8a482-126">Lädt den Inhalt von java_app.jar in die Web-App namens ContosoApp hoch, die zur Ressourcengruppe ContosoRG gehört.</span><span class="sxs-lookup"><span data-stu-id="8a482-126">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="8a482-127">Der Benutzer kann die Zeitspanne in Millisekunden so lange angeben, bis die Anforderung abfing.</span><span class="sxs-lookup"><span data-stu-id="8a482-127">User can Sets the timespan in Milliseconds to wait before the request times out.</span></span>

## <span data-ttu-id="8a482-128">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8a482-128">PARAMETERS</span></span>

### <span data-ttu-id="8a482-129">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="8a482-129">-ArchivePath</span></span>
<span data-ttu-id="8a482-130">Der Pfad der Archivdatei.</span><span class="sxs-lookup"><span data-stu-id="8a482-130">The path of the archive file.</span></span> <span data-ttu-id="8a482-131">ZIP, WAR und JAR werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8a482-131">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="8a482-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a482-132">-AsJob</span></span>
<span data-ttu-id="8a482-133">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8a482-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a482-134">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="8a482-134">-Force</span></span>
<span data-ttu-id="8a482-135">Option "Mit Gewalt entfernen"</span><span class="sxs-lookup"><span data-stu-id="8a482-135">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="8a482-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a482-136">-DefaultProfile</span></span>
<span data-ttu-id="8a482-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a482-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a482-138">-Name</span><span class="sxs-lookup"><span data-stu-id="8a482-138">-Name</span></span>
<span data-ttu-id="8a482-139">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="8a482-139">The name of the web app.</span></span>

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

### <span data-ttu-id="8a482-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a482-140">-ResourceGroupName</span></span>
<span data-ttu-id="8a482-141">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8a482-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="8a482-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="8a482-142">-Slot</span></span>
<span data-ttu-id="8a482-143">Der Name des Web-App-Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="8a482-143">The name of the web app slot.</span></span>

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

### <span data-ttu-id="8a482-144">-Timeout</span><span class="sxs-lookup"><span data-stu-id="8a482-144">-Timeout</span></span>
<span data-ttu-id="8a482-145">Legt die Zeitspanne in Millisekunden fest, die gewartet werden soll, bevor das Anforderungszeitfache erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="8a482-145">Sets the timespan in Milliseconds to wait before the request times out.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a482-146">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8a482-146">-WebApp</span></span>
<span data-ttu-id="8a482-147">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="8a482-147">The web app object</span></span>

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

### <span data-ttu-id="8a482-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a482-148">CommonParameters</span></span>
<span data-ttu-id="8a482-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a482-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a482-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a482-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a482-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a482-151">INPUTS</span></span>

### <span data-ttu-id="8a482-152">System.String</span><span class="sxs-lookup"><span data-stu-id="8a482-152">System.String</span></span>

### <span data-ttu-id="8a482-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8a482-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8a482-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a482-154">OUTPUTS</span></span>

### <span data-ttu-id="8a482-155">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8a482-155">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8a482-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8a482-156">NOTES</span></span>

## <span data-ttu-id="8a482-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8a482-157">RELATED LINKS</span></span>
