---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370878"
---
# <span data-ttu-id="b34fc-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="b34fc-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="b34fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b34fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b34fc-103">Bei den Azure-Kontexten handelt es sich um PowerShell-Objekte, die Ihr aktives Abonnement zum Ausführen von Befehlen darstellen, sowie die Authentifizierungsinformationen, die zum Herstellen einer Verbindung mit einer Azure Cloud erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b34fc-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="b34fc-104">Bei Azure-Kontexten muss Azure PowerShell Ihr Konto nicht jedes Mal neu authentifizieren, wenn Sie zwischen Abonnements wechseln.</span><span class="sxs-lookup"><span data-stu-id="b34fc-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="b34fc-105">Weitere Informationen finden Sie unter [Azure PowerShell-Kontextobjekten.](https://docs.microsoft.com/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="b34fc-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="b34fc-106">Mit diesem Cmdlet können die Azure-Kontextinformationen gespeichert und automatisch geladen werden, wenn Sie einen PowerShell-Prozess starten.</span><span class="sxs-lookup"><span data-stu-id="b34fc-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="b34fc-107">Beispielsweise beim Öffnen eines neuen Fensters.</span><span class="sxs-lookup"><span data-stu-id="b34fc-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="b34fc-108">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b34fc-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b34fc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b34fc-109">DESCRIPTION</span></span>

<span data-ttu-id="b34fc-110">Ermöglicht das Speichern und automatische Laden der Azure-Kontextinformationen, wenn ein PowerShell-Prozess gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b34fc-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="b34fc-111">Der Kontext wird am Ende der Ausführung eines Cmdlets gespeichert, das sich auf den Kontext auswirkt.</span><span class="sxs-lookup"><span data-stu-id="b34fc-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="b34fc-112">Beispiel: ein beliebiges Profil-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b34fc-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="b34fc-113">Wenn Sie die Benutzerauthentifizierung verwenden, können die Token während der Ausführung jedes Cmdlets aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b34fc-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="b34fc-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b34fc-114">EXAMPLES</span></span>

### <span data-ttu-id="b34fc-115">Beispiel 1: Aktivieren der automatischen Speicherung von Anmeldeinformationen für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="b34fc-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="b34fc-116">Aktivieren Sie die automatische Speicherung der Anmeldeinformationen für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b34fc-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="b34fc-117">Wenn ein PowerShell-Fenster geöffnet wird, wird der aktuelle Kontext ohne Anmeldung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b34fc-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="b34fc-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b34fc-118">Example 2</span></span>

<span data-ttu-id="b34fc-119">Lassen Sie zu, dass die Azure-Anmeldeinformationen, das Konto und die Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster in dieser PowerShell-Sitzung öffnen.</span><span class="sxs-lookup"><span data-stu-id="b34fc-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="b34fc-120">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="b34fc-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="b34fc-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b34fc-121">PARAMETERS</span></span>

### <span data-ttu-id="b34fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34fc-122">-DefaultProfile</span></span>

<span data-ttu-id="b34fc-123">Die Anmeldeinformationen, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b34fc-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="b34fc-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="b34fc-124">-Scope</span></span>

<span data-ttu-id="b34fc-125">Bestimmt den Umfang der Kontextänderungen.</span><span class="sxs-lookup"><span data-stu-id="b34fc-125">Determines the scope of context changes.</span></span> <span data-ttu-id="b34fc-126">Beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="b34fc-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="b34fc-127">Änderungen, die mit dem Bereich vorgenommen werden, wirken sich auf alle vom Benutzer `CurrentUser` gestarteten PowerShell-Sitzungen aus.</span><span class="sxs-lookup"><span data-stu-id="b34fc-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="b34fc-128">Wenn eine bestimmte Sitzung unterschiedliche Einstellungen haben muss, verwenden Sie den `Process` Bereich.</span><span class="sxs-lookup"><span data-stu-id="b34fc-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

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

### <span data-ttu-id="b34fc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b34fc-129">-Confirm</span></span>

<span data-ttu-id="b34fc-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b34fc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b34fc-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b34fc-131">-WhatIf</span></span>

<span data-ttu-id="b34fc-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b34fc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34fc-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b34fc-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="b34fc-134">Allgemeine Parameter</span><span class="sxs-lookup"><span data-stu-id="b34fc-134">Common Parameters</span></span>

<span data-ttu-id="b34fc-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34fc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34fc-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b34fc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34fc-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b34fc-137">INPUTS</span></span>

### <span data-ttu-id="b34fc-138">Keine</span><span class="sxs-lookup"><span data-stu-id="b34fc-138">None</span></span>

## <span data-ttu-id="b34fc-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b34fc-139">OUTPUTS</span></span>

### <span data-ttu-id="b34fc-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="b34fc-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="b34fc-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b34fc-141">NOTES</span></span>

## <span data-ttu-id="b34fc-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b34fc-142">RELATED LINKS</span></span>
