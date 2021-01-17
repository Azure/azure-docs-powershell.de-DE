---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471586"
---
# <span data-ttu-id="ac6de-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="ac6de-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="ac6de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac6de-102">SYNOPSIS</span></span>
<span data-ttu-id="ac6de-103">Anzeigen von Metadaten zum automatischen Speichern des Kontextfeatures, einschließlich Angaben dazu, ob der Kontext automatisch gespeichert wird und wo gespeicherte Kontext- und Anmeldeinformationen zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="ac6de-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="ac6de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac6de-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac6de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac6de-105">DESCRIPTION</span></span>
<span data-ttu-id="ac6de-106">Anzeigen von Metadaten zum automatischen Speichern des Kontextfeatures, einschließlich Angaben dazu, ob der Kontext automatisch gespeichert wird und wo gespeicherte Kontext- und Anmeldeinformationen zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="ac6de-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="ac6de-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac6de-107">EXAMPLES</span></span>

### <span data-ttu-id="ac6de-108">Kontextspeichern von Metadaten für die aktuelle Sitzung</span><span class="sxs-lookup"><span data-stu-id="ac6de-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="ac6de-109">Erfahren Sie mehr darüber, ob und wo der Kontext gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="ac6de-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="ac6de-110">Im vorstehenden Beispiel wurde das Feature "AutoAve" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ac6de-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="ac6de-111">Kontextspeichern von Metadaten für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="ac6de-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="ac6de-112">Erfahren Sie mehr darüber, ob und wo der Kontext für den aktuellen Benutzer standardmäßig gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="ac6de-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="ac6de-113">Beachten Sie, dass sich dies möglicherweise von den Einstellungen unterscheiden kann, die in der aktuellen Sitzung aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="ac6de-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="ac6de-114">Im vorstehenden Beispiel wurde das Feature "AutoSpeichern" aktiviert, und die Daten werden am Standardspeicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ac6de-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="ac6de-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac6de-115">PARAMETERS</span></span>

### <span data-ttu-id="ac6de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac6de-116">-DefaultProfile</span></span>
<span data-ttu-id="ac6de-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ac6de-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac6de-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="ac6de-118">-Scope</span></span>
<span data-ttu-id="ac6de-119">Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="ac6de-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ac6de-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac6de-120">CommonParameters</span></span>
<span data-ttu-id="ac6de-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac6de-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac6de-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac6de-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac6de-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac6de-123">INPUTS</span></span>

### <span data-ttu-id="ac6de-124">Keine</span><span class="sxs-lookup"><span data-stu-id="ac6de-124">None</span></span>

## <span data-ttu-id="ac6de-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac6de-125">OUTPUTS</span></span>

### <span data-ttu-id="ac6de-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="ac6de-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="ac6de-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ac6de-127">NOTES</span></span>

## <span data-ttu-id="ac6de-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ac6de-128">RELATED LINKS</span></span>
