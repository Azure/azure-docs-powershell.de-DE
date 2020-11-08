---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006390"
---
# <span data-ttu-id="95bbd-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95bbd-101">New-AzureWebsite</span></span>

## <span data-ttu-id="95bbd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="95bbd-103">Erstellen Sie eine neue Website, die in Azure ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95bbd-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="95bbd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95bbd-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="95bbd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95bbd-105">DESCRIPTION</span></span>
<span data-ttu-id="95bbd-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="95bbd-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="95bbd-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="95bbd-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="95bbd-108">Das Cmdlet erstellt eine neue Website, die in Azure ausgeführt werden soll, und bereitet sich auf die Bereitstellung über GitHub vor.</span><span class="sxs-lookup"><span data-stu-id="95bbd-108">The cmdlet creates a new website to run in Azure and prepares for deployment through Github.</span></span>

## <span data-ttu-id="95bbd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95bbd-109">EXAMPLES</span></span>

### <span data-ttu-id="95bbd-110">Beispiel 1: Erstellen einer neuen Website mit git</span><span class="sxs-lookup"><span data-stu-id="95bbd-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="95bbd-111">In diesem Beispiel wird eine neue Website in Azure und ein lokales git-Repository erstellt, das zum Bereitstellen von Dateien auf der neuen Website verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95bbd-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="95bbd-112">Beispiel 2: Erstellen einer in GitHub integrierten Website</span><span class="sxs-lookup"><span data-stu-id="95bbd-112">Example 2: Create website integrated with Github</span></span>
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

<span data-ttu-id="95bbd-113">In diesem Beispiel wird eine neue Website erstellt, die mit einem GitHub-Repository namens "MyAccount/myrepo" verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="95bbd-113">This example creates a new website linked to a Github repository named myaccount/myrepo.</span></span>
<span data-ttu-id="95bbd-114">Commits für das GitHub-Repository werden in Azure auf die Website verschoben.</span><span class="sxs-lookup"><span data-stu-id="95bbd-114">Commits to the Github repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="95bbd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="95bbd-115">PARAMETERS</span></span>

### <span data-ttu-id="95bbd-116">-Git</span><span class="sxs-lookup"><span data-stu-id="95bbd-116">-Git</span></span>
<span data-ttu-id="95bbd-117">Richtet ein lokales git-Repository ein und verknüpft es mit der Website.</span><span class="sxs-lookup"><span data-stu-id="95bbd-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="95bbd-118">Falls angegeben, richtet dieser Parameter ein git-Repository im lokalen Verzeichnis ein und fügt ein Remote-Repository mit dem Namen "Azure" hinzu, das mit der Website in Azure verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="95bbd-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

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

### <span data-ttu-id="95bbd-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="95bbd-119">-GitHub</span></span>
<span data-ttu-id="95bbd-120">Gibt an, dass dieses Cmdlet die neue Website mit einem vorhandenen GitHub-Repository verknüpft.</span><span class="sxs-lookup"><span data-stu-id="95bbd-120">Indicates that this cmdlet links the new website to an existing Github repository.</span></span>
<span data-ttu-id="95bbd-121">Commits für das Giuthub-Repository werden in Azure auf die Website verschoben.</span><span class="sxs-lookup"><span data-stu-id="95bbd-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

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

### <span data-ttu-id="95bbd-122">-GithubCredentials</span><span class="sxs-lookup"><span data-stu-id="95bbd-122">-GithubCredentials</span></span>
<span data-ttu-id="95bbd-123">Gibt den Benutzernamen und das Kennwort für das Herstellen einer Verbindung mit GitHub an.</span><span class="sxs-lookup"><span data-stu-id="95bbd-123">Specifies the user name and password credentials to connect to Github.</span></span>

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

### <span data-ttu-id="95bbd-124">-GithubRepository</span><span class="sxs-lookup"><span data-stu-id="95bbd-124">-GithubRepository</span></span>
<span data-ttu-id="95bbd-125">Gibt den vollständigen Namen des GitHub-Repositorys an, das mit dieser Website verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="95bbd-125">Specifies the full name of the Github repository to link to this website.</span></span>
<span data-ttu-id="95bbd-126">Beispiel: `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="95bbd-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="95bbd-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="95bbd-127">-Hostname</span></span>
<span data-ttu-id="95bbd-128">Gibt einen alternativen Hostnamen für die neue Website an.</span><span class="sxs-lookup"><span data-stu-id="95bbd-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="95bbd-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="95bbd-129">-Location</span></span>
<span data-ttu-id="95bbd-130">Gibt den Speicherort des Rechenzentrums an, in dem die Website bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95bbd-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="95bbd-131">-Name</span><span class="sxs-lookup"><span data-stu-id="95bbd-131">-Name</span></span>
<span data-ttu-id="95bbd-132">Gibt einen Namen für die Website an.</span><span class="sxs-lookup"><span data-stu-id="95bbd-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="95bbd-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="95bbd-133">-Profile</span></span>
<span data-ttu-id="95bbd-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="95bbd-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95bbd-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="95bbd-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95bbd-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="95bbd-136">-PublishingUsername</span></span>
<span data-ttu-id="95bbd-137">Gibt den Benutzernamen an, den Sie im Azure-Portal für die git-Bereitstellung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="95bbd-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="95bbd-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="95bbd-138">-Slot</span></span>
<span data-ttu-id="95bbd-139">Gibt einen Steckplatznamen für die Website an.</span><span class="sxs-lookup"><span data-stu-id="95bbd-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="95bbd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bbd-140">CommonParameters</span></span>
<span data-ttu-id="95bbd-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95bbd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bbd-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95bbd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bbd-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95bbd-143">INPUTS</span></span>

## <span data-ttu-id="95bbd-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95bbd-144">OUTPUTS</span></span>

## <span data-ttu-id="95bbd-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="95bbd-145">NOTES</span></span>

## <span data-ttu-id="95bbd-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95bbd-146">RELATED LINKS</span></span>

[<span data-ttu-id="95bbd-147">Satz-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95bbd-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


