---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145372"
---
# <span data-ttu-id="895b1-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="895b1-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="895b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="895b1-102">SYNOPSIS</span></span>
<span data-ttu-id="895b1-103">Deaktiviert AzureRm-Präfixaliase für Az-Module.</span><span class="sxs-lookup"><span data-stu-id="895b1-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="895b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="895b1-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="895b1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="895b1-105">DESCRIPTION</span></span>
<span data-ttu-id="895b1-106">Deaktiviert AzureRm-Präfixaliase für Az-Module.</span><span class="sxs-lookup"><span data-stu-id="895b1-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="895b1-107">Wenn "-Module" angegeben ist, sind die Aliase nur für die aufgelisteten Module deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="895b1-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="895b1-108">Andernfalls werden alle AzureRm-Aliase deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="895b1-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="895b1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="895b1-109">EXAMPLES</span></span>

### <span data-ttu-id="895b1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="895b1-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="895b1-111">Deaktiviert alle AzureRm-Präfixe für die aktuelle PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="895b1-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="895b1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="895b1-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="895b1-113">Deaktiviert die AzureRm-Aliase für das Modul "Az.Accounts" sowohl für den aktuellen Prozess als auch für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="895b1-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="895b1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="895b1-114">PARAMETERS</span></span>

### <span data-ttu-id="895b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="895b1-115">-DefaultProfile</span></span>
<span data-ttu-id="895b1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="895b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="895b1-117">-Module</span><span class="sxs-lookup"><span data-stu-id="895b1-117">-Module</span></span>
<span data-ttu-id="895b1-118">Gibt an, für welche Module Aliase deaktiviert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="895b1-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="895b1-119">Wenn keines angegeben wird, sind standardmäßig alle Module aktiviert.</span><span class="sxs-lookup"><span data-stu-id="895b1-119">If none are specified, default is all enabled modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895b1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="895b1-120">-PassThru</span></span>
<span data-ttu-id="895b1-121">Falls angegeben, gibt das Cmdlet alle deaktivierten Aliase zurück.</span><span class="sxs-lookup"><span data-stu-id="895b1-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="895b1-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="895b1-122">-Scope</span></span>
<span data-ttu-id="895b1-123">Gibt an, für welche Bereichsaliase deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="895b1-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="895b1-124">Der Standardwert ist "Prozess".</span><span class="sxs-lookup"><span data-stu-id="895b1-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895b1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="895b1-125">-Confirm</span></span>
<span data-ttu-id="895b1-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="895b1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="895b1-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="895b1-127">-WhatIf</span></span>
<span data-ttu-id="895b1-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="895b1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="895b1-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="895b1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="895b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="895b1-130">CommonParameters</span></span>
<span data-ttu-id="895b1-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="895b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="895b1-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="895b1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="895b1-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="895b1-133">INPUTS</span></span>

### <span data-ttu-id="895b1-134">Keine</span><span class="sxs-lookup"><span data-stu-id="895b1-134">None</span></span>

## <span data-ttu-id="895b1-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="895b1-135">OUTPUTS</span></span>

### <span data-ttu-id="895b1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="895b1-136">System.String</span></span>

## <span data-ttu-id="895b1-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="895b1-137">NOTES</span></span>

## <span data-ttu-id="895b1-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="895b1-138">RELATED LINKS</span></span>
