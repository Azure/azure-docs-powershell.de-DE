---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178472"
---
# <span data-ttu-id="a9d03-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="a9d03-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="a9d03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9d03-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d03-103">Azure-Kontexte sind PowerShell-Objekte, die das aktive Abonnement für die Ausführung von Befehlen darstellen, und die Authentifizierungsinformationen, die zum Herstellen einer Verbindung mit einer Azure-Cloud erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a9d03-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="a9d03-104">Bei Azure-Kontexten muss Azure PowerShell Ihr Konto nicht jedes Mal erneut authentifizieren, wenn Sie Abonnements wechseln.</span><span class="sxs-lookup"><span data-stu-id="a9d03-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="a9d03-105">Weitere Informationen finden Sie unter [Azure PowerShell-Kontextobjekte](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="a9d03-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="a9d03-106">Mit diesem Cmdlet können die Azure-Kontextinformationen gespeichert und beim Starten eines PowerShell-Prozesses automatisch geladen werden.</span><span class="sxs-lookup"><span data-stu-id="a9d03-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="a9d03-107">Beispielsweise beim Öffnen eines neuen Fensters.</span><span class="sxs-lookup"><span data-stu-id="a9d03-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="a9d03-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9d03-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d03-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9d03-109">DESCRIPTION</span></span>

<span data-ttu-id="a9d03-110">Ermöglicht das Speichern und Automatisches Laden der Azure-Kontextinformationen, wenn ein PowerShell-Prozess gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a9d03-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="a9d03-111">Der Kontext wird am Ende der Ausführung eines beliebigen Cmdlets gespeichert, das sich auf den Kontext auswirkt.</span><span class="sxs-lookup"><span data-stu-id="a9d03-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="a9d03-112">Beispiel: jedes Profil-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d03-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="a9d03-113">Wenn Sie die Benutzerauthentifizierung verwenden, können Token im Verlauf der Ausführung eines beliebigen Cmdlets aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9d03-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="a9d03-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9d03-114">EXAMPLES</span></span>

### <span data-ttu-id="a9d03-115">Beispiel 1: Aktivieren der AutoSpeichern-Anmeldeinformationen für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="a9d03-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="a9d03-116">Aktivieren Sie das automatische Speichern von Anmeldeinformationen für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="a9d03-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="a9d03-117">Wenn ein PowerShell-Fenster geöffnet wird, wird der aktuelle Kontext ohne Anmeldung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a9d03-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="a9d03-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a9d03-118">Example 2</span></span>

<span data-ttu-id="a9d03-119">Zulassen, dass die Azure-Anmeldeinformationen, das Konto und die Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster in dieser PowerShell-Sitzung öffnen.</span><span class="sxs-lookup"><span data-stu-id="a9d03-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="a9d03-120">automatisch</span><span class="sxs-lookup"><span data-stu-id="a9d03-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="a9d03-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9d03-121">PARAMETERS</span></span>

### <span data-ttu-id="a9d03-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d03-122">-DefaultProfile</span></span>

<span data-ttu-id="a9d03-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="a9d03-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="a9d03-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="a9d03-124">-Scope</span></span>

<span data-ttu-id="a9d03-125">Bestimmt den Bereich von Kontextänderungen.</span><span class="sxs-lookup"><span data-stu-id="a9d03-125">Determines the scope of context changes.</span></span> <span data-ttu-id="a9d03-126">So können Sie beispielsweise festlegen, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="a9d03-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="a9d03-127">Mit dem Bereich vorgenommene Änderungen `CurrentUser` wirken sich auf alle PowerShell-Sitzungen aus, die vom Benutzer gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="a9d03-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="a9d03-128">Wenn eine bestimmte Sitzung unterschiedliche Einstellungen aufweisen muss, verwenden Sie den Bereich `Process` .</span><span class="sxs-lookup"><span data-stu-id="a9d03-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d03-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9d03-129">-Confirm</span></span>

<span data-ttu-id="a9d03-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9d03-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d03-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d03-131">-WhatIf</span></span>

<span data-ttu-id="a9d03-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9d03-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9d03-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9d03-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="a9d03-134">Allgemeine Parameter</span><span class="sxs-lookup"><span data-stu-id="a9d03-134">Common Parameters</span></span>

<span data-ttu-id="a9d03-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d03-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d03-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9d03-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d03-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9d03-137">INPUTS</span></span>

### <span data-ttu-id="a9d03-138">Keine</span><span class="sxs-lookup"><span data-stu-id="a9d03-138">None</span></span>

## <span data-ttu-id="a9d03-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9d03-139">OUTPUTS</span></span>

### <span data-ttu-id="a9d03-140">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="a9d03-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="a9d03-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9d03-141">NOTES</span></span>

## <span data-ttu-id="a9d03-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9d03-142">RELATED LINKS</span></span>
