---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: 60120e66596830e018351ceb492a36cd1ad1032d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496965"
---
# <span data-ttu-id="3aef9-101">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="3aef9-101">Get-AzureRmContextAutosaveSetting</span></span>

## <span data-ttu-id="3aef9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3aef9-102">SYNOPSIS</span></span>
<span data-ttu-id="3aef9-103">Anzeigen von Metadaten über das Feature zum Speichern von Kontexten, einschließlich whterh der Kontext wird automatisch Aved, und wo gespeicherte Kontext-und Anmeldeinformationen gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="3aef9-103">Display metadata about the context autosave feature, including whterh the context is automaticallys aved, and where saved context and credential information cna be found.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aef9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aef9-104">SYNTAX</span></span>

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aef9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3aef9-105">DESCRIPTION</span></span>
<span data-ttu-id="3aef9-106">Anzeigen von Metadaten über das Feature zum Speichern von Kontexten, einschließlich, ob der Kontext automatisch gespeichert wird und wo gespeicherte Kontext-und Anmeldeinformationen gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="3aef9-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="3aef9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3aef9-107">EXAMPLES</span></span>

### <span data-ttu-id="3aef9-108">Kontext Speichermetadaten für die aktuelle Sitzung abrufen</span><span class="sxs-lookup"><span data-stu-id="3aef9-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="3aef9-109">Hier erhalten Sie Informationen darüber, ob und erwarteten der Kontext gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3aef9-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="3aef9-110">Im obigen Beispiel wurde das Autosave-Feature deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3aef9-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="3aef9-111">Kontext Speichermetadaten für den aktuellen Benutzer abrufen</span><span class="sxs-lookup"><span data-stu-id="3aef9-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="3aef9-112">Abrufen von Details darüber, ob und erwarteten der Kontext standardmäßig für den aktuellen Benutzer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3aef9-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="3aef9-113">Beachten Sie, dass dies von den Einstellungen abweichen kann, die in der aktuellen Sitzung aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="3aef9-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="3aef9-114">Im obigen Beispiel wurde das Autosave-Feature aktiviert, und die Daten werden am Standardspeicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3aef9-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="3aef9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3aef9-115">PARAMETERS</span></span>

### <span data-ttu-id="3aef9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aef9-116">-DefaultProfile</span></span>
<span data-ttu-id="3aef9-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3aef9-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3aef9-118">-Scope</span><span class="sxs-lookup"><span data-stu-id="3aef9-118">-Scope</span></span>
<span data-ttu-id="3aef9-119">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="3aef9-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3aef9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aef9-120">CommonParameters</span></span>
<span data-ttu-id="3aef9-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aef9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aef9-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aef9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aef9-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3aef9-123">INPUTS</span></span>

### <span data-ttu-id="3aef9-124">Keine</span><span class="sxs-lookup"><span data-stu-id="3aef9-124">None</span></span>

## <span data-ttu-id="3aef9-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3aef9-125">OUTPUTS</span></span>

### <span data-ttu-id="3aef9-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="3aef9-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="3aef9-127">Informationen zu den aktuellen AutoSpeichern-Einstellungen, einschließlich, ob Autosave für den aktuellen Benutzer aktiviert ist und wo Kontext-und Anmeldeinformationsdateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3aef9-127">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="3aef9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3aef9-128">NOTES</span></span>

## <span data-ttu-id="3aef9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3aef9-129">RELATED LINKS</span></span>

