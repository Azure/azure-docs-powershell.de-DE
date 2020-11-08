---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006677"
---
# <span data-ttu-id="bf69a-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bf69a-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="bf69a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf69a-102">SYNOPSIS</span></span>
<span data-ttu-id="bf69a-103">Entfernt das angegebene Azure Media Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="bf69a-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="bf69a-104">**Hinweis:**  Diese Version ist veraltet, bitte lesen Sie die [neuere Version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="bf69a-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="bf69a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf69a-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf69a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf69a-106">DESCRIPTION</span></span>
<span data-ttu-id="bf69a-107">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bf69a-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bf69a-108">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bf69a-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bf69a-109">Das Cmdlet **Remove-AzureMediaServicesAccount** entfernt ein Media Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="bf69a-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="bf69a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf69a-110">EXAMPLES</span></span>

### <span data-ttu-id="bf69a-111">Beispiel 1: Löschen eines Media Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="bf69a-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="bf69a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf69a-112">PARAMETERS</span></span>

### <span data-ttu-id="bf69a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bf69a-113">-Force</span></span>
<span data-ttu-id="bf69a-114">Wenn der Schalter *Force* angegeben wird, wird der Löschvorgang nicht bestätigt.</span><span class="sxs-lookup"><span data-stu-id="bf69a-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="bf69a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bf69a-115">-Name</span></span>
<span data-ttu-id="bf69a-116">Der Name des Media Services-Kontos.</span><span class="sxs-lookup"><span data-stu-id="bf69a-116">The Media Services account name.</span></span>

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

### <span data-ttu-id="bf69a-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="bf69a-117">-Profile</span></span>
<span data-ttu-id="bf69a-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="bf69a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf69a-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="bf69a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf69a-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf69a-120">-Confirm</span></span>
<span data-ttu-id="bf69a-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf69a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf69a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf69a-122">-WhatIf</span></span>
<span data-ttu-id="bf69a-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf69a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf69a-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf69a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf69a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf69a-125">CommonParameters</span></span>
<span data-ttu-id="bf69a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf69a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf69a-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf69a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf69a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf69a-128">INPUTS</span></span>

## <span data-ttu-id="bf69a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf69a-129">OUTPUTS</span></span>

## <span data-ttu-id="bf69a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf69a-130">NOTES</span></span>

## <span data-ttu-id="bf69a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf69a-131">RELATED LINKS</span></span>

[<span data-ttu-id="bf69a-132">Verwenden von Azure PowerShell für Mediendienste</span><span class="sxs-lookup"><span data-stu-id="bf69a-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="bf69a-133">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bf69a-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="bf69a-134">Neu – AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bf69a-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)


