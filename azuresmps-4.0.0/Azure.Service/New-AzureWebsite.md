---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110477"
---
# <span data-ttu-id="18aed-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="18aed-101">New-AzureWebsite</span></span>

## <span data-ttu-id="18aed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18aed-102">SYNOPSIS</span></span>
<span data-ttu-id="18aed-103">Erstellen Sie eine neue Website, die in Azure ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="18aed-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="18aed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18aed-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="18aed-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18aed-105">DESCRIPTION</span></span>
<span data-ttu-id="18aed-106">In diesem Thema wird das Cmdlet in der Version 0.8.10 des Microsoft Azure -PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="18aed-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="18aed-107">Um die Version des verwendeten Moduls zu erhalten, geben Sie in der Azure PowerShell-Konsole " `(Get-Module -Name Azure).Version` ein.</span><span class="sxs-lookup"><span data-stu-id="18aed-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="18aed-108">Das Cmdlet erstellt eine neue Website, die in Azure ausgeführt werden kann, und bereitet sich auf die Bereitstellung über GitHub vor.</span><span class="sxs-lookup"><span data-stu-id="18aed-108">The cmdlet creates a new website to run in Azure and prepares for deployment through GitHub.</span></span>

## <span data-ttu-id="18aed-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="18aed-109">EXAMPLES</span></span>

### <span data-ttu-id="18aed-110">Beispiel 1: Erstellen einer neuen Website mit Git</span><span class="sxs-lookup"><span data-stu-id="18aed-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="18aed-111">In diesem Beispiel werden eine neue Website in Azure und ein lokales Git-Repository erstellt, das zum Bereitstellen von Dateien auf der neuen Website verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="18aed-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="18aed-112">Beispiel 2: Erstellen einer in GitHub integrierten Website</span><span class="sxs-lookup"><span data-stu-id="18aed-112">Example 2: Create website integrated with GitHub</span></span>
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

<span data-ttu-id="18aed-113">In diesem Beispiel wird eine neue Website erstellt, die mit einem GitHub-Repository namens "myaccount/myrepo" verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="18aed-113">This example creates a new website linked to a GitHub repository named myaccount/myrepo.</span></span>
<span data-ttu-id="18aed-114">Commits für das GitHub-Repository werden an die Website in Azure übertragen.</span><span class="sxs-lookup"><span data-stu-id="18aed-114">Commits to the GitHub repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="18aed-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18aed-115">PARAMETERS</span></span>

### <span data-ttu-id="18aed-116">-Git</span><span class="sxs-lookup"><span data-stu-id="18aed-116">-Git</span></span>
<span data-ttu-id="18aed-117">Richtet ein lokales Git-Repository ein und verknüpft es mit der Website.</span><span class="sxs-lookup"><span data-stu-id="18aed-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="18aed-118">Falls angegeben, richtet dieser Parameter ein Git-Repository im lokalen Verzeichnis ein und fügt ein Remoterepository mit dem Namen "azure" hinzu, das mit der Website in Azure verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="18aed-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18aed-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="18aed-119">-GitHub</span></span>
<span data-ttu-id="18aed-120">Gibt an, dass dieses Cmdlet die neue Website mit einem vorhandenen GitHub-Repository verknüpft.</span><span class="sxs-lookup"><span data-stu-id="18aed-120">Indicates that this cmdlet links the new website to an existing GitHub repository.</span></span>
<span data-ttu-id="18aed-121">Commits für das Repository "Giuthub" werden auf die Website in Azure übertragen.</span><span class="sxs-lookup"><span data-stu-id="18aed-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18aed-122">-GitHubCredentials</span><span class="sxs-lookup"><span data-stu-id="18aed-122">-GitHubCredentials</span></span>
<span data-ttu-id="18aed-123">Gibt den Benutzernamen und das Kennwort als Anmeldeinformationen an, um eine Verbindung mit GitHub herzustellen.</span><span class="sxs-lookup"><span data-stu-id="18aed-123">Specifies the user name and password credentials to connect to GitHub.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18aed-124">-GitHubRepository</span><span class="sxs-lookup"><span data-stu-id="18aed-124">-GitHubRepository</span></span>
<span data-ttu-id="18aed-125">Gibt den vollständigen Namen des GitHub-Repositorys an, das mit dieser Website zu verknüpfen ist.</span><span class="sxs-lookup"><span data-stu-id="18aed-125">Specifies the full name of the GitHub repository to link to this website.</span></span>
<span data-ttu-id="18aed-126">Beispiel: `myaccount/myrepo` "</span><span class="sxs-lookup"><span data-stu-id="18aed-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="18aed-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="18aed-127">-Hostname</span></span>
<span data-ttu-id="18aed-128">Gibt einen alternativen Hostnamen für die neue Website an.</span><span class="sxs-lookup"><span data-stu-id="18aed-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="18aed-129">-Location</span><span class="sxs-lookup"><span data-stu-id="18aed-129">-Location</span></span>
<span data-ttu-id="18aed-130">Gibt den Speicherort des Rechenzentrums an, in dem Sie die Website bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="18aed-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="18aed-131">-Name</span><span class="sxs-lookup"><span data-stu-id="18aed-131">-Name</span></span>
<span data-ttu-id="18aed-132">Gibt einen Namen für die Website an.</span><span class="sxs-lookup"><span data-stu-id="18aed-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="18aed-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="18aed-133">-Profile</span></span>
<span data-ttu-id="18aed-134">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="18aed-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="18aed-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="18aed-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="18aed-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="18aed-136">-PublishingUsername</span></span>
<span data-ttu-id="18aed-137">Gibt den Benutzernamen an, den Sie im Azure-Portal für die Bereitstellung von Git angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="18aed-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="18aed-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="18aed-138">-Slot</span></span>
<span data-ttu-id="18aed-139">Gibt einen Slotnamen für die Website an.</span><span class="sxs-lookup"><span data-stu-id="18aed-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="18aed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18aed-140">CommonParameters</span></span>
<span data-ttu-id="18aed-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18aed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18aed-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18aed-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18aed-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="18aed-143">INPUTS</span></span>

## <span data-ttu-id="18aed-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="18aed-144">OUTPUTS</span></span>

## <span data-ttu-id="18aed-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="18aed-145">NOTES</span></span>

## <span data-ttu-id="18aed-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="18aed-146">RELATED LINKS</span></span>

[<span data-ttu-id="18aed-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="18aed-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


