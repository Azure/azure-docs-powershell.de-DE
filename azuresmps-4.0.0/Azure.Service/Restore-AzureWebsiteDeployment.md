---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005669"
---
# <span data-ttu-id="ad668-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="ad668-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="ad668-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad668-102">SYNOPSIS</span></span>
<span data-ttu-id="ad668-103">Stellt eine vorherige Bereitstellung einer Website in Azure erneut bereit.</span><span class="sxs-lookup"><span data-stu-id="ad668-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="ad668-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad668-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad668-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad668-105">DESCRIPTION</span></span>
<span data-ttu-id="ad668-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ad668-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ad668-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ad668-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ad668-108">Mit dem Cmdlet **Restore-AzureWebsiteDeployment** wird eine vorherige Bereitstellung einer Website in Azure erneut bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ad668-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="ad668-109">Dieser Vorgang ersetzt die aktuelle Bereitstellung durch die ausgewählte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="ad668-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="ad668-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad668-110">EXAMPLES</span></span>

### <span data-ttu-id="ad668-111">Beispiel 1: Erneutes Bereitstelleneiner Website</span><span class="sxs-lookup"><span data-stu-id="ad668-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="ad668-112">Mit diesem Befehl wird die Bereitstellung mit der ID f876543210 für die Website mit dem Namen ContosoSite erneut bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ad668-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="ad668-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad668-113">PARAMETERS</span></span>

### <span data-ttu-id="ad668-114">-Commit-Nr</span><span class="sxs-lookup"><span data-stu-id="ad668-114">-CommitId</span></span>
<span data-ttu-id="ad668-115">Gibt den Bezeichner der bereitzustellenden Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="ad668-115">Specifies the identifier of the deployment to redeploy.</span></span>

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

### <span data-ttu-id="ad668-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ad668-116">-Force</span></span>
<span data-ttu-id="ad668-117">Wenn diese Option aktiviert ist, wird die vorherige Bereitstellung erneut bereitgestellt, ohne dass eine Bestätigung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ad668-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ad668-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ad668-118">-Name</span></span>
<span data-ttu-id="ad668-119">Gibt den Namen der Website an, die erneut bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad668-119">Specifies the name of the website to redeploy.</span></span>

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

### <span data-ttu-id="ad668-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="ad668-120">-Profile</span></span>
<span data-ttu-id="ad668-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ad668-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad668-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ad668-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ad668-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="ad668-123">-Slot</span></span>
<span data-ttu-id="ad668-124">Gibt den Namen des Steckplatzes an.</span><span class="sxs-lookup"><span data-stu-id="ad668-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="ad668-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad668-125">-Confirm</span></span>
<span data-ttu-id="ad668-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad668-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad668-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad668-127">-WhatIf</span></span>
<span data-ttu-id="ad668-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad668-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad668-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad668-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad668-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad668-130">CommonParameters</span></span>
<span data-ttu-id="ad668-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad668-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad668-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad668-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad668-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad668-133">INPUTS</span></span>

## <span data-ttu-id="ad668-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad668-134">OUTPUTS</span></span>

## <span data-ttu-id="ad668-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad668-135">NOTES</span></span>

## <span data-ttu-id="ad668-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad668-136">RELATED LINKS</span></span>

[<span data-ttu-id="ad668-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ad668-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="ad668-138">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="ad668-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


