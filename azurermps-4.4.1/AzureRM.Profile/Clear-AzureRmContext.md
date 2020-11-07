---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 5a640bf705040c3bb8ed0f7dc985693b2e57c873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664743"
---
# <span data-ttu-id="4761d-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="4761d-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="4761d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4761d-102">SYNOPSIS</span></span>
<span data-ttu-id="4761d-103">Entfernen Sie alle Azure-Anmeldeinformationen, Konto-und Abonnementinformationen.</span><span class="sxs-lookup"><span data-stu-id="4761d-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4761d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4761d-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4761d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4761d-105">DESCRIPTION</span></span>
<span data-ttu-id="4761d-106">Entfernen Sie alle Azure-Anmeldeinformationen, Konto-und Abonnementinformationen.</span><span class="sxs-lookup"><span data-stu-id="4761d-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="4761d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4761d-107">EXAMPLES</span></span>

### <span data-ttu-id="4761d-108">Globaler Kontext löschen</span><span class="sxs-lookup"><span data-stu-id="4761d-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="4761d-109">Entfernen Sie alle Konto-, Abonnement-und Anmeldeinformationen für eine beliebige PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="4761d-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="4761d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4761d-110">PARAMETERS</span></span>

### <span data-ttu-id="4761d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4761d-111">-DefaultProfile</span></span>
<span data-ttu-id="4761d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="4761d-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4761d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4761d-113">-Force</span></span>
<span data-ttu-id="4761d-114">Löschen aller Benutzer und Gruppen aus dem globalen Bereich ohne Aufforderung</span><span class="sxs-lookup"><span data-stu-id="4761d-114">Delete all users and groups from the global scope without prompting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4761d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4761d-115">-PassThru</span></span>
<span data-ttu-id="4761d-116">Zurückgeben eines Werts, der auf Erfolg oder Fehler hinweist</span><span class="sxs-lookup"><span data-stu-id="4761d-116">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4761d-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="4761d-117">-Scope</span></span>
<span data-ttu-id="4761d-118">Löschen Sie den Kontext nur für die aktuelle PowerShell-Sitzung oder für alle Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="4761d-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4761d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4761d-119">-Confirm</span></span>
<span data-ttu-id="4761d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4761d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4761d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4761d-121">-WhatIf</span></span>
<span data-ttu-id="4761d-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4761d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4761d-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4761d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4761d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4761d-124">CommonParameters</span></span>
<span data-ttu-id="4761d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4761d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4761d-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4761d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4761d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4761d-127">INPUTS</span></span>

### <span data-ttu-id="4761d-128">Keine</span><span class="sxs-lookup"><span data-stu-id="4761d-128">None</span></span>

## <span data-ttu-id="4761d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4761d-129">OUTPUTS</span></span>

### <span data-ttu-id="4761d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4761d-130">System.Boolean</span></span>
<span data-ttu-id="4761d-131">"True", wenn der Kontext erfolgreich gelöscht wurde; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="4761d-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="4761d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="4761d-132">NOTES</span></span>

## <span data-ttu-id="4761d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4761d-133">RELATED LINKS</span></span>

