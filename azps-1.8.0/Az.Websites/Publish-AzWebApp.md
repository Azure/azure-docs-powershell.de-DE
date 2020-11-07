---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658530"
---
# <span data-ttu-id="cc35e-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cc35e-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="cc35e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc35e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc35e-103">Stellt eine Azure Web-App aus einer ZIP-, JAR-oder war-Datei mithilfe von zipdeploy bereit.</span><span class="sxs-lookup"><span data-stu-id="cc35e-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="cc35e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc35e-104">SYNTAX</span></span>

### <span data-ttu-id="cc35e-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="cc35e-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc35e-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="cc35e-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc35e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc35e-107">DESCRIPTION</span></span>
<span data-ttu-id="cc35e-108">Mit dem Cmdlet " **Publish-AzWebApp** " wird der Inhalt in eine vorhandene Azure Web App hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="cc35e-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="cc35e-109">Die Inhalte sollten in einer ZIP-Datei verpackt werden, wenn Sie Stapel wie .net, Python oder Node oder eine war-oder JAR-Datei verwenden, wenn Sie Java verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc35e-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="cc35e-110">Die Inhalte sollten während der Bereitstellung vorinstalliert und ohne zusätzliche Build-Schritte ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="cc35e-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="cc35e-111">Dieses Cmdlet verwendet die Features Kudu zipdeploy und wardeploy, um Inhalte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cc35e-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="cc35e-112">Im Kudu-wiki finden Sie Informationen dazu, wie zipdeploy und wardeploy funktionieren, und wie Sie eine Web-App für die Bereitstellung richtig verpacken.</span><span class="sxs-lookup"><span data-stu-id="cc35e-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="cc35e-113"> https://aka.ms/kuduzipdeploy und https://aka.ms/kuduwardeploy enthalten hilfreiche Informationen zu zipdeploy und wardeploy.</span><span class="sxs-lookup"><span data-stu-id="cc35e-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="cc35e-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc35e-114">EXAMPLES</span></span>

### <span data-ttu-id="cc35e-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc35e-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="cc35e-116">Lädt den Inhalt von app.zip in die Web-App mit dem Namen MyApp, die zur Ressourcengruppe Standard-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="cc35e-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="cc35e-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cc35e-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="cc35e-118">Lädt den Inhalt von javaproject. war in den Staging-Slot der Web-App mit dem Namen ContosoApp, die zur Ressourcengruppe ContosoRG gehört.</span><span class="sxs-lookup"><span data-stu-id="cc35e-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="cc35e-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cc35e-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="cc35e-120">Lädt den Inhalt von app.zip in die Web-App mit dem Namen ContosoApp, die zu der Ressourcengruppe ContosoRG gehört.</span><span class="sxs-lookup"><span data-stu-id="cc35e-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="cc35e-121">Das Cmdlet wird in einem Hintergrundjob ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc35e-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="cc35e-122">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="cc35e-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

<span data-ttu-id="cc35e-123">Lädt den Inhalt von java_app. jar in die Web-App mit dem Namen ContosoApp, die zur Ressourcengruppe ContosoRG gehört.</span><span class="sxs-lookup"><span data-stu-id="cc35e-123">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="cc35e-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc35e-124">PARAMETERS</span></span>

### <span data-ttu-id="cc35e-125">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="cc35e-125">-ArchivePath</span></span>
<span data-ttu-id="cc35e-126">Der Pfad der Archivdatei.</span><span class="sxs-lookup"><span data-stu-id="cc35e-126">The path of the archive file.</span></span> <span data-ttu-id="cc35e-127">ZIP, war und JAR werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc35e-127">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="cc35e-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc35e-128">-AsJob</span></span>
<span data-ttu-id="cc35e-129">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cc35e-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc35e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc35e-130">-DefaultProfile</span></span>
<span data-ttu-id="cc35e-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc35e-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc35e-132">-Name</span><span class="sxs-lookup"><span data-stu-id="cc35e-132">-Name</span></span>
<span data-ttu-id="cc35e-133">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="cc35e-133">The name of the web app.</span></span>

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

### <span data-ttu-id="cc35e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc35e-134">-ResourceGroupName</span></span>
<span data-ttu-id="cc35e-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc35e-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="cc35e-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="cc35e-136">-Slot</span></span>
<span data-ttu-id="cc35e-137">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="cc35e-137">The name of the web app slot.</span></span>

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

### <span data-ttu-id="cc35e-138">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="cc35e-138">-WebApp</span></span>
<span data-ttu-id="cc35e-139">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="cc35e-139">The web app object</span></span>

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

### <span data-ttu-id="cc35e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc35e-140">CommonParameters</span></span>
<span data-ttu-id="cc35e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc35e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc35e-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc35e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc35e-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc35e-143">INPUTS</span></span>

### <span data-ttu-id="cc35e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cc35e-144">System.String</span></span>

### <span data-ttu-id="cc35e-145">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="cc35e-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cc35e-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc35e-146">OUTPUTS</span></span>

### <span data-ttu-id="cc35e-147">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="cc35e-147">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cc35e-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc35e-148">NOTES</span></span>

## <span data-ttu-id="cc35e-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc35e-149">RELATED LINKS</span></span>
