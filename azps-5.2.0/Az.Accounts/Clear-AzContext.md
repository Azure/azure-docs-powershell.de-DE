---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291791"
---
# <span data-ttu-id="9d341-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="9d341-101">Clear-AzContext</span></span>

## <span data-ttu-id="9d341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d341-102">SYNOPSIS</span></span>
<span data-ttu-id="9d341-103">Entfernen Sie alle Azure-Anmeldeinformationen, das Konto und die Abonnementinformationen.</span><span class="sxs-lookup"><span data-stu-id="9d341-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="9d341-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d341-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d341-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d341-105">DESCRIPTION</span></span>
<span data-ttu-id="9d341-106">Entfernen Sie alle Azure-Anmeldeinformationen, das Konto und die Abonnementinformationen.</span><span class="sxs-lookup"><span data-stu-id="9d341-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="9d341-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d341-107">EXAMPLES</span></span>

### <span data-ttu-id="9d341-108">Beispiel 1: Löschen des globalen Kontexts</span><span class="sxs-lookup"><span data-stu-id="9d341-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="9d341-109">Entfernen Sie alle Konto-, Abonnement- und Anmeldeinformationen für jede Powershell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9d341-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="9d341-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d341-110">PARAMETERS</span></span>

### <span data-ttu-id="9d341-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d341-111">-DefaultProfile</span></span>
<span data-ttu-id="9d341-112">Die Anmeldeinformationen, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9d341-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d341-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9d341-113">-Force</span></span>
<span data-ttu-id="9d341-114">Löschen aller Benutzer und Gruppen aus dem globalen Bereich ohne Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="9d341-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="9d341-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d341-115">-PassThru</span></span>
<span data-ttu-id="9d341-116">Zurückgeben eines Werts, der Erfolg oder Misserfolg angibt</span><span class="sxs-lookup"><span data-stu-id="9d341-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="9d341-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="9d341-117">-Scope</span></span>
<span data-ttu-id="9d341-118">Löschen Sie den Kontext nur für die aktuelle oder für alle Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="9d341-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="9d341-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d341-119">-Confirm</span></span>
<span data-ttu-id="9d341-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d341-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d341-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9d341-121">-WhatIf</span></span>
<span data-ttu-id="9d341-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d341-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d341-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d341-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d341-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d341-124">CommonParameters</span></span>
<span data-ttu-id="9d341-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d341-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d341-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d341-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d341-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d341-127">INPUTS</span></span>

### <span data-ttu-id="9d341-128">Keine</span><span class="sxs-lookup"><span data-stu-id="9d341-128">None</span></span>

## <span data-ttu-id="9d341-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d341-129">OUTPUTS</span></span>

### <span data-ttu-id="9d341-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d341-130">System.Boolean</span></span>

## <span data-ttu-id="9d341-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d341-131">NOTES</span></span>

## <span data-ttu-id="9d341-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d341-132">RELATED LINKS</span></span>
