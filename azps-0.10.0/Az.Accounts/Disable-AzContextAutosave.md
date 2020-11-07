---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: f268c4171be78265843d5a04291bf430dc4f19b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841115"
---
# <span data-ttu-id="d167b-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="d167b-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="d167b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d167b-102">SYNOPSIS</span></span>
<span data-ttu-id="d167b-103">Deaktivieren Sie die autospeichernden Azure-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="d167b-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="d167b-104">Wenn Sie das nächste Mal ein PowerShell-Fenster öffnen, werden Ihre Anmeldeinformationen vergessen</span><span class="sxs-lookup"><span data-stu-id="d167b-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="d167b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d167b-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d167b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d167b-106">DESCRIPTION</span></span>
<span data-ttu-id="d167b-107">Deaktivieren Sie die autospeichernden Azure-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="d167b-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="d167b-108">Wenn Sie das nächste Mal ein PowerShell-Fenster öffnen, werden Ihre Anmeldeinformationen vergessen</span><span class="sxs-lookup"><span data-stu-id="d167b-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="d167b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d167b-109">EXAMPLES</span></span>

### <span data-ttu-id="d167b-110">Deaktivieren des Kontexts für das AutoSpeichern</span><span class="sxs-lookup"><span data-stu-id="d167b-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="d167b-111">Deaktivieren Sie AutoSpeichern für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d167b-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="d167b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d167b-112">PARAMETERS</span></span>

### <span data-ttu-id="d167b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d167b-113">-DefaultProfile</span></span>
<span data-ttu-id="d167b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="d167b-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d167b-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="d167b-115">-Scope</span></span>
<span data-ttu-id="d167b-116">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="d167b-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="d167b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d167b-117">-Confirm</span></span>
<span data-ttu-id="d167b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d167b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d167b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d167b-119">-WhatIf</span></span>
<span data-ttu-id="d167b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d167b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d167b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d167b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d167b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d167b-122">CommonParameters</span></span>
<span data-ttu-id="d167b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d167b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d167b-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d167b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d167b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d167b-125">INPUTS</span></span>

### <span data-ttu-id="d167b-126">Keine</span><span class="sxs-lookup"><span data-stu-id="d167b-126">None</span></span>

## <span data-ttu-id="d167b-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d167b-127">OUTPUTS</span></span>

### <span data-ttu-id="d167b-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="d167b-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="d167b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="d167b-129">NOTES</span></span>

## <span data-ttu-id="d167b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d167b-130">RELATED LINKS</span></span>
