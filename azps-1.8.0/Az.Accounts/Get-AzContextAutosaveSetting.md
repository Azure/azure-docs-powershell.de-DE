---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: a6361fabaa05d99b35874ce0de388ed0fc1bdfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650503"
---
# <span data-ttu-id="40659-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="40659-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="40659-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40659-102">SYNOPSIS</span></span>
<span data-ttu-id="40659-103">Anzeigen von Metadaten über das Feature zum Speichern von Kontexten, einschließlich, ob der Kontext automatisch gespeichert wird und wo gespeicherte Kontext-und Anmeldeinformationen gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="40659-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="40659-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40659-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40659-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40659-105">DESCRIPTION</span></span>
<span data-ttu-id="40659-106">Anzeigen von Metadaten über das Feature zum Speichern von Kontexten, einschließlich, ob der Kontext automatisch gespeichert wird und wo gespeicherte Kontext-und Anmeldeinformationen gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="40659-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="40659-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40659-107">EXAMPLES</span></span>

### <span data-ttu-id="40659-108">Kontext Speichermetadaten für die aktuelle Sitzung abrufen</span><span class="sxs-lookup"><span data-stu-id="40659-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="40659-109">Hier erhalten Sie Informationen darüber, ob und erwarteten der Kontext gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="40659-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="40659-110">Im obigen Beispiel wurde das Autosave-Feature deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="40659-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="40659-111">Kontext Speichermetadaten für den aktuellen Benutzer abrufen</span><span class="sxs-lookup"><span data-stu-id="40659-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="40659-112">Abrufen von Details darüber, ob und erwarteten der Kontext standardmäßig für den aktuellen Benutzer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="40659-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="40659-113">Beachten Sie, dass dies von den Einstellungen abweichen kann, die in der aktuellen Sitzung aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="40659-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="40659-114">Im obigen Beispiel wurde das Autosave-Feature aktiviert, und die Daten werden am Standardspeicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="40659-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="40659-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="40659-115">PARAMETERS</span></span>

### <span data-ttu-id="40659-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40659-116">-DefaultProfile</span></span>
<span data-ttu-id="40659-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="40659-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40659-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="40659-118">-Scope</span></span>
<span data-ttu-id="40659-119">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="40659-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="40659-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40659-120">CommonParameters</span></span>
<span data-ttu-id="40659-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40659-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40659-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40659-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40659-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40659-123">INPUTS</span></span>

### <span data-ttu-id="40659-124">Keine</span><span class="sxs-lookup"><span data-stu-id="40659-124">None</span></span>

## <span data-ttu-id="40659-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40659-125">OUTPUTS</span></span>

### <span data-ttu-id="40659-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="40659-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="40659-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="40659-127">NOTES</span></span>

## <span data-ttu-id="40659-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40659-128">RELATED LINKS</span></span>
