---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006715"
---
# <span data-ttu-id="259d6-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="259d6-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="259d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="259d6-102">SYNOPSIS</span></span>
<span data-ttu-id="259d6-103">Ruft die Bereitstellungen für eine Website ab.</span><span class="sxs-lookup"><span data-stu-id="259d6-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="259d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="259d6-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="259d6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="259d6-105">DESCRIPTION</span></span>
<span data-ttu-id="259d6-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="259d6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="259d6-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="259d6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="259d6-108">Ruft die Bereitstellungen für eine Website in Azure ab.</span><span class="sxs-lookup"><span data-stu-id="259d6-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="259d6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="259d6-109">EXAMPLES</span></span>

## <span data-ttu-id="259d6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="259d6-110">PARAMETERS</span></span>

### <span data-ttu-id="259d6-111">-Commit-Nr</span><span class="sxs-lookup"><span data-stu-id="259d6-111">-CommitId</span></span>
<span data-ttu-id="259d6-112">Gibt die eindeutige ID für die Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="259d6-112">Specifies the unique ID for the deployment.</span></span>

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

### <span data-ttu-id="259d6-113">-Details</span><span class="sxs-lookup"><span data-stu-id="259d6-113">-Details</span></span>
<span data-ttu-id="259d6-114">Zeigt detaillierte Informationen zu den Bereitstellungen an.</span><span class="sxs-lookup"><span data-stu-id="259d6-114">Shows detailed information about the deployments.</span></span>

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

### <span data-ttu-id="259d6-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="259d6-115">-MaxResults</span></span>
<span data-ttu-id="259d6-116">Gibt die größte Anzahl von Ergebnissen an, die der Befehl zurückgeben soll.</span><span class="sxs-lookup"><span data-stu-id="259d6-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="259d6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="259d6-117">-Name</span></span>
<span data-ttu-id="259d6-118">Gibt den Namen der Website an, für die Sie Bereitstellungsinformationen abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="259d6-118">Specifies the name of the website for which you want to get deployment information.</span></span>

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

### <span data-ttu-id="259d6-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="259d6-119">-Profile</span></span>
<span data-ttu-id="259d6-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="259d6-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="259d6-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="259d6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="259d6-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="259d6-122">-Slot</span></span>
<span data-ttu-id="259d6-123">Gibt den Namen des Steckplatzes an.</span><span class="sxs-lookup"><span data-stu-id="259d6-123">Specifies the slot name.</span></span>

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

### <span data-ttu-id="259d6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259d6-124">CommonParameters</span></span>
<span data-ttu-id="259d6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="259d6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259d6-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="259d6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259d6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="259d6-127">INPUTS</span></span>

## <span data-ttu-id="259d6-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="259d6-128">OUTPUTS</span></span>

## <span data-ttu-id="259d6-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="259d6-129">NOTES</span></span>

## <span data-ttu-id="259d6-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="259d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="259d6-131">Wiederherstellen – AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="259d6-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


