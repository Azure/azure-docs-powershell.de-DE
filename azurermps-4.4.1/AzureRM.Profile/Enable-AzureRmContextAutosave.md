---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: d785cd364cd67a9d79f8710ef664048b8f54b8ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496974"
---
# <span data-ttu-id="004cd-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="004cd-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="004cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="004cd-102">SYNOPSIS</span></span>
<span data-ttu-id="004cd-103">Zulassen, dass Azure-Anmeldeinformationen, Konto-und Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="004cd-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="004cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="004cd-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="004cd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="004cd-105">DESCRIPTION</span></span>
<span data-ttu-id="004cd-106">Zulassen, dass Azure-Anmeldeinformationen, Konto-und Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="004cd-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="004cd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="004cd-107">EXAMPLES</span></span>

### <span data-ttu-id="004cd-108">Aktivieren der AutoSpeichern-Anmeldeinformationen für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="004cd-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="004cd-109">Aktivieren Sie das automatische Speichern von Anmeldeinformationen für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="004cd-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="004cd-110">Wenn ein PowerShell-Fenster geöffnet wird, wird der aktuelle Kontext ohne Anmeldung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="004cd-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="004cd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="004cd-111">PARAMETERS</span></span>

### <span data-ttu-id="004cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004cd-112">-DefaultProfile</span></span>
<span data-ttu-id="004cd-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="004cd-113">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-114">-Scope</span><span class="sxs-lookup"><span data-stu-id="004cd-114">-Scope</span></span>
<span data-ttu-id="004cd-115">Bestimmt den Bereich von Kontextänderungen, beispielsweise wheher Änderungen gelten nur für den cusrrent-Prozess oder für alle von diesem Benutzer gestarteten Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="004cd-115">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="004cd-116">-Confirm</span></span>
<span data-ttu-id="004cd-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="004cd-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004cd-118">-WhatIf</span></span>
<span data-ttu-id="004cd-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="004cd-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="004cd-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="004cd-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004cd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004cd-121">CommonParameters</span></span>
<span data-ttu-id="004cd-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004cd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004cd-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="004cd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004cd-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="004cd-124">INPUTS</span></span>

### <span data-ttu-id="004cd-125">Keine</span><span class="sxs-lookup"><span data-stu-id="004cd-125">None</span></span>

## <span data-ttu-id="004cd-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="004cd-126">OUTPUTS</span></span>

### <span data-ttu-id="004cd-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="004cd-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="004cd-128">Informationen zu den aktuellen AutoSpeichern-Einstellungen, einschließlich, ob Autosave für den aktuellen Benutzer aktiviert ist und wo Kontext-und Anmeldeinformationsdateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="004cd-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="004cd-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="004cd-129">NOTES</span></span>

## <span data-ttu-id="004cd-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="004cd-130">RELATED LINKS</span></span>

