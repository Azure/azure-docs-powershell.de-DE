---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175324"
---
# <span data-ttu-id="cd72b-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="cd72b-101">Clear-AzContext</span></span>

## <span data-ttu-id="cd72b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd72b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd72b-103">Entfernen Sie alle Azure-Anmeldeinformationen, Konto-und Abonnementinformationen.</span><span class="sxs-lookup"><span data-stu-id="cd72b-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="cd72b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd72b-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd72b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd72b-105">DESCRIPTION</span></span>
<span data-ttu-id="cd72b-106">Entfernen Sie alle Azure-Anmeldeinformationen, Konto-und Abonnementinformationen.</span><span class="sxs-lookup"><span data-stu-id="cd72b-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="cd72b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd72b-107">EXAMPLES</span></span>

### <span data-ttu-id="cd72b-108">Beispiel 1: Löschen des globalen Kontexts</span><span class="sxs-lookup"><span data-stu-id="cd72b-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="cd72b-109">Entfernen Sie alle Konto-, Abonnement-und Anmeldeinformationen für eine beliebige PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="cd72b-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="cd72b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd72b-110">PARAMETERS</span></span>

### <span data-ttu-id="cd72b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd72b-111">-DefaultProfile</span></span>
<span data-ttu-id="cd72b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements</span><span class="sxs-lookup"><span data-stu-id="cd72b-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd72b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cd72b-113">-Force</span></span>
<span data-ttu-id="cd72b-114">Löschen aller Benutzer und Gruppen aus dem globalen Bereich ohne Aufforderung</span><span class="sxs-lookup"><span data-stu-id="cd72b-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="cd72b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd72b-115">-PassThru</span></span>
<span data-ttu-id="cd72b-116">Zurückgeben eines Werts, der auf Erfolg oder Fehler hinweist</span><span class="sxs-lookup"><span data-stu-id="cd72b-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="cd72b-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="cd72b-117">-Scope</span></span>
<span data-ttu-id="cd72b-118">Löschen Sie den Kontext nur für die aktuelle PowerShell-Sitzung oder für alle Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="cd72b-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="cd72b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd72b-119">-Confirm</span></span>
<span data-ttu-id="cd72b-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd72b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd72b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd72b-121">-WhatIf</span></span>
<span data-ttu-id="cd72b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd72b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd72b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd72b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd72b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd72b-124">CommonParameters</span></span>
<span data-ttu-id="cd72b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd72b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd72b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd72b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd72b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd72b-127">INPUTS</span></span>

### <span data-ttu-id="cd72b-128">Keine</span><span class="sxs-lookup"><span data-stu-id="cd72b-128">None</span></span>

## <span data-ttu-id="cd72b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd72b-129">OUTPUTS</span></span>

### <span data-ttu-id="cd72b-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd72b-130">System.Boolean</span></span>

## <span data-ttu-id="cd72b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd72b-131">NOTES</span></span>

## <span data-ttu-id="cd72b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd72b-132">RELATED LINKS</span></span>
