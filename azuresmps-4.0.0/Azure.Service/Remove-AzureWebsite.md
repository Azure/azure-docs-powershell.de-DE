---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005689"
---
# <span data-ttu-id="55cd8-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="55cd8-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="55cd8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="55cd8-103">Entfernt die angegebene Website aus Azure.</span><span class="sxs-lookup"><span data-stu-id="55cd8-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="55cd8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55cd8-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55cd8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="55cd8-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="55cd8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="55cd8-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="55cd8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="55cd8-108">Das Cmdlet **Remove-AzureWebsite** entfernt die angegebene Website aus Azure, entweder mit oder ohne Aufforderung zur Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="55cd8-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="55cd8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55cd8-109">EXAMPLES</span></span>

### <span data-ttu-id="55cd8-110">Beispiel 1: Entfernen der aktuellen Website</span><span class="sxs-lookup"><span data-stu-id="55cd8-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="55cd8-111">In diesem Beispiel wird die Website in Azure entfernt, die dem aktuellen Verzeichnis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="55cd8-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="55cd8-112">Beispiel 2: Entfernen einer Website ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="55cd8-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="55cd8-113">In diesem Beispiel wird die Website mit dem Namen "Meine Website" gelöscht, ohne dass eine Bestätigung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="55cd8-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="55cd8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="55cd8-114">PARAMETERS</span></span>

### <span data-ttu-id="55cd8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="55cd8-115">-Force</span></span>
<span data-ttu-id="55cd8-116">Wenn angegeben, wird die angegebene Website ohne Aufforderung zur Bestätigung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="55cd8-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

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

### <span data-ttu-id="55cd8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="55cd8-117">-Name</span></span>
<span data-ttu-id="55cd8-118">Gibt den Namen der Website an, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="55cd8-118">Specifies the name of the website to delete.</span></span>

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

### <span data-ttu-id="55cd8-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="55cd8-119">-Profile</span></span>
<span data-ttu-id="55cd8-120">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="55cd8-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="55cd8-121">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="55cd8-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="55cd8-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="55cd8-122">-Slot</span></span>
<span data-ttu-id="55cd8-123">Gibt den Steckplatznamen der Website an.</span><span class="sxs-lookup"><span data-stu-id="55cd8-123">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="55cd8-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55cd8-124">-Confirm</span></span>
<span data-ttu-id="55cd8-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55cd8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55cd8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55cd8-126">-WhatIf</span></span>
<span data-ttu-id="55cd8-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55cd8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55cd8-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55cd8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55cd8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55cd8-129">CommonParameters</span></span>
<span data-ttu-id="55cd8-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55cd8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55cd8-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55cd8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55cd8-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55cd8-132">INPUTS</span></span>

## <span data-ttu-id="55cd8-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55cd8-133">OUTPUTS</span></span>

## <span data-ttu-id="55cd8-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="55cd8-134">NOTES</span></span>

## <span data-ttu-id="55cd8-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55cd8-135">RELATED LINKS</span></span>

[<span data-ttu-id="55cd8-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="55cd8-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


