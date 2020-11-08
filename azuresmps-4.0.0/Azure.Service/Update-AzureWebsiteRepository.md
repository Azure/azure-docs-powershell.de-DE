---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006049"
---
# <span data-ttu-id="0f9d5-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="0f9d5-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="0f9d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f9d5-103">Aktualisiert die Remote-Repositories eines lokalen git-Repositorys für alle Slots.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="0f9d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f9d5-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f9d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f9d5-105">DESCRIPTION</span></span>
<span data-ttu-id="0f9d5-106">Das Cmdlet **Update-AzureWebsiteRepository** aktualisiert die Remote-Repositories eines lokalen git-Repositorys für alle Slots.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="0f9d5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f9d5-107">EXAMPLES</span></span>

### <span data-ttu-id="0f9d5-108">Beispiel 1: Aktualisieren von Website-Remote Repositories</span><span class="sxs-lookup"><span data-stu-id="0f9d5-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="0f9d5-109">Aktualisiert die Remote-Repositories eines lokalen git-Repositorys für alle Slots für Website mywebsite.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="0f9d5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f9d5-110">PARAMETERS</span></span>

### <span data-ttu-id="0f9d5-111">-Name</span><span class="sxs-lookup"><span data-stu-id="0f9d5-111">-Name</span></span>
<span data-ttu-id="0f9d5-112">Der Name der Website.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-112">The name of the website.</span></span>

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

### <span data-ttu-id="0f9d5-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f9d5-113">-Profile</span></span>
<span data-ttu-id="0f9d5-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f9d5-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f9d5-116">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="0f9d5-116">-PublishingUsername</span></span>
<span data-ttu-id="0f9d5-117">Der Benutzername, den Sie im Microsoft Azure-Portal für die git-Bereitstellung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f9d5-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0f9d5-118">-Confirm</span></span>
<span data-ttu-id="0f9d5-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f9d5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f9d5-120">-WhatIf</span></span>
<span data-ttu-id="0f9d5-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f9d5-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f9d5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9d5-123">CommonParameters</span></span>
<span data-ttu-id="0f9d5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f9d5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9d5-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f9d5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f9d5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f9d5-126">INPUTS</span></span>

## <span data-ttu-id="0f9d5-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f9d5-127">OUTPUTS</span></span>

## <span data-ttu-id="0f9d5-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f9d5-128">NOTES</span></span>

## <span data-ttu-id="0f9d5-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f9d5-129">RELATED LINKS</span></span>

[<span data-ttu-id="0f9d5-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0f9d5-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="0f9d5-131">Neu – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0f9d5-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="0f9d5-132">Anfang-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0f9d5-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="0f9d5-133">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0f9d5-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


