---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006083"
---
# <span data-ttu-id="e7ae9-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="e7ae9-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="e7ae9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ae9-103">Veröffentlichen eines Visual Studio-Webprojekts auf einer Microsoft Azure-Website mithilfe von WebDeploy</span><span class="sxs-lookup"><span data-stu-id="e7ae9-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="e7ae9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7ae9-104">SYNTAX</span></span>

### <span data-ttu-id="e7ae9-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="e7ae9-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ae9-106">Paket</span><span class="sxs-lookup"><span data-stu-id="e7ae9-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e7ae9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7ae9-107">DESCRIPTION</span></span>
<span data-ttu-id="e7ae9-108">Veröffentlichen eines Visual Studio-Webprojekts auf einer Microsoft Azure-Website mithilfe von WebDeploy</span><span class="sxs-lookup"><span data-stu-id="e7ae9-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="e7ae9-109">Sie kann entweder ein WebDeploy-Paket übernehmen und direkt veröffentlichen, oder Sie können ein Visual Studio-Webprojekt erstellen, das Projekt erstellen und veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="e7ae9-110">Außerdem können die Verbindungszeichenfolgen im Web.config während der Veröffentlichung ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="e7ae9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7ae9-111">EXAMPLES</span></span>

### <span data-ttu-id="e7ae9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7ae9-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="e7ae9-113">Erstellen Sie ein Visual Studio-Webprojekt mit der Konfiguration "Debuggen" (Bedeutung verwenden Sie Web.Debug.config), und veröffentlichen Sie auf einer Microsoft Azure-Website mithilfe von WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="e7ae9-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e7ae9-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="e7ae9-115">Veröffentlichen Sie eine ZIP-Datei für WebDeploy-Pakete auf einer Microsoft Azure-Website mit WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="e7ae9-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e7ae9-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="e7ae9-117">Veröffentlichen eines WebDeploy-Paketordners auf einer Microsoft Azure-Website mithilfe von WebDeploy</span><span class="sxs-lookup"><span data-stu-id="e7ae9-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="e7ae9-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e7ae9-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="e7ae9-119">Erstellen Sie ein Visual Studio-Webprojekt, überschreiben Sie die Verbindungszeichenfolge "DefaultConnection" in Web.config, und veröffentlichen Sie Sie mithilfe von WebDeploy auf einer Microsoft Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="e7ae9-120">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="e7ae9-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="e7ae9-121">Erstellen Sie ein Visual Studio-Webprojekt, überschreiben Sie die Verbindungszeichenfolge "DefaultConnection" in Web.config, und veröffentlichen Sie Sie mithilfe von WebDeploy auf einer Microsoft Azure-Website.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="e7ae9-122">Beachten Sie, dass-DefaultConnection ein dynamischer Parameter ist, der durch Analyse Web.config hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="e7ae9-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7ae9-123">PARAMETERS</span></span>

### <span data-ttu-id="e7ae9-124">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e7ae9-124">-Configuration</span></span>
<span data-ttu-id="e7ae9-125">Die Konfiguration, die zum Erstellen des Visual Studio-Webanwendungsprojekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae9-126">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e7ae9-126">-ConnectionString</span></span>
<span data-ttu-id="e7ae9-127">Die für die Bereitstellung zu verwendenden Verbindungszeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae9-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="e7ae9-128">-DoNotDelete</span></span>
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

### <span data-ttu-id="e7ae9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e7ae9-129">-Name</span></span>
<span data-ttu-id="e7ae9-130">Der Name der Website.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-130">The web site name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae9-131">-Paket</span><span class="sxs-lookup"><span data-stu-id="e7ae9-131">-Package</span></span>
<span data-ttu-id="e7ae9-132">Der WebDeploy-Paketordner für die ZIP-Datei des Visual Studio-Webanwendungsprojekts, das veröffentlicht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae9-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7ae9-133">-Profile</span></span>
<span data-ttu-id="e7ae9-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7ae9-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae9-136">-Projectdatei</span><span class="sxs-lookup"><span data-stu-id="e7ae9-136">-ProjectFile</span></span>
<span data-ttu-id="e7ae9-137">Das zu veröffentlichende Visual Studio-Webanwendungsprojekt.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae9-138">-Setparameterdatei</span><span class="sxs-lookup"><span data-stu-id="e7ae9-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae9-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="e7ae9-139">-SkipAppData</span></span>
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

### <span data-ttu-id="e7ae9-140">-Slot</span><span class="sxs-lookup"><span data-stu-id="e7ae9-140">-Slot</span></span>
<span data-ttu-id="e7ae9-141">Der Name des Website Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-141">The web site slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae9-142">-Tokens</span><span class="sxs-lookup"><span data-stu-id="e7ae9-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ae9-143">CommonParameters</span></span>
<span data-ttu-id="e7ae9-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ae9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ae9-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7ae9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ae9-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7ae9-146">INPUTS</span></span>

## <span data-ttu-id="e7ae9-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7ae9-147">OUTPUTS</span></span>

## <span data-ttu-id="e7ae9-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7ae9-148">NOTES</span></span>

## <span data-ttu-id="e7ae9-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7ae9-149">RELATED LINKS</span></span>

[<span data-ttu-id="e7ae9-150">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e7ae9-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="e7ae9-151">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e7ae9-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="e7ae9-152">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e7ae9-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="e7ae9-153">Satz-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e7ae9-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


