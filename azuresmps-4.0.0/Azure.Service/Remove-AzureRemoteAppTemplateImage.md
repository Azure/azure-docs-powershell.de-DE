---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006355"
---
# <span data-ttu-id="faeeb-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="faeeb-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="faeeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="faeeb-102">SYNOPSIS</span></span>
<span data-ttu-id="faeeb-103">Löscht ein Azure RemoteApp-Vorlagenbild.</span><span class="sxs-lookup"><span data-stu-id="faeeb-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="faeeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="faeeb-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="faeeb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faeeb-105">DESCRIPTION</span></span>
<span data-ttu-id="faeeb-106">Das Cmdlet **Remove-AzureRemoteAppTemplateImage** löscht ein Azure RemoteApp-Vorlagenbild.</span><span class="sxs-lookup"><span data-stu-id="faeeb-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="faeeb-107">Ein Vorlagenbild kann nur gelöscht werden, wenn es nicht mit einer Azure RemoteApp-Sammlung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="faeeb-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="faeeb-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="faeeb-108">EXAMPLES</span></span>

### <span data-ttu-id="faeeb-109">Beispiel 1: Löschen eines Vorlagenbilds</span><span class="sxs-lookup"><span data-stu-id="faeeb-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="faeeb-110">Mit diesem Befehl wird das Vorlagenbild mit dem Namen ContosoApps gelöscht.</span><span class="sxs-lookup"><span data-stu-id="faeeb-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="faeeb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="faeeb-111">PARAMETERS</span></span>

### <span data-ttu-id="faeeb-112">-Bildname</span><span class="sxs-lookup"><span data-stu-id="faeeb-112">-ImageName</span></span>
<span data-ttu-id="faeeb-113">Gibt den Namen des RemoteApp-Vorlagenbilds an.</span><span class="sxs-lookup"><span data-stu-id="faeeb-113">Specifies the name of the RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faeeb-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="faeeb-114">-Profile</span></span>
<span data-ttu-id="faeeb-115">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="faeeb-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="faeeb-116">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="faeeb-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="faeeb-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="faeeb-117">-Confirm</span></span>
<span data-ttu-id="faeeb-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="faeeb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faeeb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faeeb-119">-WhatIf</span></span>
<span data-ttu-id="faeeb-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="faeeb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faeeb-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="faeeb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faeeb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faeeb-122">CommonParameters</span></span>
<span data-ttu-id="faeeb-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faeeb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faeeb-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faeeb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faeeb-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="faeeb-125">INPUTS</span></span>

## <span data-ttu-id="faeeb-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="faeeb-126">OUTPUTS</span></span>

## <span data-ttu-id="faeeb-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="faeeb-127">NOTES</span></span>

## <span data-ttu-id="faeeb-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="faeeb-128">RELATED LINKS</span></span>

[<span data-ttu-id="faeeb-129">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="faeeb-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="faeeb-130">Neu – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="faeeb-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="faeeb-131">Umbenennen – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="faeeb-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


