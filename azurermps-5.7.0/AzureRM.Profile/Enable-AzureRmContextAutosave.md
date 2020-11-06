---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: 0e875087d52ecddbf216c6e49db96fefdf63e82f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502541"
---
# <span data-ttu-id="2bf11-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="2bf11-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="2bf11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bf11-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf11-103">Zulassen, dass Azure-Anmeldeinformationen, Konto-und Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="2bf11-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bf11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bf11-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf11-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bf11-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf11-106">Zulassen, dass Azure-Anmeldeinformationen, Konto-und Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="2bf11-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="2bf11-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bf11-107">EXAMPLES</span></span>

### <span data-ttu-id="2bf11-108">Aktivieren der AutoSpeichern-Anmeldeinformationen für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="2bf11-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="2bf11-109">Aktivieren Sie das automatische Speichern von Anmeldeinformationen für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="2bf11-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="2bf11-110">Wenn ein PowerShell-Fenster geöffnet wird, wird der aktuelle Kontext ohne Anmeldung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2bf11-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="2bf11-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bf11-111">PARAMETERS</span></span>

### <span data-ttu-id="2bf11-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf11-112">-DefaultProfile</span></span>
<span data-ttu-id="2bf11-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="2bf11-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bf11-114">-Scope</span><span class="sxs-lookup"><span data-stu-id="2bf11-114">-Scope</span></span>
<span data-ttu-id="2bf11-115">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="2bf11-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="2bf11-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2bf11-116">-Confirm</span></span>
<span data-ttu-id="2bf11-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2bf11-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bf11-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf11-118">-WhatIf</span></span>
<span data-ttu-id="2bf11-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bf11-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bf11-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2bf11-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bf11-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf11-121">CommonParameters</span></span>
<span data-ttu-id="2bf11-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf11-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf11-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bf11-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf11-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bf11-124">INPUTS</span></span>

### <span data-ttu-id="2bf11-125">Keine</span><span class="sxs-lookup"><span data-stu-id="2bf11-125">None</span></span>

## <span data-ttu-id="2bf11-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bf11-126">OUTPUTS</span></span>

### <span data-ttu-id="2bf11-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="2bf11-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="2bf11-128">Informationen zu den aktuellen AutoSpeichern-Einstellungen, einschließlich, ob Autosave für den aktuellen Benutzer aktiviert ist und wo Kontext-und Anmeldeinformationsdateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="2bf11-128">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="2bf11-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bf11-129">NOTES</span></span>

## <span data-ttu-id="2bf11-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bf11-130">RELATED LINKS</span></span>

