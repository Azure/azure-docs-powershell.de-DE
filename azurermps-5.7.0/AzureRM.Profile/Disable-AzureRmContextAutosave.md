---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 622cbd399f554173bbe9734429f4ae787fe94d0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476686"
---
# <span data-ttu-id="3a9de-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="3a9de-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="3a9de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a9de-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9de-103">Deaktivieren Sie die autospeichernden Azure-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="3a9de-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="3a9de-104">Wenn Sie das nächste Mal ein PowerShell-Fenster öffnen, werden Ihre Anmeldeinformationen vergessen</span><span class="sxs-lookup"><span data-stu-id="3a9de-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a9de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a9de-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a9de-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a9de-106">DESCRIPTION</span></span>
<span data-ttu-id="3a9de-107">Deaktivieren Sie die autospeichernden Azure-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="3a9de-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="3a9de-108">Wenn Sie das nächste Mal ein PowerShell-Fenster öffnen, werden Ihre Anmeldeinformationen vergessen</span><span class="sxs-lookup"><span data-stu-id="3a9de-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="3a9de-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a9de-109">EXAMPLES</span></span>

### <span data-ttu-id="3a9de-110">Deaktivieren des Kontexts für das AutoSpeichern</span><span class="sxs-lookup"><span data-stu-id="3a9de-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="3a9de-111">Deaktivieren Sie AutoSpeichern für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3a9de-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="3a9de-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a9de-112">PARAMETERS</span></span>

### <span data-ttu-id="3a9de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9de-113">-DefaultProfile</span></span>
<span data-ttu-id="3a9de-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="3a9de-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9de-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="3a9de-115">-Scope</span></span>
<span data-ttu-id="3a9de-116">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="3a9de-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9de-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a9de-117">-Confirm</span></span>
<span data-ttu-id="3a9de-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a9de-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9de-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9de-119">-WhatIf</span></span>
<span data-ttu-id="3a9de-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a9de-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a9de-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a9de-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9de-122">CommonParameters</span></span>
<span data-ttu-id="3a9de-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a9de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9de-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a9de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9de-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a9de-125">INPUTS</span></span>

### <span data-ttu-id="3a9de-126">Keine</span><span class="sxs-lookup"><span data-stu-id="3a9de-126">None</span></span>

## <span data-ttu-id="3a9de-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a9de-127">OUTPUTS</span></span>

### <span data-ttu-id="3a9de-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="3a9de-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="3a9de-129">Informationen zu den aktuellen AutoSpeichern-Einstellungen, einschließlich, ob Autosave für den aktuellen Benutzer aktiviert ist und wo Kontext-und Anmeldeinformationsdateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3a9de-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="3a9de-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a9de-130">NOTES</span></span>

## <span data-ttu-id="3a9de-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a9de-131">RELATED LINKS</span></span>

