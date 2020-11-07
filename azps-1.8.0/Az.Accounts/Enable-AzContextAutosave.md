---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: eedd28fe1df7992658dfe9b36ebab58e77eb87c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650508"
---
# <span data-ttu-id="72685-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="72685-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="72685-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72685-102">SYNOPSIS</span></span>
<span data-ttu-id="72685-103">Zulassen, dass Azure-Anmeldeinformationen, Konto-und Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="72685-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="72685-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72685-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72685-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72685-105">DESCRIPTION</span></span>
<span data-ttu-id="72685-106">Zulassen, dass Azure-Anmeldeinformationen, Konto-und Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster öffnen.</span><span class="sxs-lookup"><span data-stu-id="72685-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="72685-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72685-107">EXAMPLES</span></span>

### <span data-ttu-id="72685-108">Aktivieren der AutoSpeichern-Anmeldeinformationen für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="72685-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="72685-109">Aktivieren Sie das automatische Speichern von Anmeldeinformationen für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="72685-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="72685-110">Wenn ein PowerShell-Fenster geöffnet wird, wird der aktuelle Kontext ohne Anmeldung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="72685-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="72685-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="72685-111">PARAMETERS</span></span>

### <span data-ttu-id="72685-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72685-112">-DefaultProfile</span></span>
<span data-ttu-id="72685-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="72685-113">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72685-114">-Scope</span><span class="sxs-lookup"><span data-stu-id="72685-114">-Scope</span></span>
<span data-ttu-id="72685-115">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="72685-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="72685-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72685-116">-Confirm</span></span>
<span data-ttu-id="72685-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72685-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72685-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72685-118">-WhatIf</span></span>
<span data-ttu-id="72685-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72685-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72685-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72685-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72685-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72685-121">CommonParameters</span></span>
<span data-ttu-id="72685-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72685-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72685-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72685-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72685-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72685-124">INPUTS</span></span>

### <span data-ttu-id="72685-125">Keine</span><span class="sxs-lookup"><span data-stu-id="72685-125">None</span></span>

## <span data-ttu-id="72685-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72685-126">OUTPUTS</span></span>

### <span data-ttu-id="72685-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="72685-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="72685-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="72685-128">NOTES</span></span>

## <span data-ttu-id="72685-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72685-129">RELATED LINKS</span></span>
